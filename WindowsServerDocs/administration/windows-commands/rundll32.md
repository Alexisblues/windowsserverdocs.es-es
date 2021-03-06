---
title: rundll32
description: Artículo de referencia de * * * *-
ms.topic: reference
ms.assetid: 46d9cd64-8186-4cd4-a500-44700340fe81
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: f938edce72d29f7e316ae50733e8fe1062ec7365
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89037583"
---
# <a name="rundll32"></a>rundll32



Carga y ejecuta las bibliotecas de vínculos dinámicos (dll) de 32 bits. No hay ninguna configuración configurable para rundll32. Se proporciona información de ayuda para un archivo DLL específico que se ejecuta con el comando **rundll32** .

Debe ejecutar el comando **rundll32** desde un símbolo del sistema con privilegios elevados. Para abrir un símbolo del sistema con privilegios elevados, haga clic en **Inicio**, haga clic con el botón secundario en **símbolo del sistema**y, a continuación, haga clic en **Ejecutar como administrador**.

## <a name="syntax"></a>Sintaxis

```
Rundll32 <DLLname>
```

## <a name="commands"></a>Comandos

|Parámetro|Descripción|
|---------|-----------|
|[Rundll32 printui.dll, PrintUIEntry](rundll32-printui.md)|Muestra la interfaz de usuario de la impresora|

## <a name="remarks"></a>Observaciones

Rundll32 solo puede llamar a funciones de un archivo DLL escrito explícitamente para ser llamado por rundll32.

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)
