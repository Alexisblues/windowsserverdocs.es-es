---
title: color
description: Artículo de referencia del comando color, que cambia los colores de primer plano y de fondo de la ventana del símbolo del sistema para la sesión actual.
ms.topic: reference
ms.assetid: f5b67131-d196-45ec-a3f9-b5d9f091fd86
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 3ce7aa8e927e3796917d2720495f394636d9c240
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89028463"
---
# <a name="color"></a>color

Cambia los colores de primer plano y de fondo de la ventana del símbolo del sistema para la sesión actual. Si se usa sin parámetros, el **color** restaura los colores de primer plano y de fondo de la ventana del símbolo del sistema predeterminado.

## <a name="syntax"></a>Sintaxis

```
color [[<b>]<f>]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<b>` | Especifica el color de fondo. |
| `<f>` | Especifica el color de primer plano. |
| /? | Muestra la ayuda en el símbolo del sistema. |

Donde:

En la tabla siguiente se enumeran los dígitos hexadecimales válidos que puede usar como valores para `<b>` y `<f>` :

| Valor | Color |
| ----- | ----- |
| 0 | Negro |
| 1 | Azul |
| 2 | Verde |
| 3 | Aqua |
| 4 | Red |
| 5 | Púrpura |
| 6 | Amarillo |
| 7 | Blanco |
| 8 | Gris |
| 9 | Azul claro |
| a | Verde claro |
| b | Aguamarina claro |
| c | Rojo claro |
| d | Púrpura claro |
| e | Amarillo claro |
| f | Blanco brillante |

#### <a name="remarks"></a>Observaciones

- No use caracteres de espacio entre `<b>` y `<f>` .

- Si especifica un solo dígito hexadecimal, el color correspondiente se utiliza como color de primer plano y el color de fondo se establece en el color predeterminado.

- Para establecer el color predeterminado de la ventana del símbolo del sistema, seleccione la esquina superior izquierda de la ventana del **símbolo del sistema** , seleccione **valores predeterminados**, seleccione la pestaña **colores** y, a continuación, seleccione los colores que desee utilizar para el **texto de pantalla** y el fondo de la **pantalla**.

- Si `<b>` y `<f>` son el mismo valor de color, ERRORLEVEL se establece en y `1` no se realiza ningún cambio en el color de primer plano o de fondo.

## <a name="examples"></a>Ejemplos

Para cambiar el color de fondo de la ventana del símbolo del sistema a gris y el color de primer plano a rojo, escriba:

```
color 84
```

Para cambiar el color de primer plano de la ventana del símbolo del sistema a amarillo claro, escriba:

```
color e
```

> [!NOTE]
> En este ejemplo, el fondo se establece en el color predeterminado porque solo se especifica un dígito hexadecimal.

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
