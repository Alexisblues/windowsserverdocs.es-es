---
ms.assetid: a7c39656-81ee-4c2b-80ef-4d017dd11b07
title: Planeación de una implementación de carpetas de trabajo
ms.topic: article
author: JasonGerend
manager: dongill
ms.author: jgerend
ms.date: 4/5/2017
description: Cómo planear una implementación de carpetas de trabajo, incluidos los requisitos del sistema y cómo preparar el entorno de red.
ms.openlocfilehash: 3f082a9542853f822b2b493cf3dabafe2cd65add
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87954592"
---
# <a name="planning-a-work-folders-deployment"></a>Planeación de una implementación de carpetas de trabajo

>Se aplica a: Windows Server (canal semianual), Windows Server 2016, Windows Server 2012 R2, Windows 10, Windows 8.1, Windows 7

En este tema se explica el proceso de diseño de una implementación de Carpetas de trabajo. Se entiende que el usuario ya cuenta con lo siguiente:

- Conozca los aspectos básicos de las carpetas de trabajo (como se describe en [carpetas de trabajo](work-folders-overview.md))

- Conocimientos básicos sobre los conceptos de Servicios de dominio de Active Directory (AD DS)

- Conocimientos básicos sobre el uso compartido de archivos de Windows y tecnologías relacionadas

- Conocimientos básicos sobre el uso de certificados SSL

- Conocimientos básicos sobre cómo habilitar el acceso web a recursos internos a través de un proxy inverso web

  Las siguientes secciones le servirán para diseñar su implementación de Carpetas de trabajo. La implementación de Carpetas de trabajo se detalla en el siguiente tema, [Implementar Carpetas de trabajo](deploy-work-folders.md).

##  <a name="software-requirements"></a><a name="BKMK_SOFT"></a>Requisitos de software

Carpetas de trabajo presenta los siguientes requisitos de software en cuanto a servidores de archivos e infraestructura de red:

-   Un servidor que ejecuta Windows Server 2012 R2 o Windows Server 2016 para hospedar recursos compartidos de sincronización con archivos de usuario

-   Un volumen con formato de sistema de archivos NTFS para almacenar archivos de usuario

-   Para aplicar directivas de contraseña en equipos con Windows 7, debe usar las directivas de contraseña de directiva de grupo. También debe excluir los equipos con Windows 7 de las directivas de contraseña de Carpetas de trabajo (si es que los usa).

-   Un certificado de servidor para cada servidor de archivos que vaya a hospedar carpetas de trabajo. Estos certificados deben provienen de una entidad de certificación (CA) que sea de confianza para los usuarios, idealmente una CA pública.

-   Opta Un bosque de Active Directory Domain Services con extensiones de esquema en Windows Server 2012 R2 para admitir automáticamente la referencia de equipos y dispositivos al servidor de archivos correcto al usar varios servidores de archivos.

Existen más requisitos para permitir que los usuarios sincronicen a través de Internet:

-   La capacidad de hacer que un servidor sea accesible desde Internet mediante la creación de reglas de publicación en el proxy inverso o la puerta de enlace de red de la organización.

-   Opta Un nombre de dominio registrado públicamente y la capacidad de crear más registros DNS públicos para el dominio

-   (Opcional) Una infraestructura de Servicios de federación de Active Directory (AD FS) cuando se use la autenticación de AD FS.

Carpetas de trabajo presenta los siguientes requisitos de software relativos a los equipos cliente:

-   Los equipos deben ejecutar uno de los siguientes sistemas operativos:

    -   Windows 10

    -   Windows 8.1

    -   Windows RT 8.1

    -   Windows 7

    -   Android 4,4 KitKat y versiones posteriores

    -   iOS 10.2 y versiones posteriores

-   Los equipos con Windows 7 deben ejecutar una de las siguientes ediciones de Windows:

    -   Windows 7 Professional

    -   Windows 7 Ultimate

    -   Windows 7 Enterprise

-   Los equipos con Windows 7 deben estar Unidos al dominio de su organización (no pueden unirse a un grupo de trabajo).

