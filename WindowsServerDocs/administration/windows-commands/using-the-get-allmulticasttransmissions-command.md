---
title: Get-AllMulticastTransmissions
description: Artículo de referencia de Get-AllMulticastTransmissions, que muestra información sobre todas las transmisiones de multidifusión en un servidor.
ms.topic: reference
ms.assetid: 95b8fb79-7a8a-4f0c-88f4-92bc1111c67f
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: c0c7c4e77c2ad23fab864839cde03ed4f4806c80
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89035963"
---
# <a name="get-allmulticasttransmissions"></a>Get-AllMulticastTransmissions

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Muestra información acerca de todas las transmisiones de multidifusión en un servidor.

## <a name="syntax"></a>Sintaxis
para Windows Server 2008:
```
wdsutil /Get-AllMulticastTransmissions [/Server:<Server name>] [/Show:Clients] [/ExcludedeletePending]
```
para Windows Server 2008 R2:
```
wdsutil /Get-AllMulticastTransmissions [/Server:<Server name>] [/Show:{Boot | Install | All}] [/details:Clients]  [/ExcludedeletePending]
```
### <a name="parameters"></a>Parámetros

|        Parámetro        |                                                                                                                                                                                                                                                                   Explicación                                                                                                                                                                                                                                                                    |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [/Server:<Server name>] |                                                                                                                                                                                 Especifica el nombre del servidor. Puede ser el nombre de NetBIOS o el nombre de dominio completo (FQDN). Si no se especifica ningún nombre de servidor, se utilizará el servidor local.                                                                                                                                                                                  |
|         /Show         | **Windows Server 2008**<p>/Show: clients: muestra información acerca de los equipos cliente que están conectados a las transmisiones de multidifusión.<p>**Windows Server 2008 R2**<p>Mostrar: {arranque &#124; instalar &#124; todos}-el tipo de imagen que se va a devolver.                                El **arranque** solo devuelve transmisiones de imagen de arranque.                                  La **instalación** solo devuelve transmisiones de imagen de instalación. **All** devuelve ambos tipos de imagen. |
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|    /Details: clientes     |                                                                                                                                                                                              Solo se admite para Windows Server 2008 R2. Si está presente, se mostrarán los clientes que están conectados a la transmisión.                                                                                                                                                                                               |
| [/ExcludedeletePending] |                                                                                                                                                                                                                                              Excluye cualquier transmisión desactivada de la lista.                                                                                                                                                                                                                                               |

## <a name="examples"></a>Ejemplos
Para ver información acerca de todas las transmisiones, escriba:
- Windows Server 2008: `wdsutil /Get-AllMulticastTransmissions`
- Windows Server 2008 R2: `wdsutil /Get-AllMulticastTransmissions /Show:All` para ver información acerca de todas las transmisiones excepto las transmisiones desactivadas, escriba:
- Windows Server 2008: `wdsutil /Get-AllMulticastTransmissions /Server:MyWDSServer /Show:Clients /ExcludedeletePending`
- Windows Server 2008 R2: `wdsutil /Get-AllMulticastTransmissions /Server:MyWDSServer /Show:All /details:Clients /ExcludedeletePending`
  ## <a name="additional-references"></a>Referencias adicionales
  - Clave de sintaxis [de línea de comandos](command-line-syntax-key.md) 
   [Usar el comando](using-the-get-multicasttransmission-command.md) 
   Get-MulticastTransmission [Usar el comando](using-the-new-multicasttransmission-command.md) 
   New-MulticastTransmission [Usar el comando](using-the-remove-multicasttransmission-command.md) 
   Remove-MulticastTransmission [Subcomando: Start-MulticastTransmission](subcommand-start-multicasttransmission.md)
