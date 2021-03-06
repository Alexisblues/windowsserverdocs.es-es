---
title: Remove-DriverGroupPackage
description: Artículo de referencia de Remove-DriverGroupPackage, que quita un paquete de controladores de un grupo de controladores en un servidor.
ms.topic: reference
ms.assetid: 2e48616d-d6a4-45f0-a5c6-efe62bf6a0ed
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: e71482859adb9cb9a0f4f848a41c7f526f54fc91
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89023239"
---
# <a name="remove-drivergrouppackage"></a>Remove-DriverGroupPackage



Quita un paquete de controladores de un grupo de controladores de un servidor.

## <a name="syntax"></a>Sintaxis

```
WDSUTIL /Remove-DriverGroupPackage /DriverGroup:<Group Name> [/Server:<Server Name>] {/DriverPackage:<Name> | /PackageId:<ID>}
```

### <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|---------|-----------|
|[/Server:\<Server name>]|Especifica el nombre del servidor. Puede ser el nombre NetBIOS o el FQDN. Si no se especifica un nombre de servidor, se utiliza el servidor local.|
|[/DriverPackage: \<Name> ]|Especifica el nombre del paquete de controladores que se va a quitar.|
|[/PackageId: \<ID> ]|Especifica el ID. de servicios de implementación de Windows del paquete de controladores que se va a quitar. Debe especificar esta opción si el paquete de controladores no se puede identificar de forma única por nombre.|

## <a name="examples"></a>Ejemplos

```
WDSUTIL /Remove-DriverGroupPackage /DriverGroup:PrinterDrivers /PackageId:{4D36E972-E325-11CE-BFC1-08002BE10318}
```
```
WDSUTIL /Remove-DriverGroupPackage /DriverGroup:PrinterDrivers /DriverPackage:XYZ
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)