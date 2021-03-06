---
title: help
description: Artículo de referencia del comando ayuda, que muestra una lista de los comandos disponibles o información de ayuda detallada sobre un comando especificado.
ms.topic: reference
ms.assetid: c65b5ac3-711a-4368-95b8-ba82e2d00713
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 701b3a1840ac56e399bb4febf0765c2f69a84633
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89035463"
---
# <a name="help"></a>help

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Muestra una lista de los comandos disponibles o información de ayuda detallada sobre un comando especificado. Si se usa sin parámetros, las listas de **ayuda** y describen brevemente cada comando del sistema.

## <a name="syntax"></a>Sintaxis

```
help [<command>]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<command>` | Especifica el comando para el que se va a mostrar información de ayuda detallada. |

### <a name="examples"></a>Ejemplos

Para ver información acerca del comando **Robocopy** , escriba:

```
help robocopy
```

Para mostrar una lista de todos los comandos disponibles en DiskPart, escriba:

```
help
```

Para mostrar información detallada sobre la ayuda sobre cómo usar el comando **Create Partition Primary** en DiskPart, escriba:

```
help create partition primary
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
