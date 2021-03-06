---
title: select partition
description: Artículo de referencia de * * * *-
ms.topic: reference
ms.assetid: 25f70083-b8f7-4a8e-9b34-4b3ffbe06670
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 816a235f7ba83320828a5dc72c9f2558c27b2ed8
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89027913"
---
# <a name="select-partition"></a>select partition

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

selecciona la partición especificada y desplaza el foco a ella. Este comando también se puede usar para mostrar la partición que tiene actualmente el foco en el disco seleccionado.



## <a name="syntax"></a>Sintaxis

```
select partition=<n>
```

### <a name="parameters"></a>Parámetros

|   Parámetro    |                                                                                    Descripción                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| divide\=<n> | Número de la partición que va a recibir el foco. Puede ver los números de todas las particiones del disco seleccionado actualmente mediante el comando **List Partition** en Diskpart. |

## <a name="remarks"></a>Observaciones

-   Antes de poder seleccionar una partición, primero debe seleccionar un disco con el comando **Seleccionar disco** .

-   Si no se especifica ningún número de partición, este comando muestra la partición que tiene actualmente el foco en el disco seleccionado.

-   Si se selecciona un volumen con una partición correspondiente, la partición se seleccionará automáticamente.

-   Si se selecciona una partición con un volumen correspondiente, el volumen se seleccionará automáticamente.

## <a name="examples"></a>Ejemplos
Para desplazar el foco a la partición 3, escriba:

```
select partitition=3
```

Para mostrar la partición que tiene actualmente el foco en el disco seleccionado, escriba:

```
select partition
```

## <a name="additional-references"></a>Referencias adicionales
- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)




