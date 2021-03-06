---
title: ftp type
description: Artículo de referencia del comando FTP Type, que establece o muestra el tipo de transferencia de archivos.
ms.topic: reference
ms.assetid: 6e96dcd4-08f8-4e7b-90b7-1e1761fea4c7
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: f97c7959fcc0788298055b989433eec572d61584
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89035693"
---
# <a name="ftp-type"></a>ftp type

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Establece o muestra el tipo de transferencia de archivos. El comando **FTP** admite los tipos de transferencia de archivos de imagen ASCII (predeterminada) y binaria:

- Se recomienda usar ASCII al transferir archivos de texto. En el modo ASCII, se realizan las conversiones de caracteres a y desde el juego de caracteres estándar de red. Por ejemplo, los caracteres de fin de línea se convierten según sea necesario, en función del sistema operativo de destino.

- Se recomienda usar Binary al transferir archivos ejecutables. En el modo binario, los archivos se transfieren en unidades de un byte.

## <a name="syntax"></a>Sintaxis

```
type [<typename>]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `[<typename>]` | Especifica el tipo de transferencia de archivo. Si no se especifica este parámetro, se muestra el tipo actual.|

### <a name="examples"></a>Ejemplos

Para establecer el tipo de transferencia de archivo en ASCII, escriba:

```
type ascii
```

Para establecer el tipo de archivo de transferencia en binario, escriba:

```
type binary
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [Guía de FTP adicional](/previous-versions/orphan-topics/ws.10/cc756013(v=ws.10))
