---
title: Configurar el reenvío de DNS y la confianza de dominio
ms.topic: article
manager: dongill
author: rpsqrd
ms.author: ryanpu
ms.date: 08/29/2018
ms.openlocfilehash: 102d1267fe2b15e50ab2d078647ff86f7c937a6d
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87966172"
---
# <a name="configure-dns-forwarding-in-the-hgs-domain-and-a-one-way-trust-with-the-fabric-domain"></a>Configuración del reenvío de DNS en el dominio HGS y una confianza unidireccional con el dominio de tejido

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

>[!IMPORTANT]
>El modo de AD está en desuso a partir de Windows Server 2019. En entornos donde no es posible la atestación de TPM, configure la [atestación de clave de host](guarded-fabric-initialize-hgs-key-mode.md). La atestación de clave de host proporciona una garantía similar al modo de AD y es más fácil de configurar.

Siga estos pasos para configurar el reenvío de DNS y establecer una confianza unidireccional con el dominio de tejido. Estos pasos permiten al HGS localizar los controladores de dominio del tejido y validar la pertenencia a grupos de los hosts de Hyper-V.

1.  Ejecute el siguiente comando en una sesión de PowerShell con privilegios elevados para configurar el reenvío de DNS. Reemplace fabrikam.com por el nombre del dominio de tejido y escriba las direcciones IP de los servidores DNS en el dominio de tejido. Para una mayor disponibilidad, señale a más de un servidor DNS.

    ```powershell
    Add-DnsServerConditionalForwarderZone -Name "fabrikam.com" -ReplicationScope "Forest" -MasterServers <DNSserverAddress1>, <DNSserverAddress2>
    ```

2.  Para crear una confianza de bosque unidireccional, ejecute el siguiente comando en un símbolo del sistema con privilegios elevados:

    Reemplace `bastion.local` por el nombre del dominio HGS y `fabrikam.com` por el nombre del dominio del tejido. Proporcione la contraseña para un administrador del dominio del tejido.

    ```powershell
    netdom trust bastion.local /domain:fabrikam.com /userD:fabrikam.com\Administrator /passwordD:<password> /add
    ```

## <a name="next-step"></a>Paso siguiente

> [!div class="nextstepaction"]
> [Configurar HTTPS](guarded-fabric-configure-hgs-https.md)
