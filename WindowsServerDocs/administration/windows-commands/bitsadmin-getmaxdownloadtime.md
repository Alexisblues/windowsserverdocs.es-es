---
title: bitsadmin getmaxdownloadtime
description: Artículo de referencia para el comando bitsadmin getmaxdownloadtime, que recupera el tiempo de espera de descarga en segundos.
ms.prod: windows-servemr
ms.topic: reference
ms.assetid: cdce64f6-7125-489d-be3c-4af1dfc8c46a
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 610553a839bb36bd764da1283ba398af49824731
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89030343"
---
# <a name="bitsadmin-getmaxdownloadtime"></a>bitsadmin getmaxdownloadtime

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Recupera el tiempo de espera de descarga en segundos.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /getmaxdownloadtime <job>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| -------------- | -------------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |

## <a name="examples"></a>Ejemplos

Para obtener el tiempo de descarga máximo para el trabajo llamado *myDownloadJob* en segundos:

```
bitsadmin /getmaxdownloadtime myDownloadJob
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
