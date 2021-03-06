---
title: ntcmdprompt
description: Artículo de referencia para el comando ntcmdprompt, que ejecuta el intérprete de comandos **Cmd.exe**, en lugar de **Command.com**, después de ejecutar un comando finalizar y permanecer residente (TSR) o después de iniciar el símbolo del sistema desde una aplicación de ms-dos.
ms.topic: reference
ms.assetid: 0063bdbb-dc2b-41c4-99ee-b011603aaa86
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 557db55ea99b209f2bca152f1e45622aa0df4887
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89032763"
---
# <a name="ntcmdprompt"></a>ntcmdprompt

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Ejecuta el intérprete de comandos **Cmd.exe**, en lugar de **Command.com**, después de ejecutar un comando finalizar y permanecer residente (TSR) o después de iniciar el símbolo del sistema desde una aplicación de ms-dos.

## <a name="syntax"></a>Sintaxis

```
ntcmdprompt
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| /? | Muestra la ayuda en el símbolo del sistema. |

#### <a name="remarks"></a>Observaciones

- Cuando **Command.com** se está ejecutando, algunas características de **Cmd.exe**, como la visualización de **doskey** del historial de comandos, no están disponibles. Si prefiere ejecutar el intérprete de comandos de **Cmd.exe** después de haber iniciado una terminación y permanecer residente (TSR) o de iniciar el símbolo del sistema desde una aplicación basada en MS-dos, puede usar el comando **ntcmdprompt** . Sin embargo, tenga en cuenta que es posible que el TSR no esté disponible para su uso cuando se ejecuta **Cmd.exe**. Puede incluir el comando **ntcmdprompt** en el archivo **config. NT** o el archivo de inicio personalizado equivalente en el archivo de información de programa (PIF) de una aplicación.

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
