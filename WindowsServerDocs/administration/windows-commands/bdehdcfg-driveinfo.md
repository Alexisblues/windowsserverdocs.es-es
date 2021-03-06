---
title: bdehdcfg driveinfo
description: Artículo de referencia para el comando bdehdcfg DriveInfo, que muestra la letra de unidad, el tamaño total, el espacio libre máximo y las características de la partición.
ms.topic: reference
ms.assetid: f2d065e7-eced-4509-a1a0-ee2521a7f02e
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 016733e2a10bd942b04a77af3d8e01577d4fff86
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89031563"
---
# <a name="bdehdcfg-driveinfo"></a>bdehdcfg: DriveInfo

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Muestra la letra de unidad, el tamaño total, el espacio libre máximo y las características de la partición. Solo se enumeran las particiones válidas. El espacio sin asignar no se enumera si ya existen cuatro particiones principales o extendidas.

>[!NOTE]
> Este comando es meramente informativo y no realiza ningún cambio en la unidad.

## <a name="syntax"></a>Sintaxis

```
bdehdcfg -driveinfo <drive_letter>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| <drive_letter> | Especifica una letra de unidad seguida de dos puntos. |

## <a name="example"></a>Ejemplo

Para mostrar la información de la unidad C:

```
bdehdcfg  driveinfo C:
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bdehdcfg](bdehdcfg.md)
