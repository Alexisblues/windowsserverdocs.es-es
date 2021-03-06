---
title: Subcomando Start-Server
description: Artículo de referencia para el subcomando Start-Server, que inicia todos los servicios de un servidor de servicios de implementación de Windows.
ms.topic: reference
ms.assetid: 1e4343e2-0a16-4e65-8769-c09adaef5680
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 4d79ef2689f15a0f6fdc67cf5c068372f6f448c7
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89024749"
---
# <a name="subcommand-start-server"></a>Subcomando: Start-Server

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Inicia todos los servicios de un servidor de servicios de implementación de Windows.

## <a name="syntax"></a>Sintaxis
```
wdsutil [Options] /start-Server [/Server:<Server name>]
```
### <a name="parameters"></a>Parámetros
|Parámetro|Descripción|
|-------|--------|
|[/Server:<Server name>]|Especifica el nombre del servidor que se va a iniciar. Puede ser el nombre de NetBIOS o el nombre de dominio completo (FQDN). Si no se especifica ningún nombre de servidor, se utilizará el servidor local.|
## <a name="examples"></a>Ejemplos
Para iniciar el servidor, escriba uno de los siguientes:
```
wdsutil /start-Server
wdsutil /verbose /start-Server /Server:MyWDSServer
```
## <a name="additional-references"></a>Referencias adicionales
- Clave de sintaxis [de línea de comandos](command-line-syntax-key.md) 
 [Usar el comando](using-the-disable-server-command.md) 
 Disable-Server [Usar el comando](using-the-enable-server-command.md) 
 enable-Server [Usar el comando](using-the-get-server-command.md) 
 Get-Server [Usar el comando](using-the-initialize-server-command.md) 
 Initialize-Server [Subcomando: set-Server](subcommand-set-server.md) 
 [Subcomando: Stop-Server](subcommand-stop-server.md) 
 [La opción UnInitialize-Server](the-uninitialize-server-option.md)
