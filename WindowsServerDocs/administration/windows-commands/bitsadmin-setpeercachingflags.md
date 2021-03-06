---
title: bitsadmin setpeercachingflags
description: Artículo de referencia para el comando bitsadmin setpeercachingflags, que establece marcas que determinan si los archivos del trabajo pueden almacenarse en caché y servirse a los elementos del mismo nivel y si el trabajo puede descargar contenido de elementos del mismo nivel.
ms.topic: reference
ms.assetid: 3f54a127-fb68-49a5-b843-664ec833df67
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 1305d8d865f51556f4b518c7972eaff4ca9ec3e5
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89026213"
---
# <a name="bitsadmin-setpeercachingflags"></a>bitsadmin setpeercachingflags

Establece marcas que determinan si los archivos del trabajo se pueden almacenar en caché y servir a los elementos del mismo nivel y si el trabajo puede descargar contenido de elementos del mismo nivel.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /setpeercachingflags <job> <value>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |
| value | Entero sin signo, incluido:<ul><li>**1.** el trabajo puede descargar contenido de elementos del mismo nivel.</li><li>**2.** los archivos del trabajo se pueden almacenar en caché y servir a los equipos del mismo nivel.</li></ul> |

## <a name="examples"></a>Ejemplos

Para permitir que el trabajo denominado *myDownloadJob* Descargue contenido de elementos del mismo nivel:

```
bitsadmin /setpeercachingflags myDownloadJob 1
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
