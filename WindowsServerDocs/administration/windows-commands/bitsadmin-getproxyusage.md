---
title: bitsadmin getproxyusage
description: Artículo de referencia para el comando bitsadmin getproxyusage, que recupera la configuración de uso del proxy para el trabajo especificado.
ms.topic: reference
ms.assetid: f940a70e-3b02-497e-a47f-b37b905c299e
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 423168d72a88ecad90fd8de43eab3cb4486a750b
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89024409"
---
# <a name="bitsadmin-getproxyusage"></a>bitsadmin getproxyusage

Recupera la configuración de uso del proxy para el trabajo especificado.

## <a name="syntax"></a>Sintaxis

```
bitsadmin /getproxyusage <job>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| -------------- | -------------- |
| trabajo | El nombre para mostrar o el GUID del trabajo. |

#### <a name="output"></a>Output

Los valores de uso del proxy devueltos pueden ser:

- **Configuración** predeterminada: Use los valores predeterminados de Internet Explorer del propietario.

- **No_Proxy** : no use un servidor proxy.

- **Invalidar** : usa una lista de proxy explícita.

- **Detección** automática: detecta automáticamente la configuración de proxy.

## <a name="examples"></a>Ejemplos

Para recuperar el uso de proxy para el trabajo denominado *myDownloadJob*:

```
bitsadmin /getproxyusage myDownloadJob
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [bitsadmin (comando)](bitsadmin.md)
