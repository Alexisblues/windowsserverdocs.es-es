---
title: dfsdiag testdfsconfig
description: Artículo de referencia para dfsdiag testdfsconfig, que comprueba la configuración de un espacio de nombres Sistema de archivos distribuido (DFS).
ms.topic: reference
ms.assetid: 106aeeb9-ea79-4e6e-829c-eca06309bab2
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 60070b9f4076ee90cf0705992f31aff583f92968
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89024009"
---
# <a name="dfsdiag-testdfsconfig"></a>dfsdiag testdfsconfig

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Comprueba la configuración de un espacio de nombres de Sistema de archivos distribuido (DFS) mediante la realización de las siguientes acciones:

- Comprueba que el servicio de espacio de nombres DFS se está ejecutando y que su tipo de inicio está establecido en **automático** en todos los servidores de espacio de nombres.

- Comprueba que la configuración del registro DFS es coherente entre los servidores de espacio de nombres.

- Valida las siguientes dependencias en servidores de espacio de nombres en clúster:

  - Dependencia de recursos raíz de espacio de nombres en el recurso de nombre de red.

  - Dependencia de recurso de nombre de red en el recurso de dirección IP.

  - Dependencia de recursos raíz del espacio de nombres en el recurso de disco físico.

## <a name="syntax"></a>Sintaxis

```
dfsdiag /testdfsconfig /DFSroot:<namespace>
```

#### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| /DFSroot:`<namespace>` | Espacio de nombres (raíz DFS) que se va a diagnosticar. |

## <a name="examples"></a>Ejemplos

Para comprobar la configuración de los espacios de nombres de Sistema de archivos distribuido (DFS) en *contoso. com\MyNamespace*, escriba:

```
dfsdiag /testdfsconfig /DFSroot:\contoso.com\MyNamespace
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [comando dfsdiag](dfsdiag.md)
