---
title: ftp put
description: Artículo de referencia del comando FTP Put, que copia un archivo local en el equipo remoto mediante el tipo de transferencia de archivos actual.
ms.topic: reference
ms.assetid: 95cc1e3f-523d-4374-98b8-16e6c276b2ca
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 03/30/2020
ms.openlocfilehash: 518ef051b0e515351a14a0d6895ad50100f1dbd8
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89030573"
---
# <a name="ftp-put"></a>ftp put

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Copia un archivo local en el equipo remoto mediante el tipo de transferencia de archivos actual.

> [!NOTE]
> Este comando es el mismo que el [comando FTP Send](ftp-send_1.md).

## <a name="syntax"></a>Sintaxis

```
put <localfile> [<remotefile>]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<localfile>` | Especifica el archivo local que se va a copiar. |
| `[<remotefile>]` | Especifica el nombre que se va a usar en el equipo remoto. Si no especifica un *archivoremoto*, el archivo asigna el nombre *archivolocal* .|

### <a name="examples"></a>Ejemplos

Para copiar el archivo local *test.txt* y asignarle el nombre *test1.txt* en el equipo remoto, escriba:

```
put test.txt test1.txt
```

Para copiar el archivo local *program.exe* en el equipo remoto, escriba:

```
put program.exe
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [comando ASCII de FTP](ftp-ascii.md)

- [comando binario de FTP](ftp-binary.md)

- [Guía de FTP adicional](/previous-versions/orphan-topics/ws.10/cc756013(v=ws.10))
