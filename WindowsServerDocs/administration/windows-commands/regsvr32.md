---
title: regsvr32
description: Artículo de referencia para el comando regsvr32, que registra los archivos. dll como componentes de comando en el registro.
ms.topic: reference
ms.assetid: 3345e964-7d3e-42b8-abeb-42ed6edfe2b2
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 3bb39070ba1744ca261419e5b996144f89b17b11
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89027432"
---
# <a name="regsvr32"></a>regsvr32

Registra los archivos. dll como componentes de comando en el registro.

## <a name="syntax"></a>Sintaxis

```
regsvr32 [/u] [/s] [/n] [/i[:cmdline]] <Dllname>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
|--|--|
| /U | Anula el registro del servidor. |
| /s | Impide que se muestren mensajes. |
| /n | Evita la llamada a **DllRegisterServer**. Este parámetro requiere que también se use el parámetro **/i** . |
| /i`<cmdline>` | Pasa una cadena de línea de comandos (*cmdline*) opcional a **DllInstall**. Si usa este parámetro con el parámetro **/u** , llama a **DllUninstall**. |
| `<Dllname>` | Nombre del archivo. dll que se va a registrar. |
| /? | Muestra la ayuda en el símbolo del sistema. |

### <a name="examples"></a>Ejemplos

Para registrar el archivo. dll para el esquema de Active Directory, escriba:

```
regsvr32 schmmgmt.dll
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
