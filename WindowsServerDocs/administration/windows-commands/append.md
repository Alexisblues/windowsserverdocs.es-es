---
title: append
description: Artículo de referencia del comando APPEND, que permite a los programas abrir archivos de datos en directorios especificados, como si estuvieran en el directorio actual.
ms.topic: reference
ms.assetid: 9c3fea20-9502-40ad-a442-7a927aad88eb
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 6a92b87a9e35af45480c01f0a2422abc14fb3ca1
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89029413"
---
# <a name="append"></a>append

Permite a los programas abrir archivos de datos en directorios especificados como si estuvieran en el directorio actual. Si se usa sin parámetros, **Append** muestra la lista de directorios anexados.

> [!NOTE]
> Este comando no se admite en Windows 10.

## <a name="syntax"></a>Sintaxis

```
append [[<drive>:]<path>[;...]] [/x[:on|:off]] [/path:[:on|:off] [/e]
append ;
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `[\<drive>:]<path>` | Especifica una unidad y un directorio para anexar. |
| /x: on | Aplica los directorios anexados a las búsquedas de archivos y las aplicaciones de inicio. |
| /x: desactivado | Solo se aplica a las solicitudes para abrir archivos. La opción **/x: OFF** es la configuración predeterminada. |
| /path: activado | Aplica los directorios anexados a las solicitudes de archivos que ya especifican una ruta de acceso. **/path: on** es el valor predeterminado. |
| /path: desactivado | Desactiva el efecto de **/path: on**. |
| /e | Almacena una copia de la lista de directorios anexada en una variable de entorno denominada APPEND. **/e** solo se puede usar la primera vez que se usa **Append** después de iniciar el sistema. |
| ; | Borra la lista de directorios anexados. |
| /? | Muestra la ayuda en el símbolo del sistema. |

## <a name="examples"></a>Ejemplos

Para borrar la lista de directorios anexados, escriba:

```
append ;
```

Para almacenar una copia del directorio anexado en una variable de entorno denominada *Append*, escriba:

```
append /e
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
