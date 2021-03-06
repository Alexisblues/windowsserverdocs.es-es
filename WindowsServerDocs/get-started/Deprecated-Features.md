---
title: Características eliminadas o en desuso en Windows Server 2016
description: Una lista de las características y funcionalidades de Windows Server 2016 que se quitaron del producto en la versión actual o cuya eliminación se planea para las siguientes versiones (en desuso). Este artículo está orientado a profesionales de TI que actualizan sus sistemas operativos en un entorno comercial.
ms.topic: article
ms.date: 08/22/2019
ms.assetid: 5d10c5f9-ebac-49a0-b808-c0b1702e0437
author: jasongerend
ms.author: jgerend
manager: dougkim
ms.localizationpriority: medium
ms.openlocfilehash: baa5b19eb20c0ac46c8b1f5d94e2ad56ee6d3288
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87959873"
---
# <a name="features-removed-or-deprecated-in--windows-server-2016"></a>Características eliminadas o en desuso en Windows Server 2016

>Se aplica a: Windows Server 2016

A continuación se enumeran las características y funcionalidades de Windows Server 2016 que se quitaron del producto en la versión actual o cuya eliminación se planea para las siguientes versiones (en desuso). Este artículo está orientado a profesionales de TI que actualizan sus sistemas operativos en un entorno comercial. Esta lista está sujeta a cambios en versiones posteriores y es posible que no incluya todas las características o funcionalidades desusadas. Para obtener más detalles sobre una característica o funcionalidad en concreto y su reemplazo, consulte la documentación relativa a la característica en cuestión.

> [!TIP]
> Para más información sobre qué se ha quitado o ha quedado en desuso en las versiones más recientes, consulta [Características eliminadas o cuyo reemplazo está planeado en Windows Server](../get-started-19/removed-features.md).

## <a name="features-removed-from-windows-server-2016"></a>Características quitadas de Windows Server 2016

Las siguientes características y funcionalidades se quitaron de esta versión de Windows Server 2016. Las aplicaciones, el código o el uso que dependen de estas características no funcionarán en esta versión, a menos que se emplee un método alternativo.

> [!NOTE]
> Si va a pasar a Windows Server 2016 desde una versión de servidor anterior a Windows Server 2012 R2 o Windows Server 2012, también debe consultar [Características quitadas o desusadas en Windows Server 2012 R2](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn303411(v=ws.11)) y [Características o funcionalidades desusadas en Windows Server 2012](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831568(v=ws.11)).

### <a name="share-and-storage-management"></a>Administración de almacenamiento y recursos compartidos

El complemento de administración de almacenamiento y recursos compartidos para Microsoft Management Console se ha quitado. En su lugar, lleve a cabo cualquiera de las siguientes acciones:

-   Si el equipo que desea administrar está ejecutando un sistema operativo anterior a Windows Server 2016, conéctese a él con Escritorio remoto y use la versión local del complemento de administración de almacenamiento y recursos compartidos.

-   En un equipo que ejecuta Windows 8.1 o versiones anteriores, utilice el complemento de administración de almacenamiento y recursos compartidos desde RSAT para ver el equipo que quiere administrar.

-   Utilice Hyper-V en un equipo cliente para ejecutar una máquina virtual con Windows 7, Windows 8 o Windows 8.1 con el complemento de administración de almacenamiento y recursos compartidos de RSAT.

### <a name="journaldll"></a>Journal.dll

El archivo Journal.dll se ha suprimido en Windows Server 2016. No hay sustitución.

### <a name="security-configuration-wizard"></a>Asistente para configuración de seguridad

El Asistente para configuración de seguridad se ha quitado. En su lugar, se protegen las características de forma predeterminada. Si necesita controlar la configuración de seguridad específica, puede usar una directiva de grupo o el [Administrador de cumplimiento de normas de seguridad de Microsoft](/previous-versions/tn-archive/cc936627(v=technet.10)).

### <a name="sqm"></a>SQM

Se han quitado los componentes de participación que administran la participación en el Programa para la mejora de la experiencia del usuario.

### <a name="windows-update"></a>Windows Update

Se ha quitado el comando **wuauclt.exe /detectnow** y ya no se admite. Para desencadenar una búsqueda de actualizaciones, sigue una de las acciones a continuación:

- Ejecuta estos comandos de PowerShell:
    ````powershell
    $AutoUpdates = New-Object -ComObject "Microsoft.Update.AutoUpdate"
    $AutoUpdates.DetectNow()
    ````

- Como alternativa, usa este VBScript:
    ````vb
    Set automaticUpdates = CreateObject("Microsoft.Update.AutoUpdate")
    automaticUpdates.DetectNow()
    ````

## <a name="features-deprecated-starting-with-windows-server-2016"></a>Características desusadas a partir de Windows Server 2016

Las siguientes características y funcionalidades quedarán en desuso a partir de esta versión. Con el tiempo, se quitarán completamente del producto, pero aún están disponibles en esta versión (en algunos casos, se les ha quitado cierta funcionalidad). Debe comenzar a planear el empleo de métodos alternativos para cualquier aplicación, código o uso que dependa de estas características.

### <a name="configuration-tools"></a>Herramientas de configuración

-   **Scregedit.exe** ha quedado en desuso. Si tiene scripts que dependen de Scregedit.exe, ajústelos para que utilicen los métodos Reg.exe o de Windows PowerShell.

-   **Sconfig.exe** ha quedado en desuso. En su lugar, utiliza [Sconfig. cmd](./sconfig-on-ws2016.md).

### <a name="netcfg-custom-apis"></a>API personalizadas de NetCfg

La instalación de PrintProvider, NetClient e ISDN mediante las API personalizadas de NetCfg está en desuso.

### <a name="remote-management"></a>Administración remota

WinRM.vbs está en desuso. En su lugar, utilice la funcionalidad del proveedor de WinRM de Windows PowerShell.

### <a name="smb"></a>SMB

SMB 2+ en NetBT está en desuso. En su lugar, implemente SMB sobre TCP o RDMA.
