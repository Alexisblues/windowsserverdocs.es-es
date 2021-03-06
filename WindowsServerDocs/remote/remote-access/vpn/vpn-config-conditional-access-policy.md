---
title: Configurar la directiva de acceso condicional
description: Una vez creado un certificado raíz, la ' conectividad VPN ' desencadena la creación de la aplicación de nube ' servidor VPN ' en el inquilino del cliente.
ms.topic: article
ms.date: 05/25/2018
ms.author: v-tea
author: Teresa-MOTIV
ms.localizationpriority: medium
ms.reviewer: deverette
ms.openlocfilehash: 7535de9f11a8daf38ad1aab2fe95a620f9682025
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87946708"
---
# <a name="step-73-configure-the-conditional-access-policy"></a>Paso 7.3. Configurar la directiva de acceso condicional

>Se aplica a: Windows Server (canal semianual), Windows Server 2016, Windows Server 2012 R2, Windows 10

- [**Anterior:** Paso 7,2. Crear certificados raíz para la autenticación VPN con Azure AD](vpn-create-root-cert-for-vpn-auth-azure-ad.md)
- [**Siguiente:** Paso 7,4. Implementar certificados raíz de acceso condicional en AD local](vpn-deploy-cond-access-root-cert-to-on-premise-ad.md)

En este paso, configurará la Directiva de acceso condicional para la conectividad VPN. Cuando el primer certificado raíz se crea en la hoja "Conectividad VPN", crea automáticamente una aplicación en la nube "servidor VPN" en el inquilino.

Cree una directiva de acceso condicional que esté asignada al grupo de usuarios de VPN y el ámbito de la **aplicación de nube** al **servidor VPN**:

- **Usuarios**: usuarios de VPN
- **Aplicación en la nube**: servidor VPN
- **Grant (control de acceso)**: "requerir multi-factor Authentication". Si lo desea, se pueden usar otros controles.

**Procedimiento:** En este paso se describe la creación de la Directiva de acceso condicional más básica.Si lo desea, se pueden usar condiciones y controles adicionales.


1. En la página **acceso condicional** , en la barra de herramientas de la parte superior, seleccione **Agregar**.

    ![Seleccione Agregar en la página de acceso condicional](../../media/Always-On-Vpn/07.png)

2. En la página **nuevo** , en el cuadro **nombre** , escriba un nombre para la Directiva. Por ejemplo, escriba **Directiva de VPN**.

    ![Agregar el nombre de la directiva en la página de acceso condicional](../../media/Always-On-Vpn/08.png)

3. En la sección **asignación** , seleccione **usuarios y grupos**.

    ![Seleccionar Usuarios y grupos](../../media/Always-On-Vpn/09.png)

4. En la página **Usuarios y grupos**, siga estos pasos:

    ![Seleccionar un usuario de prueba](../../media/Always-On-Vpn/10.png)

    a. Seleccione **Seleccionar usuarios y grupos**.

    b. Elija **Seleccionar**.

    c. En la página **seleccionar** , seleccione el grupo **usuarios de VPN** y, a continuación, seleccione **seleccionar**.

    d. En la página **usuarios y grupos** , seleccione **listo**.

5. En la página **Nuevo**, realice los pasos siguientes:

    ![Seleccionar aplicaciones en la nube](../../media/Always-On-Vpn/11.png)

    a. En la sección **asignaciones** , seleccione aplicaciones en la **nube**.

    b. En la página aplicaciones en la **nube** , seleccione **seleccionar aplicaciones**.

    d. Seleccione **Servidor VPN**.

6.  En la página **nuevo** , para abrir la página **conceder** , en la sección **controles** , seleccione **conceder**.

    ![Seleccionar Conceder](../../media/Always-On-Vpn/13.png)

7.  En la página **Conceder**, siga estos pasos:

    ![Seleccionar Requerir autenticación multifactor](../../media/Always-On-Vpn/14.png)

    a. Seleccione **Requerir autenticación multifactor**.

    b. Elija **Seleccionar**.

8.  En la página **nuevo** , en **Habilitar Directiva**, seleccione **activado**.

    ![Habilitar directiva](../../media/Always-On-Vpn/15.png)

9.  En la página **nuevo** , seleccione **crear**.


## <a name="next-steps"></a>Pasos siguientes
[Paso 7,4. Implementar certificados raíz de acceso condicional en AD local](vpn-deploy-cond-access-root-cert-to-on-premise-ad.md): en este paso, implementará el certificado raíz de acceso condicional como certificado raíz de confianza para la autenticación de VPN en su instancia local de ad.
