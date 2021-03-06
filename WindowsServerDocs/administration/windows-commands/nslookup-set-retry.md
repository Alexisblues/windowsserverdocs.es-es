---
title: nslookup set retry
description: Artículo de referencia del comando Nslookup set retry, que establece el número de intentos para obtener información de un servidor especificado.
ms.topic: reference
ms.assetid: 615fdfa2-fa29-47a8-8c9e-a6c5b45b3b71
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 10f60b48485ae51d727f17a5cfcec8b2af61a743
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89025179"
---
# <a name="nslookup-set-retry"></a>nslookup set retry

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Si no se recibe una respuesta dentro de un período de tiempo determinado, el tiempo de espera se duplica y se reenvía la solicitud. Este comando establece el número de veces que se reenvía una solicitud a un servidor para obtener información, antes de abandonarla.

> [!NOTE]
> Para cambiar el período de tiempo antes de que se agote el tiempo de espera de la solicitud, use el comando [nslookup Set timeout](nslookup-set-timeout.md) .

## <a name="syntax"></a>Sintaxis

```
set retry=<number>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| ---------- | ---------- |
| `<number>` | Especifica el nuevo valor para el número de reintentos. El número predeterminado de reintentos es **4**. |
| /? | Muestra la ayuda en el símbolo del sistema. |
| /help | Muestra la ayuda en el símbolo del sistema. |

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [nslookup set timeout](nslookup-set-timeout.md)
