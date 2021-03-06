---
title: bitsadmin setnotifycmdline
description: Artículo de referencia del comando bitsadmin setnotifycmdline, que establece el comando de línea de comandos que se ejecutará cuando el trabajo finalice la transferencia de datos o cuando un trabajo entre en un estado.
ms.topic: reference
ms.assetid: 415ae6ef-8549-48b2-9693-2368a6e24075
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 7f486efcbaef5f68d6f8be7cab1caba204c77c7a
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89026233"
---
# <a name="bitsadmin-setnotifycmdline"></a>bitsadmin setnotifycmdline

Establece el comando de línea de comandos que se ejecuta cuando el trabajo finaliza la transferencia de datos o después de que un trabajo entra en un estado especificado.

> [!NOTE]
> Este comando no es compatible con BITS 1,2 y versiones anteriores.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /setnotifycmdline <job> <program_name> [program_parameters]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |
| program_name | Nombre del comando que se va a ejecutar cuando se complete el trabajo. Puede establecer este valor en NULL, pero si lo hace, *program_parameters* también debe establecerse en NULL. |
| program_parameters | Parámetros que se van a pasar a *program_name*. Este valor se puede establecer como NULL. Si *program_parameters* no está establecido en null, el primer parámetro de *program_parameters* debe coincidir con el *program_name*. |

## <a name="examples"></a>Ejemplos

Para ejecutar Notepad.exe al finalizar el trabajo denominado *myDownloadJob*:

```
bitsadmin /setnotifycmdline myDownloadJob c:\winnt\system32\notepad.exe NULL
```

Para mostrar el texto del CLUF en Notepad.exe, al finalizar el trabajo denominado myDownloadJob:

```
bitsadmin /setnotifycmdline myDownloadJob c:\winnt\system32\notepad.exe notepad c:\eula.txt
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
