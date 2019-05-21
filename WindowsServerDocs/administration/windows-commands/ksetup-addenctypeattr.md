---
title: ksetup:addenctypeattr
description: 'Tema de los comandos de Windows para ***- '
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-windows-commands
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 32cc87d7-b9e1-4d14-9eb7-3b439c55aa3a
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 711da6a81269fc838ca091765ddbcac63c3fe6e4
ms.sourcegitcommit: 0d0b32c8986ba7db9536e0b8648d4ddf9b03e452
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2019
ms.locfileid: "59886396"
---
# <a name="ksetupaddenctypeattr"></a>ksetup:addenctypeattr



Agrega el atributo de tipo de cifrado a la lista de posibles tipos para el dominio. Para obtener ejemplos de cómo se puede usar este comando, consulte [ejemplos](#BKMK_Examples).

## <a name="syntax"></a>Sintaxis

```
ksetup /addenctypeattr <DomainName> {DES-CBC-CRC | DES-CBC-MD5 | RC4-HMAC-MD5 | AES128-CTS-HMAC-SHA1-96 | AES256-CTS-HMAC-SHA1-96}
```

### <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|---------|-----------|
|\<DomainName>|Nombre del dominio al que va a establecer una conexión. Utilice el nombre de dominio completo o un formulario simple del nombre, por ejemplo, corp.contoso.com o contoso.|
|Tipo de cifrado|Debe ser uno de los siguientes tipos de cifrado admitidos:</br>-   DES-CBC-CRC</br>-   DES-CBC-MD5</br>-   RC4-HMAC-MD5</br>-   AES128-CTS-HMAC-SHA1-96</br>-   AES256-CTS-HMAC-SHA1-96|

## <a name="remarks"></a>Comentarios

Para ver el tipo de cifrado para el vale de concesión de vales (TGT) de Kerberos y la clave de sesión, ejecute el **klist** de comandos y ver la salida.

Puede establecer o agregar varios tipos de cifrado mediante la separación de los tipos de cifrado en el comando con un espacio. Sin embargo, puede solo hacerlo para un dominio a la vez.

Si el comando se ejecuta correctamente o produce un error, se muestra un mensaje de estado.

Para establecer el dominio que desea conectarse y usar, ejecute el **/Domain ksetup \<DomainName >** comando.

## <a name="BKMK_Examples"></a>Ejemplos

Determinar los tipos de cifrado actuales que se establecen en este equipo:
```
klist
```
Establezca el dominio corp.contoso.com:
```
ksetup /domain corp.contoso.com
```
Agregue el tipo de cifrado AES-256-CTS-HMAC-SHA1-96 a la lista de posibles tipos para el dominio corp.contoso.com:
```
ksetup /addenctypeattr corp.contoso.com AES-256-CTS-HMAC-SHA1-96
```
Establezca el atributo de tipo de cifrado en AES-256-CTS-HMAC-SHA1-96 para el dominio corp.contoso.com:
```
ksetup /setenctypeattr corp.contoso.com AES-256-CTS-HMAC-SHA1-96
```
Compruebe que el atributo de tipo de cifrado se ha establecido según lo previsto en el dominio:
```
ksetup /getenctypeattr corp.contoso.com
```

#### <a name="additional-references"></a>Referencias adicionales

-   [Klist](klist.md)
-   [Ksetup:domain](ksetup-domain.md)
-   [Ksetup:setenctypeattr](ksetup-setenctypeattr.md)
-   [Ksetup:getenctypeattr](ksetup-getenctypeattr.md)
-   [Ksetup:delenctypeattr](ksetup-delenctypeattr.md)
-   [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)