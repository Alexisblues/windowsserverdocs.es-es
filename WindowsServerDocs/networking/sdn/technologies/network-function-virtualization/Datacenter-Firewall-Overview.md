---
title: Información general de Datacenter Firewall
description: Puede usar este tema para obtener información sobre el Firewall de centros de seguridad, que es una capa de red, números de puerto de 5-tupla (Protocolo, número de puerto de origen y destino, direcciones IP de origen y de destino), Firewall multiinquilino con estado en Windows Server 2016.
manager: grcusanz
ms.topic: article
ms.assetid: 67576533-206b-428a-956c-ed8c53218d9b
ms.author: anpaul
author: AnirbanPaul
ms.openlocfilehash: 40c827282d1145ea711670842e95db3c61139683
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87952522"
---
# <a name="datacenter-firewall-overview"></a>Información general de Datacenter Firewall

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

Firewall de centro de recursos es un nuevo servicio incluido en Windows Server 2016. Es un nivel de red, 5-tupla (Protocolo, números de puerto de origen y de destino, direcciones IP de origen y de destino), Firewall multiempresa con estado. Cuando el proveedor de servicios implementa y ofrece como servicio, los administradores de inquilinos pueden instalar y configurar directivas de Firewall para ayudar a proteger sus redes virtuales del tráfico no deseado procedente de redes de Internet e Intranet.

![Firewall de Datacenter en la pila de red](../../../media/Datacenter-Firewall-Overview/MultitenantFirewallOverview2.png)

El administrador del proveedor de servicios o el administrador de inquilinos pueden administrar las directivas de firewall del centro de seguridad a través de la controladora de red y las API de Northbound.

El firewall del centro de seguridad de ofrece las siguientes ventajas para los proveedores de servicios en la nube:

-   Una solución de Firewall basada en software muy escalable, administrable y diagnóstico que se puede ofrecer a los inquilinos.

-   Libertad de trasladar máquinas virtuales de inquilinos a distintos hosts de proceso sin interrumpir las directivas de Firewall de inquilino

    -   Implementado como un firewall del agente host del puerto vSwitch

    -   Las máquinas virtuales de inquilino obtienen las directivas asignadas a su firewall de agente de host de vSwitch

    -   Las reglas de Firewall se configuran en cada puerto vSwitch, independientemente del host real que ejecuta la máquina virtual.

-   Ofrece protección a las máquinas virtuales de inquilinos independientemente del sistema operativo invitado del inquilino.

El firewall del centro de seguridad de ofrece las siguientes ventajas para los inquilinos:

-   Capacidad de definir reglas de Firewall para ayudar a proteger las cargas de trabajo orientadas a Internet en redes virtuales

-   Capacidad de definir reglas de Firewall para ayudar a proteger el tráfico entre máquinas virtuales en la misma subred virtual de nivel 2, así como entre máquinas virtuales en subredes virtuales de nivel 2 diferentes.

-   Capacidad de definir reglas de Firewall para ayudar a proteger y aislar el tráfico de red entre las redes locales de inquilinos y sus redes virtuales en el proveedor de servicios.



