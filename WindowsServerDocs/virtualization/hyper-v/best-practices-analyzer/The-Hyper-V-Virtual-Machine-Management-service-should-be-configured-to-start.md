---
title: El servicio de administración de máquinas virtuales de Hyper-V debe estar configurado para iniciarse automáticamente
description: Proporciona instrucciones para resolver el problema que informa esta regla de Analizador de procedimientos recomendados.
manager: dongill
ms.author: kathydav
ms.topic: article
ms.assetid: 222bbe76-c514-4a3f-b61b-860a4dc2826a
author: kbdazure
ms.date: 8/16/2016
ms.openlocfilehash: 73ef8f7de89da5a05fedd53b9b23a32fed683dbf
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87960488"
---
# <a name="the-hyper-v-virtual-machine-management-service-should-be-configured-to-start-automatically"></a>El servicio de administración de máquinas virtuales de Hyper-V debe estar configurado para iniciarse automáticamente

>Se aplica a: Windows Server 2016

Para más información acerca de los análisis y los procedimientos recomendados, vea [Analizador de procedimientos recomendados](https://go.microsoft.com/fwlink/?LinkId=122786).

|Propiedad|Detalles|
|-|-|
|**Sistema operativo**|Windows Server 2016|
|**Producto/Característica**|Hyper-V|
|**Gravedad**|Advertencia|
|**Categoría**|Configuración|

En las secciones siguientes, cursiva indica el texto de la interfaz de usuario que aparece en la herramienta de Analizador de procedimientos recomendados para este problema.

## <a name="issue"></a>Incidencia

*El servicio administración de máquinas virtuales de Hyper-V no está configurado para iniciarse automáticamente.*

## <a name="impact"></a>Impacto

*Las máquinas virtuales no se pueden administrar hasta que se inicie el servicio.*

Las máquinas virtuales que se están ejecutando seguirán ejecutándose. Sin embargo, no podrá administrar máquinas virtuales ni crearlas o eliminarlas hasta que se ejecute el servicio.

## <a name="resolution"></a>Resolución

*Use el complemento servicios o la herramienta de línea de comandos SC config para volver a configurar el servicio para que se inicie automáticamente.*

> [!TIP]
> Si no encuentra el servicio en la aplicación de escritorio o la herramienta de línea de comandos informa de que el servicio no existe, es probable que las herramientas de administración de Hyper-V no estén instaladas. Para instalarlos:
>
> - En Windows Server, abra Administrador del servidor y use el Asistente para agregar roles y características. Para obtener más información, vea [instalar el rol Hyper-V en Windows Server 2016](../get-started/Install-the-Hyper-V-role-on-Windows-Server.md).
> - En Windows, desde el escritorio, empiece a escribir **programas**, haga clic en **programas y características** (panel de control) > **activar o desactivar las características de Windows en**  >  herramientas de administración de Hyper **-v**  >  **Hyper-V Management Tools**. A continuación, haga clic en **Aceptar**.

#### <a name="to-reconfigure-the-service-to-start-automatically-using-the-services-desktop-app"></a>Para volver a configurar el servicio para que se inicie automáticamente con la aplicación de escritorio servicios

1.  Abra la aplicación de escritorio servicios. (Haga clic en **Inicio**, haga clic en el cuadro de búsqueda, empiece a escribir **servicios**y, a continuación, haga clic en servicios en la lista de resultados.

2.  En el panel de detalles, haga clic con el botón secundario en **Administración de máquinas virtuales de Hyper-V**y, a continuación, haga clic en **propiedades**.

3.  En la pestaña **General** , en tipo de **Inicio** , haga clic en **automático**.

#### <a name="to-reconfigure-the-service-to-start-automatically-using-the-sc-config-command"></a>Para volver a configurar el servicio para que se inicie automáticamente con el comando SC config

1.  Abra Windows PowerShell.

2.  Escriba:

    ```
    set-service  vmms -startuptype automatic
    ```

3.  Si el servicio no se está ejecutando, escriba:

    ```
    start-service -name vmms
    ```



