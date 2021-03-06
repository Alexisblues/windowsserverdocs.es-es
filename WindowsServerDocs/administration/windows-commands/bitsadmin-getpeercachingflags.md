---
title: bitsadmin getpeercachingflags
description: Artículo de referencia para el comando bitsadmin getpeercachingflags, que recupera marcas que determinan si los archivos del trabajo pueden almacenarse en caché y servirse a los elementos del mismo nivel, y si BITS puede descargar el contenido del trabajo desde los elementos del mismo nivel.
ms.topic: reference
ms.assetid: 3c3c9f28-4c04-4c49-a23a-dee5bbcc8981
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 6c6d7b53dc9c9ff99188b98d19e1418cbf9f1656
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89028723"
---
# <a name="bitsadmin-getpeercachingflags"></a>bitsadmin getpeercachingflags

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Recupera marcas que determinan si los archivos del trabajo se pueden almacenar en caché y servir a los elementos del mismo nivel, y si BITS puede descargar el contenido del trabajo de los elementos del mismo nivel.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /getpeercachingflags <job>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| -------------- | -------------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |

## <a name="examples"></a>Ejemplos

Para recuperar las marcas para el trabajo denominado *myDownloadJob*:

```
bitsadmin /getpeercachingflags myDownloadJob
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
