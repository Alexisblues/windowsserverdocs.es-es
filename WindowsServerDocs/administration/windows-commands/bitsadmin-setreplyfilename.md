---
title: bitsadmin setreplyfilename
description: Artículo de referencia del comando bitsadmin setreplyfilename, que especifica la ruta de acceso del archivo que contiene la respuesta de carga del servidor.
ms.topic: reference
ms.assetid: c26d3342-0533-40b1-a13e-e09678232b25
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 2991503ad558b318f52d07447af18d4f9e6178aa
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89033423"
---
# <a name="bitsadmin-setreplyfilename"></a>bitsadmin setreplyfilename

Especifica la ruta de acceso del archivo que contiene la respuesta de carga del servidor.

> [!NOTE]
> Este comando no es compatible con BITS 1,2 y versiones anteriores.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /setreplyfilename <job> <file_path>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| -------------- | -------------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |
| file_path | Ubicación para poner el servidor de carga-respuesta. |

## <a name="examples"></a>Ejemplos

Para establecer la ruta de acceso del archivo de nombre de archivo de la respuesta de carga para el trabajo denominado *myDownloadJob*:

```
bitsadmin /setreplyfilename myDownloadJob c:\upload-reply
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
