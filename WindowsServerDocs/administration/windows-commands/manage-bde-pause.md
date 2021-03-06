---
title: la pausa de Manage-BDE
description: Artículo de referencia para el comando Manage-BDE PAUSE, que pone en pausa el cifrado o descifrado de BitLocker.
ms.topic: reference
ms.assetid: efda0e08-b9ff-4e71-83d8-bb666b3032bd
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 7260728851b40db1c547176185653b9537beea41
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89036333"
---
# <a name="manage-bde-pause"></a>la pausa de Manage-BDE

Pausa el cifrado o descifrado de BitLocker.

## <a name="syntax"></a>Sintaxis

```
manage-bde -pause [<volume>] [-computername <name>] [{-?|/?}] [{-help|-h}]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<volume>` | Especifica una letra de unidad seguida de dos puntos, una ruta de acceso de GUID de volumen o un volumen montado. |
| -COMPUTERNAME | Especifica que se utilizará manage-bde.exe para modificar la protección de BitLocker en otro equipo. También puede usar **-CN** como una versión abreviada de este comando. |
| `<name>` | Representa el nombre del equipo en el que se va a modificar la protección de BitLocker. Los valores aceptados incluyen el nombre NetBIOS del equipo y la dirección IP del equipo. |
| -? o/? | Muestra una breve ayuda en el símbolo del sistema. |
| -Help o-h | Muestra la ayuda completa en el símbolo del sistema. |

### <a name="examples"></a>Ejemplos

Para pausar el cifrado de BitLocker en la unidad C, escriba:

```
manage-bde pause C:
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [Manage-BDE on (comando)](manage-bde-on.md)

- [comando Manage-BDE OFF](manage-bde-off.md)

- [comando Manage-BDE resume](manage-bde-resume.md)

- [comando Manage-BDE](manage-bde.md)
