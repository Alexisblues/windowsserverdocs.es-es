---
title: mask
description: Artículo de referencia del comando Mask, que quita las instantáneas de hardware que se importaron mediante el comando IMPORT.
ms.topic: reference
ms.assetid: bf301474-d74a-44e7-9fad-c8a11e7ca3bd
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: c5d8f86de3019e47da3aff56aa370972de3288fa
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89037873"
---
# <a name="mask"></a>mask

Quita las instantáneas de hardware que se importaron mediante el comando de **importación** .

## <a name="syntax"></a>Sintaxis

```
mask <shadowsetID>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| shadowsetID | Quita las instantáneas que pertenecen al identificador de conjunto de instantáneas especificado. |

#### <a name="remarks"></a>Observaciones

- Puede usar un alias existente o una variable de entorno en lugar de *ShadowSetID*. Use **Agregar** sin parámetros para ver los alias existentes.

### <a name="examples"></a>Ejemplos

Para quitar la instantánea importada *% Import_1%*, escriba:

```
mask %Import_1%
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)