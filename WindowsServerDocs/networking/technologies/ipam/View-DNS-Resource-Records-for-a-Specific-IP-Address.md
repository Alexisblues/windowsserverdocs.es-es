---
title: Visualización de registros de recursos DNS para una dirección IP específica
description: Este tema forma parte de la guía de administración de la administración de direcciones IP (IPAM) en Windows Server 2016.
manager: brianlic
ms.topic: article
ms.assetid: f590fb86-4195-4f90-98cb-e90459d4c1e3
ms.author: lizross
author: eross-msft
ms.openlocfilehash: 211dcfdc17cfa81aad7adb1a424a9fadc0c932c6
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87944606"
---
# <a name="view-dns-resource-records-for-a-specific-ip-address"></a>Visualización de registros de recursos DNS para una dirección IP específica

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

Puede usar este tema para ver los registros de recursos DNS que están asociados a la dirección IP que elija.

El requisito mínimo para realizar este procedimiento es la pertenencia al grupo **Administradores** o grupo equivalente.

### <a name="to-view-resource-records-for-an-ip-address"></a>Para ver los registros de recursos de una dirección IP

1.  En Administrador del servidor, haga clic en **IPAM**. Aparece la consola de cliente de IPAM.

2.  En el panel de navegación, en **espacio de direcciones IP**, haga clic en **inventario de direcciones IP**. En el panel de navegación inferior, haga clic en **IPv4** o **IPv6**. El inventario de direcciones IP aparece en la vista de búsqueda del panel de información. Busque y seleccione la dirección IP cuyos registros de recursos DNS desea ver.

    ![Ver el inventario de direcciones IP](../../media/View-DNS-Resource-Records-for-a-Specific-IP-Address/ipam_IPInventory_01.jpg)

3.  En la vista de **detalles**del panel de información, haga clic en **registros de recursos DNS**. Se muestran los registros de recursos asociados a la dirección IP seleccionada.

    ![Visualización de registros de recursos DNS](../../media/View-DNS-Resource-Records-for-a-Specific-IP-Address/ipam_IPInventory_02.jpg)

## <a name="see-also"></a>Consulte también
Administración de registros de [recursos DNS](DNS-Resource-Record-Management.md) 
 [Administrar IPAM](Manage-IPAM.md)



