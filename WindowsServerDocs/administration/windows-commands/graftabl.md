---
title: graftabl
description: Artículo de referencia del comando Graftabl, que permite que los sistemas operativos Windows muestren un juego de caracteres extendido en el modo gráficos.
ms.topic: reference
ms.assetid: b08351d4-3d24-490c-86f6-1252da11d923
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 8b92cc0501b69127bb8dd9e3faba5591a48542ea
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89035493"
---
# <a name="graftabl"></a>graftabl

Permite que los sistemas operativos Windows muestren un juego de caracteres extendido en el modo gráficos. Si se utiliza sin parámetros, **Graftabl** muestra las páginas de códigos anterior y actual.

## <a name="syntax"></a>Sintaxis

```
graftabl <codepage>
graftabl /status
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<codepage>` | Especifica una página de códigos para definir el aspecto de los caracteres extendidos en el modo gráficos. Los números de identificación válidos de la página de códigos son:<ul><li>**437** -Estados Unidos</li><li>**850** -multilingüe (Latín I)</li><li>**852** -Eslava (Latín II)</li><li>**855** -cirílico (Ruso)</li><li>**857** -Turco</li><li>**860** -Portugués</li><li>**861** : Islandés</li><li>**863** -Canadá-francés</li><li>**865** : Nordic</li><li>**866** -Ruso</li><li>**869** : Griego moderno</li></ul> |
| /status | Muestra la página de códigos actual utilizada por este comando. |
| /? | Muestra la ayuda en el símbolo del sistema. |

#### <a name="remarks"></a>Observaciones

- El comando **Graftabl** afecta solo a la presentación del monitor de caracteres extendidos de la página de códigos que especifique. No cambia la página de código de entrada de la consola real. Para cambiar la página de códigos de entrada de la consola, use el comando [mode](mode.md) o [chcp](chcp.md) .

- Cada código de salida y una breve descripción:

    | Código de salida | Descripción |
    | --------- | ----------- |
    | 0 | El juego de caracteres se cargó correctamente. No se cargó ninguna página de códigos anterior. |
    | 1 | Se especificó un parámetro incorrecto. No se realizó ninguna acción. |
    | 2 | Error de archivo. |

- Puede usar la variable de entorno ERRORLEVEL en un programa por lotes para procesar códigos de salida devueltos por **Graftabl**.

### <a name="examples"></a>Ejemplos

Para ver la página de códigos actual utilizada por **Graftabl**, escriba:

```
graftabl /status
```

Para cargar el juego de caracteres gráficos de la página de códigos 437 (Estados Unidos) en la memoria, escriba:

```
graftabl 437
```

Para cargar el juego de caracteres gráficos de la página de códigos 850 (multilingüe) en la memoria, escriba:

```
graftabl 850
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [comando FREEDISK](freedisk.md)

- [modo (comando)](mode.md)

- [chcp (comando)](chcp.md)
