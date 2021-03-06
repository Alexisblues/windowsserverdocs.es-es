---
title: nslookup ls
description: Artículo de referencia del comando Nslookup LS, que muestra información del dominio DNS.
ms.topic: reference
ms.assetid: f15f06fe-67e7-41a9-93b5-192ab14ab380
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: c37054002edcebe1551ef9d6aed4210978e52832
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89023489"
---
# <a name="nslookup-ls"></a>nslookup ls

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Muestra información de dominio DNS.

## <a name="syntax"></a>Sintaxis

```
ls [<option>] <DNSdomain> [{[>] <filename>|[>>] <filename>}]
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<option>` | Entre las opciones válidas se incluyen:<ul><li>**-t:** Enumera todos los registros del tipo especificado. Para obtener más información, consulte [nslookup Set QueryType](nslookup-set-querytype.md).</li><li>**-a:** Enumera los alias de los equipos del dominio DNS. Este parámetro es igual que **-t CNAME**</li><li>**-d:** Enumera todos los registros del dominio DNS. Este parámetro es igual que **-t any**</li><li>**-h:** Muestra información de CPU y del sistema operativo para el dominio DNS. Este parámetro es el mismo que **-t HINFO**</li><li>**-s:** Enumera los servicios conocidos de los equipos del dominio DNS. Este parámetro es igual que **-t WKS**. |
| `<DNSdomain>` | Especifica el dominio DNS para el que desea obtener información. |
| `<filename>` | Especifica un nombre de archivo que se utilizará para la salida guardada. Puede usar los caracteres mayor que ( `>` ) y Double mayor que ( `>>` ) para redirigir la salida de la manera habitual. |
| /? | Muestra la ayuda en el símbolo del sistema. |
| /help | Muestra la ayuda en el símbolo del sistema. |

#### <a name="remarks"></a>Observaciones

- La salida predeterminada de este comando incluye nombres de equipo y sus direcciones IP asociadas.

- Si el resultado se dirige a un archivo, se agregan marcas de hash por cada 50 registros recibidos del servidor.

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [nslookup set querytype](nslookup-set-querytype.md)