-   Suficiente espacio disponible en una unidad local con formato NTFS para almacenar todos los archivos de usuario en carpetas de trabajo, además de 6 GB adicionales de espacio disponible si carpetas de trabajo se encuentra en la unidad del sistema, como de forma predeterminada. Carpetas de trabajo usa la siguiente ubicación de forma predeterminada **%USERPROFILE%\Work Folders**

     No obstante, esta ubicación se puede modificar durante la instalación (se pueden usar ubicaciones como tarjetas microSD y unidades USB con el formato del sistema de archivos NTFS, pero cabe recordar que la sincronización se detendrá si se extraen las unidades).

     El tamaño máximo de los archivos individuales es de 10 GB de forma predeterminada. No existe límite de almacenamiento por usuario, si bien los administradores pueden hacer uso de la función de cuotas del Administrador de recursos del servidor de archivos para implementar cuotas.

-   Carpetas de trabajo no admite revertir el estado de la máquina virtual de las máquinas virtuales cliente. realice en su lugar operaciones de copia de seguridad y restauración desde la máquina virtual cliente, ya sea por medio de Copia de seguridad de imagen del sistema o de cualquier otra aplicación de copia de seguridad.

> [!NOTE]
>  Asegúrese de instalar el paquete acumulativo de actualizaciones de disponibilidad general de Windows 8.1 y Windows Server 2012 R2 en todos los servidores de carpetas de trabajo y los equipos cliente que ejecuten Windows 8.1 o Windows Server 2012 R2. Para más información, vea el artículo [2883200](https://support.microsoft.com/kb/2883200) en Microsoft Knowledge Base.

## <a name="deployment-scenarios"></a>Escenarios de implementación
 Carpetas de trabajo se puede implementar en un número indeterminado de servidores de archivos de un entorno de cliente. Esto hace que Carpetas de trabajo pueda escalar de acuerdo con las necesidades del cliente, de modo que las implementaciones son tremendamente individualizadas. No obstante, casi todas las implementaciones coinciden con uno de los tres siguientes escenarios básicos.

### <a name="single-site-deployment"></a>Implementación de sitio único
 En una implementación de sitio único, los servidores de archivos se hospedan en un sitio central dentro de la infraestructura del cliente. Este tipo de implementación es más frecuente en clientes con una infraestructura muy centralizada o con pequeñas sucursales que no mantienen servidores de archivos locales. Se trata de un modelo de implementación más fácil de administrar para el personal de TI, ya que todos los activos de servidor son locales y la entrada/salida de Internet probablemente esté centralizada también en esa ubicación. Sin embargo, este modelo depende de una buena conectividad de WAN entre el sitio central y las sucursales, con lo cual los usuarios de las sucursales están expuestos a posibles interrupciones del servicio a causa del estado de la red.

### <a name="multiple-site-deployment"></a>Implementación con varios sitios
 En una implementación de varios sitios, los servidores de archivos se hospedan en varias ubicaciones dentro de la infraestructura del cliente. que podrían ser varios centros de datos o varias sucursales donde se mantienen los servidores de archivos. Este tipo de implementación es el habitual en entornos de cliente de mayor tamaño o en clientes con varias sucursales grandes donde se mantienen activos de servidores locales. Se trata de un modelo de implementación más difícil de administrar para el personal de TI y que depende de una minuciosa coordinación entre el almacenamiento de datos y el mantenimiento de Servicios de dominio de Active Directory (AD DS) para garantizar que los usuarios usen el servidor de sincronización adecuado para Carpetas de trabajo.

### <a name="hosted-deployment"></a>Implementación hospedada
 En una implementación hospedada, los servidores de sincronización están implementados en una solución IaaS (infraestructura como servicio) como, por ejemplo, VM de Windows Azure. Este método de implementación tiene la ventaja de que la disponibilidad de los servidores de archivos es menos dependiente de la conectividad WAN dentro de la empresa de un cliente. Si un dispositivo puede conectarse a Internet, podrá tener acceso a su servidor de sincronización. Sin embargo, los servidores implementados en el entorno hospedado todavía tienen que ser capaces de llegar al dominio de Active Directory de la organización para autenticar a los usuarios, y el cliente de los requisitos de infraestructura local para la complejidad adicional en el mantenimiento de la conexión.

## <a name="deployment-technologies"></a>Tecnologías de implementación
 Las implementaciones de Carpetas de trabajo constan de una serie de tecnologías que funcionan de manera conjunta para prestar servicio a dispositivos en redes tanto internas como externas. Antes de diseñar una implementación de Carpetas de trabajo, los clientes deben estar familiarizados con los requisitos de cada una de las siguientes tecnologías.

### <a name="active-directory-domain-services"></a>Active Directory Domain Services
 AD DS proporciona dos servicios importantes en una implementación de Carpetas de trabajo. En primer lugar, como el back-end de la autenticación de Windows, AD DS presta los servicios de autenticación y seguridad que se usan para dar acceso a los datos de usuario. Si no se puede tener acceso a un controlador de dominio, un servidor de archivos no podrá autenticar una solicitud entrante y el dispositivo no podrá acceder a los datos almacenados en el recurso compartido de sincronización del servidor de archivos.

 En segundo lugar, AD DS (con la actualización de esquema de Windows Server 2012 R2) mantiene el atributo msDS-SyncServerURL en cada usuario, que se usa para dirigir automáticamente a los usuarios al servidor de sincronización adecuado.

### <a name="file-servers"></a>Servidores de archivos
 Los servidores de archivos que ejecutan Windows Server 2012 R2 o Windows Server 2016 hospedan el servicio de rol carpetas de trabajo y hospedan los recursos compartidos de sincronización que almacenan los datos de carpetas de trabajo de los usuarios. Los servidores de archivos también pueden hospedar los datos almacenados por otras tecnologías activas en la red interna (como los recursos compartidos de archivos) y, asimismo, se pueden agrupar para disponer de tolerancia a errores en los datos de usuario.

###  <a name="group-policy"></a><a name="GroupPolicy"></a> Directiva de grupo
 Si tiene equipos con Windows 7 en el entorno, se recomienda lo siguiente:

- Usar la directiva de grupo para controlar las directivas de contraseña para todos los equipos unidos al dominio que usen Carpetas de trabajo.

- Use la pantalla de bloqueo automática de carpetas de trabajo **y requiera una directiva de contraseñas** en los equipos que no estén Unidos a su dominio.

  La directiva de grupo también se puede usar para especificar un servidor de Carpetas de trabajo en equipos unidos a dominios. Esto simplifica en cierto modo la configuración de Carpetas de trabajo; de otro modo, los usuarios tendrían que indicar su dirección de correo electrónico del trabajo para buscar la configuración (siempre y cuando Carpetas de trabajo se haya configurado correctamente), o bien indicar la dirección URL de Carpetas de trabajo que se les haya hecho llegar explícitamente por correo electrónico o por cualquier otro medio de comunicación.

  La directiva de grupo también puede servir para configurar Carpetas de trabajo forzosamente de manera individual por cada usuario o equipo, pese a que esto hace que Carpetas de trabajo se sincronice en todos los equipos en los que un usuario inicie sesión (si se usa la configuración de directiva por usuario) e impide que los usuarios establezcan otra ubicación en su PC para Carpetas de trabajo (como una tarjeta microSD, a fin de ahorrar espacio en la unidad principal). Aconsejamos evaluar detenidamente las necesidades de los usuarios antes de implantar la configuración automática.

### <a name="windows-intune"></a>Windows Intune
 Windows Intune aporta un nivel de seguridad y facilidad de administración para los dispositivos no unidos a dominios que de otra forma no estarían presentes. Puede usar Windows Intune para configurar y administrar dispositivos personales de los usuarios, como tabletas que se conectan a carpetas de trabajo desde Internet. Windows Intune puede proporcionar dispositivos con la dirección URL del servidor de sincronización que se va a usar; de lo contrario, los usuarios deben escribir su dirección de correo electrónico del trabajo para buscar la configuración (si publica una dirección URL de carpetas de trabajo pública con el formato https://workfolders .<em> contoso.com</em>) o escriba la dirección URL del servidor de sincronización directamente.

 Sin una implementación de Windows Intune, los usuarios deben configurar los dispositivos externos manualmente, lo que puede dar lugar a una mayor demanda del personal del Departamento de soporte técnico de un cliente.

 Windows Intune también puede servir para borrar los datos de Carpetas de trabajo de forma selectiva del dispositivo de un usuario sin que ello afecte al resto de datos, algo que resulta especialmente útil si alguien deja la empresa o si un dispositivo se sustrae.

### <a name="web-application-proxyazure-ad-application-proxy"></a>Proxy de aplicación web/Proxy de aplicación de Azure AD
 Carpetas de trabajo se basa en el concepto de permitir que los dispositivos conectados a Internet recuperen datos empresariales de forma segura desde la red interna, lo que permite a los usuarios "tomar sus datos con ellos" en sus tabletas y dispositivos que normalmente no podrían tener acceso a los archivos de trabajo. Para lograrlo, se debe usar un proxy inverso para publicar direcciones URL de servidor de sincronización y ponerlas a disposición de los clientes de Internet.

Carpetas de trabajo admite el uso de proxy de aplicación Web, Azure AD proxy de aplicación o soluciones de proxy inverso de terceros:

-  Proxy de aplicación web es una solución de proxy inverso local. Para obtener más información, vea [proxy de aplicación web en Windows Server 2016](../../remote/remote-access/web-application-proxy/web-application-proxy-windows-server.md).

-  Azure AD proxy de aplicación es una solución de proxy inverso en la nube. Para obtener más información, consulte [cómo proporcionar acceso remoto seguro a aplicaciones locales](/azure/active-directory/active-directory-application-proxy-get-started) .

## <a name="additional-design-considerations"></a>Otras consideraciones de diseño
 Aparte de conocer cada uno de los componentes anteriores, los clientes deben dedicar tiempo a pensar en el número de servidores y recursos de sincronización que debe haber y, asimismo, si conviene usar clústeres de conmutación por error para que exista tolerancia a errores en estos servidores de sincronización.

### <a name="number-of-sync-servers"></a>Número de servidores de sincronización
 Un cliente puede poner en marcha varios servidores de sincronización en un solo entorno. Esta configuración puede ser muy adecuada por diversos motivos:

- Dispersión geográfica de los usuarios: por ejemplo, servidores de archivos de sucursales o centros de datos regionales.

- Requisitos de almacenamiento de datos: puede que algunos departamentos empresariales presenten requisitos de tratamiento o almacenamiento de los datos que sean más fáciles de cubrir con un servidor dedicado.

- Equilibrio de carga: en entornos de gran tamaño, el rendimiento y el tiempo de actividad de los servidores pueden aumentar si los datos se almacenan en varios servidores.

  Para obtener información sobre el rendimiento y la escala de los servidores de Carpetas de trabajo, vea [Consideraciones de rendimiento de las implementaciones de Carpetas de trabajo](../../remote/remote-access/web-application-proxy/web-application-proxy-windows-server.md).

> [!NOTE]
>  Cuando se usen varios servidores de sincronización, recomendamos configurar la detección automática de servidores para los usuarios. Este proceso se basa en la configuración de un atributo de cada cuenta de usuario en AD DS. El atributo se denomina **MSDS-SyncServerURL** y está disponible en las cuentas de usuario después de agregar un controlador de dominio de Windows Server 2012 R2 al dominio o de aplicar las actualizaciones del esquema Active Directory. Este atributo debe definirse en cada usuario si se quiere garantizar que los usuarios se conecten al servidor de sincronización adecuado. Mediante el uso de la detección automática de servidores, las organizaciones pueden publicar carpetas de trabajo detrás de una dirección URL "descriptiva" como *https://workfolders.contoso.com* , independientemente del número de servidores de sincronización en funcionamiento.

### <a name="number-of-sync-shares"></a>Número de recursos compartidos de sincronización
 Los servidores de sincronización individuales pueden mantener varios recursos compartidos de sincronización, lo que puede ser práctico por los motivos siguientes:

-   Requisitos de auditoría y seguridad: si los datos que un determinado departamento utiliza se deben auditar o retener de manera más controlada y prolongada, tener recursos compartidos de sincronización independientes ayuda a los administradores a mantener por separado las carpetas de usuario con distintos niveles de auditoría.

-   Filtros de archivos o cuotas diferentes: disponer de recursos compartidos por separado puede ser de ayuda si quiere establecer distintos límites o cuotas de almacenamiento para permitir tipos de archivo en Carpetas de trabajo (filtros de archivos) para diversos grupos o usuarios.

-   Control por departamentos: si las obligaciones administrativas están repartidas por departamentos, el uso de recursos compartidos separados en cada departamento ayuda a los administradores a imponer cuotas y otras directivas.

-   Directivas de dispositivo divergentes: el uso de múltiples recursos compartidos hace posible que una organización pueda mantener varias directivas de dispositivo (como el cifrado de Carpetas de trabajo) para distintos grupos o usuarios.

-   Capacidad de almacenamiento: si un servidor de archivos tiene varios volúmenes, se pueden usar recursos compartidos extra con los que sacar partido de esos volúmenes adicionales. Un recurso compartido concreto tiene acceso únicamente al volumen en el que está hospedado y no podrá usar ningún otro volumen de un servidor de archivos.

#### <a name="access-to-sync-shares"></a>Acceso a recursos compartidos de sincronización

Del mismo modo que el servidor de sincronización al que un usuario tiene acceso viene determinado por la dirección URL especificada en el cliente (o la dirección URL publicada para dicho usuario en AD DS si se usa la detección automática de servidores), el acceso a recursos compartidos de sincronización individuales viene determinado por los permisos existentes en el recurso compartido en cuestión.

En consecuencia, si un cliente hospeda varios recursos compartidos de sincronización en el mismo servidor, deberá tener cuidado y asegurarse de que cada usuario tenga permiso de acceso a únicamente uno de esos recursos compartidos. En caso contrario, cuando los usuarios se conecten al servidor, puede existir la posibilidad de que sus clientes se conecten al recurso compartido equivocado. Para evitarlo, puede crear un grupo de seguridad independiente por cada recurso compartido de sincronización.

Además, el acceso a la carpeta de un usuario individual dentro de un recurso compartido de sincronización viene determinado por los derechos de propiedad de la carpeta. Al crear un recurso compartido de sincronización, Carpetas de trabajo concede a los usuarios acceso exclusivo a sus archivos de forma predeterminada (la herencia se deshabilita y tales usuarios pasan a ser los propietarios de sus carpetas individuales).

## <a name="design-checklist"></a>Lista de comprobación de diseño

La siguiente relación de preguntas está pensada para ayudar a los clientes a diseñar la mejor implementación de Carpetas de trabajo para sus entornos. Conviene que los clientes se detengan a analizar esta lista de comprobación antes de intentar implementar servidores.

-   Usuarios objetivo

    -   ¿Qué usuarios van a usar Carpetas de trabajo?

    -   ¿Cómo están organizados los usuarios? (Geográficamente, por oficina, por departamento, etc.)

    -   ¿Hay usuarios que tengan requisitos especiales de almacenamiento, seguridad o retención de datos?

    -   ¿Hay usuarios que tengan requisitos específicos de directiva de dispositivo, como el cifrado?

    -   ¿Para qué equipos y dispositivos cliente necesita compatibilidad? (Windows 8.1, Windows RT 8.1, Windows 7)

         Si es compatible con equipos con Windows 7 y desea usar directivas de contraseñas, excluya el dominio que almacena sus cuentas de equipo de la Directiva de contraseñas de carpetas de trabajo y, en su lugar, use directiva de grupo directivas de contraseña para equipos Unidos a un dominio en ese dominio.

    -   ¿Necesita migrar desde otras soluciones de administración de datos de usuario (como Redirección de carpetas) o interoperar con ellas?

    -   ¿Es necesario que usuarios de varios dominios puedan sincronizarse por Internet con un único servidor?

    -   ¿Es necesario admitir usuarios que no sean miembros del grupo Administradores local en sus equipos unidos a dominio? (Si así es, deberá excluir los dominios en cuestión de las directivas de dispositivo de Carpetas de trabajo, como las directivas de contraseña y cifrado).

-   Planeación de la infraestructura y la capacidad

    -   ¿En qué sitios de la red deben estar los servidores de sincronización?

    -   ¿Alguno de los servidores de sincronización va a estar hospedado por un proveedor de IaaS (infraestructura como servicio), como una VM de Azure?

    -   ¿Va a necesitar servidores dedicados para grupos de usuarios específicos? De ser así, ¿cuántos usuarios por cada servidor dedicado?

    -   ¿Dónde están los puntos de entrada/salida de Internet en la red?

    -   ¿Se van a agrupar los servidores de sincronización para la tolerancia a errores?

    -   ¿Deben los servidores de sincronización mantener varios volúmenes de datos para hospedar datos de usuario?

-   Seguridad de los datos

    -   ¿Necesita crear varios recursos compartidos de sincronización en cualquiera de los servidores de sincronización?

    -   ¿Qué grupos se van a usar para dar acceso a los recursos compartidos de sincronización?

    -   Si usa varios servidores de sincronización, ¿qué grupo de seguridad va a crear para la capacidad delegada de modificar la propiedad msDS-SyncServerURL de los objetos de usuario?

    -   ¿Existen requisitos especiales de auditoría o seguridad en algún recurso compartido de sincronización concreto?

    -   ¿Va a necesitar la autenticación multifactor (MFA)?

    -   ¿Necesita poder borrar de forma remota los datos de Carpetas de trabajo de equipos y dispositivos?

-   Acceso de dispositivo

    -   ¿Qué dirección URL se va a usar para dar acceso a dispositivos basados en Internet (*la dirección URL predeterminada que se necesita para la detección automática de servidores basada en correo electrónico es workfolders.nombreDeDominio*)?

    -   ¿De qué manera se va a publicar la dirección URL en Internet?

    -   ¿Va a utilizar la detección automática de servidores?

    -   ¿Va a utilizar la directiva de grupo para configurar equipos unidos a dominio?

    -   ¿Va a utilizar Windows Intune para configurar dispositivos externos?

    -   ¿Será necesario el registro de dispositivos para que los dispositivos puedan conectarse?

## <a name="next-steps"></a>Pasos siguientes
 Después de diseñar la implementación de carpetas de trabajo, es el momento de implementar carpetas de trabajo. Para obtener más información, vea [Implementar Carpetas de trabajo](deploy-work-folders.md).

## <a name="additional-references"></a>Referencias adicionales
 Para obtener más información relacionada, vea los siguientes recursos.

|Tipo de contenido|Referencias|
|------------------|----------------|
|**Evaluación del producto**|-   [Carpetas de trabajo](work-folders-overview.md)<br />-   [Carpetas de trabajo para Windows 7](https://techcommunity.microsoft.com/t5/storage-at-microsoft/bg-p/FileCAB) (entrada de blog)|
|**Implementación**|-   [Diseñar una implementación de carpetas de trabajo](plan-work-folders.md)<br />-   [Implementar carpetas de trabajo](deploy-work-folders.md)<br />-   [Implementación de carpetas de trabajo con AD FS y proxy de aplicación web (WAP)](deploy-work-folders-adfs-overview.md)<br />- [Implementación de carpetas de trabajo con Azure AD proxy de aplicación](https://techcommunity.microsoft.com/t5/storage-at-microsoft/bg-p/FileCAB)<br />-   [Consideraciones de rendimiento para las implementaciones de carpetas de trabajo](../../remote/remote-access/web-application-proxy/web-application-proxy-windows-server.md)<br />-   [Carpetas de trabajo para Windows 7 (descarga de 64 bits)](https://www.microsoft.com/download/details.aspx?id=42558)<br />-   [Carpetas de trabajo para Windows 7 (descarga de 32 bits)](https://www.microsoft.com/download/details.aspx?id=42559)<br />-   [Implementación del laboratorio de pruebas de carpetas de trabajo](https://techcommunity.microsoft.com/t5/storage-at-microsoft/bg-p/FileCAB) (entrada de blog)|
