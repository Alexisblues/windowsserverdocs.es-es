---
title: Get-AllImageGroups
description: Artículo de referencia de Get-AllImageGroups, que recupera información sobre todos los grupos de imágenes de un servidor y todas las imágenes de esos grupos de imágenes.
ms.topic: reference
ms.assetid: 2ca06533-bcf5-4590-ac8e-263d6c9874f8
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: f472a1907e07e08ae646d9c454125dfb64ff54df
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89036013"
---
# <a name="get-allimagegroups"></a>Get-AllImageGroups

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Recupera información sobre todos los grupos de imágenes de un servidor y todas las imágenes de esos grupos de imágenes.

## <a name="syntax"></a>Sintaxis
```
wdsutil [Options] /Get-AllImageGroups [/Server:<Server name>] [/detailed]
```
### <a name="parameters"></a>Parámetros
|Parámetro|Descripción|
|-------|--------|
|[/Server:<Server name>]|Especifica el nombre del servidor. Puede ser el nombre de NetBIOS o el nombre de dominio completo (FQDN). Si no se especifica ningún nombre de servidor, se utilizará el servidor local.|
|[/detailed]|Devuelve los metadatos de la imagen de cada imagen. Si no se utiliza este parámetro, el comportamiento predeterminado es devolver solo el nombre de la imagen, la descripción y el nombre de archivo de cada imagen.|
## <a name="examples"></a>Ejemplos
Para ver información acerca de los grupos de imágenes, escriba uno de los siguientes:
```
wdsutil /Get-AllImageGroups
wdsutil /verbose /Get-AllImageGroups /Server:MyWDSServer /detailed
```
## <a name="additional-references"></a>Referencias adicionales
- Clave de sintaxis [de línea de comandos](command-line-syntax-key.md) 
 [Uso del comando](using-the-add-imagegroup-command.md) 
 Add-ImageGroup [Usar el comando](using-the-get-imagegroup-command.md) 
 Get-ImageGroup [Usar el comando](using-the-remove-imagegroup-command.md) 
 Remove-ImageGroup [Subcomando: set-ImageGroup](subcommand-set-imagegroup.md)
