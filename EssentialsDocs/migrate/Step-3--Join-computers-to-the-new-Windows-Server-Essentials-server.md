---
title: 'Paso 3: Unión de equipos al nuevo servidor de Windows Server Essentials'
description: Describe cómo usar Windows Server Essentials
ms.date: 10/03/2016
ms.topic: article
ms.assetid: a0e07d1a-8409-429b-87d7-0f4a7e14d668
author: nnamuhcs
ms.author: coreyp
manager: dongill
ms.openlocfilehash: 46de5b182a162563a81772bf489d8d182514d9d6
ms.sourcegitcommit: d99bc78524f1ca287b3e8fc06dba3c915a6e7a24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/27/2020
ms.locfileid: "87180471"
---
# <a name="step-3-join-computers-to-the-new-windows-server-essentials-server"></a>Paso 3: Unión de equipos al nuevo servidor de Windows Server Essentials

>Se aplica a: Windows Server 2016 Essentials, Windows Server 2012 R2 Essentials

El siguiente paso del proceso de migración consiste en conectar los equipos cliente al nuevo servidor que ejecuta Windows Server Essentials.

> [!NOTE]
>  Puede omitir este paso en los equipos con Windows XP o Windows Vista. El software del Conector de Windows Server no admite equipos que ejecuten Windows XP o Windows Vista.

 Para poder unir un equipo cliente al nuevo servidor de Windows Server Essentials, debe desconectarlo del servidor de origen desinstalando el software del conector de Windows Server en el equipo cliente.

### <a name="to-uninstall-windows-server-connector-on-a-client-computer"></a>Para desinstalar el Conector de Windows Server en un equipo cliente

1.  En un equipo cliente, abra el Panel de control y, a continuación, abra **Programas y características**.

2.  En la lista de programas, haga clic en la aplicación de conexión que se ejecuta en el equipo.

    > [!NOTE]
    >  La aplicación de conector puede ser el **conector de Windows Small Business Server 2011 Essentials**o el **conector de Windows Server Essentials**, dependiendo de la versión de Windows Server Essentials a la que se conectó el equipo cliente.

3.  Haga clic en **Desinstalar**.

### <a name="to-reconnect-a-client-computer-to-the-server"></a>Para volver a conectar un equipo cliente al servidor

1.  Inicie sesión en el equipo que desea conectar al servidor.

    > [!NOTE]
    >  Si el equipo tiene varias cuentas de usuario, inicie sesión en la que se encuentren los documentos, imágenes y preferencias personales que desee mantener después de conectar el equipo al servidor.

2.  Abra un explorador de Internet, como, por ejemplo, Internet Explorer.

3.  En la barra de direcciones, escriba **http://<ServerName \> /Connect**y, a continuación, presione Entrar.

4.  Siga las instrucciones en pantalla para unir el equipo cliente al nuevo servidor de Windows Server Essentials.

## <a name="next-steps"></a>Pasos siguientes
 Ha unido los equipos cliente al nuevo servidor que ejecuta Windows Server Essentials. Ahora, vaya a [paso 4: trasladar la configuración y los datos al servidor de destino para la migración a Windows Server Essentials](Step-4--Move-settings-and-data-to-the-Destination-Server-for-Windows-Server-Essentials-migration.md).


Para ver todos los pasos, vea [migrar a Windows Server Essentials](Migrate-from-Previous-Versions-to-Windows-Server-Essentials-or-Windows-Server-Essentials-Experience.md).

