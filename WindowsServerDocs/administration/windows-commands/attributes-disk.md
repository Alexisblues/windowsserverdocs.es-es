---
title: attributes disk
description: Artículo de referencia para el comando de disco Attributes, que muestra, establece o borra los atributos de un disco.
ms.topic: reference
ms.assetid: eed57071-c1c6-4394-9542-62b52a878c92
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 72b4a99c36085062441a7a8751a065dad1dd0c51
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89029203"
---
# <a name="attributes-disk"></a>attributes disk

Muestra, establece o borra los atributos de un disco. Cuando este comando se usa para mostrar los atributos actuales de un disco, el atributo disco de inicio denota el disco que se usa para iniciar el equipo. En el caso de una réplica dinámica, muestra el disco que contiene el Plex de arranque del volumen de arranque.

> [!IMPORTANT]
> Se debe seleccionar un disco para que el comando de **disco de atributos** se ejecute correctamente. Use el comando **Seleccionar disco** para seleccionar un disco y desplazar el foco a él.

## <a name="syntax"></a>Sintaxis

```
attributes disk [{set | clear}] [readonly] [noerr]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| set | Establece el atributo especificado del disco con el foco. |
| clear | Borra el atributo especificado del disco que tiene el foco. |
| readonly | Especifica que el disco es de solo lectura. |
| noerr | Sólo para scripting. Cuando se detecta un error, DiskPart sigue procesando los comandos como si no hubiera ningún error. Sin este parámetro, un error hace que DiskPart salga con un código de error. |

## <a name="examples"></a>Ejemplos

Para ver los atributos del disco seleccionado, escriba:

```
attributes disk
```

Para establecer el disco seleccionado como de solo lectura, escriba:

```
attributes disk set readonly
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [Seleccionar disco (comando)](select-disk.md)
