---
title: logman query
description: Artículo de referencia para el comando Logman Query, que consulta las propiedades del recopilador de datos o del conjunto de recopiladores de datos.
ms.topic: reference
ms.assetid: 1116a0f0-5415-4369-a045-12f79f8f66de
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: e7d3d9da5b5885c15135b764454bd68818c4aded
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89023789"
---
# <a name="logman-query"></a>logman query

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Consulta las propiedades del recopilador de datos o del conjunto de recopiladores de datos.

## <a name="syntax"></a>Sintaxis

```
logman query [providers|Data Collector Set name] [options]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| -s `<computer name>` | Ejecute el comando en el equipo remoto especificado. |
| -config `<value>` | Especifica el archivo de configuración que contiene opciones de comando. |
| [-n] `<name>` | Nombre del objeto de destino. |
| -ETS | Envía comandos a sesiones de seguimiento de eventos directamente sin guardar o programar. |
| /? | Muestra la ayuda contextual. |

### <a name="examples"></a>Ejemplos

Para enumerar todos los conjuntos de recopiladores de datos configurados en el sistema de destino, escriba:

```
logman query
```

Para enumerar los recopiladores de datos contenidos en el conjunto de recopiladores de datos denominado *perf_log*, escriba:

```
logman query perf_log
```

Para enumerar todos los proveedores disponibles de recopiladores de datos en el sistema de destino, escriba:

```
logman query providers
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [Logman (comando)](logman.md)
