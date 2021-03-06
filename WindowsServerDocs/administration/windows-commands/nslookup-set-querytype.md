---
title: nslookup set querytype
description: Artículo de referencia del comando Nslookup Set QueryType, que cambia el tipo de registro de recursos de la consulta.
ms.topic: reference
ms.assetid: 5af54ac5-fc1a-4af6-977b-f8e97c8eba90
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: b75fd9f80de828b6927289480351db106ba50fd6
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89038746"
---
# <a name="nslookup-set-querytype"></a>nslookup set querytype

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Cambia el tipo de registro de recursos de la consulta. Para obtener información acerca de los tipos de registro de recursos, consulte la [solicitud de comentarios (RFC) 1035](https://tools.ietf.org/html/rfc1035).

> [!NOTE]
> Este comando es el mismo que el comando [nslookup Set Type](nslookup-set-type.md) .

## <a name="syntax"></a>Sintaxis

```
set querytype=<resourcerecordtype>
```

### <a name="parameters"></a>Parámetros

| Parámetro | Descripción |
| --------- | ----------- |
| `<resourcerecordtype>` | Especifica un tipo de registro de recursos DNS. El tipo de registro de recursos **predeterminado es,** pero puede usar cualquiera de los siguientes valores:<ul><li>**R:** Especifica la dirección IP de un equipo.</li><li>**Cualquiera:** Especifica la dirección IP de un equipo.</li><li>**CNAME:** Especifica un nombre canónico para un alias.</li><li>**GID** Especifica un identificador de grupo de un nombre de grupo.</li><li>**HINFO:** Especifica la CPU y el tipo de sistema operativo de un equipo.</li><li>**MB:** Especifica un nombre de dominio de buzón.</li><li>**Mg:** Especifica un miembro del grupo de correo.</li><li>**MINFO:** Especifica la información de buzón o de lista de correo.</li><li>**Mr:** Especifica el nombre de dominio del cambio de nombre de correo.</li><li>**Mx:** Especifica el intercambiador de correo.</li><li>**NS:** Especifica un servidor de nombres DNS para la zona con nombre.</li><li>**PTR:** Especifica un nombre de equipo si la consulta es una dirección IP; de lo contrario, especifica el puntero a otra información.</li><li>**SOA:** Especifica el inicio de autoridad de una zona DNS.</li><li>**Txt:** Especifica la información de texto.</li><li>**UID:** Especifica el identificador de usuario.</li><li>**UINFO:** Especifica la información del usuario.</li><li>**WKS:** Describe un servicio bien conocido.</li></ul> |
| /? | Muestra la ayuda en el símbolo del sistema. |
| /help | Muestra la ayuda en el símbolo del sistema. |

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [nslookup set type](nslookup-set-type.md)
