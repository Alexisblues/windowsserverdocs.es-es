---
title: dispdiag
description: Artículo de referencia para el comando dispdiag, que registra la información en un archivo.
ms.topic: reference
ms.assetid: 5079e1dd-b57c-44ed-970f-e6b409369e03
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 92dd0b49d8907f3ec934fd59d61b0504b622e80b
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89030843"
---
# <a name="dispdiag"></a>dispdiag

Los registros muestran información en un archivo.

## <a name="syntax"></a>Sintaxis

```
dispdiag [-testacpi] [-d] [-delay <seconds>] [-out <filepath>]
```

#### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| - testacpi | Ejecuta la prueba de diagnóstico de Hotkey. Muestra el nombre de la clave, el código y el código de examen de cualquier clave presionada durante la prueba. |
| -d | Genera un archivo de volcado de memoria con los resultados de las pruebas. |
| -retraso `<seconds>` | Retrasa la recopilación de datos según el tiempo especificado en *segundos*. |
| -out `<filepath>`  | Especifica la ruta de acceso y el nombre de archivo para guardar los datos recopilados. Este debe ser el último parámetro. |
| -? | Muestra los parámetros de comando disponibles y proporciona ayuda para usarlos. |

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
