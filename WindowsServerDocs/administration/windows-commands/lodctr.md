---
title: lodctr
description: Artículo de referencia del comando LODCTR, que permite registrar o guardar la configuración del registro y el nombre del contador de rendimiento en un archivo y designar servicios de confianza.
ms.topic: reference
ms.assetid: 5a849abd-6b31-4833-bc8a-306c05eca29a
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 61b449678fae62e0909d19b8cae8411102898bd8
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89037883"
---
# <a name="lodctr"></a>lodctr

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Permite registrar o guardar la configuración del registro y el nombre del contador de rendimiento en un archivo y designar los servicios de confianza.

## <a name="syntax"></a>Sintaxis

```
lodctr <filename> [/s:<filename>] [/r:<filename>] [/t:<servicename>]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<filename>` | Especifica el nombre del archivo de inicialización que registra la configuración del nombre del contador de rendimiento y el texto explicativo. |
| modificado`<filename>` | Especifica el nombre del archivo en el que se guardan la configuración del registro del contador de rendimiento y el texto explicativo. |
| /r | Restaura la configuración del registro de contadores y el texto explicativo de la configuración actual del registro y los archivos de rendimiento almacenados en caché relacionados con el registro. |
| /r`<filename>` | Especifica el nombre del archivo que restaura los valores del registro del contador de rendimiento y el texto explicativo.<p>**ADVERTENCIA:** Si usa este comando, sobrescribirá todos los valores del registro de contadores de rendimiento y el texto explicativo y los reemplazará por la configuración definida en el archivo especificado. |
| /t:`<servicename>` | Indica que el servicio `<servicename>` es de confianza. |
| /? | Muestra la ayuda en el símbolo del sistema. |

#### <a name="remarks"></a>Observaciones

- Si la información proporcionada contiene espacios, utilice comillas alrededor del texto (por ejemplo, "nombre de archivo 1").

### <a name="examples"></a>Ejemplos

Para guardar la configuración del registro de rendimiento actual y el texto explicativo en el archivo *"perf backup1.txt"*, escriba:

```
lodctr /s:"perf backup1.txt"
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
