---
title: Filtrado de la vista de registros de recursos DNS
description: Este tema forma parte de la guía de administración de la administración de direcciones IP (IPAM) en Windows Server 2016.
manager: brianlic
ms.topic: article
ms.assetid: 5b80294a-7325-476b-84eb-69f0d051e8b2
ms.author: lizross
author: eross-msft
ms.openlocfilehash: 5c629c4f05e0eb1198a6dc1a2ac074967765ff7b
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87971792"
---
# <a name="filter-the-view-of-dns-resource-records"></a>Filtrado de la vista de registros de recursos DNS

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

Puede usar este tema para filtrar la vista de los registros de recursos DNS en la consola de cliente de IPAM.

El requisito mínimo para realizar este procedimiento es la pertenencia al grupo **Administradores** o grupo equivalente.

### <a name="to-filter-the-view-of-dns-resource-records"></a>Para filtrar la vista de los registros de recursos DNS

1.  En Administrador del servidor, haga clic en **IPAM**. Aparece la consola de cliente de IPAM.

2.  En el panel de navegación, en **supervisión y administración**, haga clic en **zonas DNS**.  El panel de navegación se divide en un panel de navegación superior y un panel de navegación inferior.

3.  En el panel de navegación inferior, haga clic en **búsqueda directa**. Todas las zonas de búsqueda directa de DNS administradas por IPAM se muestran en los resultados de la búsqueda del panel de información.

4.  Haga clic en la zona cuyos registros desea ver y filtrar.

5.  En el panel de información, haga clic en **vista actual**y, a continuación, haga clic en **registros de recursos**. Los registros de recursos de la zona se muestran en el panel de información.

6.  En el panel de información, haga clic en **Agregar criterios**.

    ![Agregar criterios](../../media/Filter-the-View-of-DNS-Resource-Records/ipam_FilterRR_01.jpg)

7.  Seleccione un criterio de la lista desplegable. Por ejemplo, si desea ver un tipo de registro específico, haga clic en **tipo de registro**.

    ![Seleccionar un criterio](../../media/Filter-the-View-of-DNS-Resource-Records/ipam_FilterRR_02.jpg)

8.  Haga clic en **Agregar**.

    ![Agregar los criterios](../../media/Filter-the-View-of-DNS-Resource-Records/ipam_FilterRR_03.jpg)

9. El **tipo de registro** se agrega como parámetro de búsqueda. Escriba el texto para el tipo de registro que desea buscar. Por ejemplo, si desea ver solo los registros SRV, escriba **SRV**.

    ![Especifique el tipo de registro que desea buscar](../../media/Filter-the-View-of-DNS-Resource-Records/ipam_FilterRR_04.jpg)

10. Presione ENTRAR. Los registros de recursos DNS se filtran según los criterios y la frase de búsqueda que haya especificado.

    ![Ejecutar el filtro](../../media/Filter-the-View-of-DNS-Resource-Records/ipam_FilterRR_05.jpg)

## <a name="see-also"></a>Consulte también
Administración de registros de [recursos DNS](DNS-Resource-Record-Management.md) 
 [Administrar IPAM](Manage-IPAM.md)



