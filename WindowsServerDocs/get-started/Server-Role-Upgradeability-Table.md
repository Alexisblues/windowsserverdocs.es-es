---
title: Matriz de actualización y migración del rol de servidor para Windows Server 2016
description: Muestra los roles de servidor que se pueden actualizar o migrar a Windows Server 2016.
ms.date: 10/05/2016
ms.topic: article
ms.assetid: 7e031a64-b1e6-4cf6-994a-e7c575835f6a
author: jaimeo
ms.author: jaimeo
manager: dongill
ms.localizationpriority: medium
ms.openlocfilehash: ee263e7de5d16c9992102b8c09cc709f51fa719d
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87959303"
---
# <a name="server-role-upgrade-and-migration-matrix-for-windows-server-2016"></a>Matriz de actualización y migración del rol de servidor para Windows Server 2016

>Se aplica a: Windows Server 2016

En la cuadrícula de esta página se explican las opciones de actualización y migración de roles de servidor específicamente para migrar a Windows Server 2016. Para obtener instrucciones para la migración de roles individuales, visite [Migración de roles y características en Windows Server](./migrate-roles-and-features.md). Para más información sobre la instalación y las actualizaciones, vea [Windows Server Installation, Upgrade, and Migration](./installation-and-upgrade.md) (Instalación, actualización y migración de Windows Server).

|Rol de servidor|¿Se puede actualizar desde Windows Server 2012 R2?|¿Se puede actualizar desde Windows Server 2012?|¿Se admite la migración?|¿La migración puede completarse sin tiempo de inactividad?|
|-------------------|----------|--------------|--------------|----------|
|Servicios de certificados de Active Directory|    Sí|    Sí|    Sí|    No|
|Servicios de dominio de Active Directory|    Sí|    Sí|    Sí|    Sí|
|Servicios de federación de Active Directory (AD FS)|    No|    No|    Sí|    No (es necesario agregar nuevos nodos a la granja)|
|Active Directory Lightweight Directory Services|    Sí|    Sí|    Sí|    Sí|
|Active Directory Rights Management Services|    Sí|    Sí|    Sí|    No|
|Servidor DHCP|    Sí|    Sí|    Sí|    Sí|
|Servidor DNS|    Sí|    Sí|    Sí|    No|
|Clúster de conmutación por error|Sí, con el proceso de [Cluster OS Rolling Upgrade](../failover-clustering/cluster-operating-system-rolling-upgrade.md) (Actualización gradual de sistema operativo de clúster) que incluye el nodo Pause-Drain, Evict, actualizar a Windows Server 2016 y volver a unir el clúster original. Sí, cuando el servidor se quita del clúster para la actualización y después se agrega a un clúster diferente.|No mientras el servidor forma parte de un clúster. Sí, cuando el servidor se quita del clúster para la actualización y después se agrega a un clúster diferente.    |Sí|No para clústeres de conmutación por error en Windows Server 2012. Sí, para clústeres de conmutación por error de Windows Server 2012 R2 con máquinas virtuales de Hyper-V o clústeres de conmutación por error de Windows Server 2012 R2 que ejecutan el rol de Servidor de archivos de escalabilidad horizontal. Vea [Cluster OS Rolling Upgrade](../failover-clustering/cluster-operating-system-rolling-upgrade.md) (Actualización gradual de sistema operativo de clúster).|
|Servicios de archivos y almacenamiento|    Sí|    Sí|    Varía según la subcaracterística|    No|
|Hyper-V| Sí. (Cuando el host forma parte de un clúster con el proceso de actualización gradual de sistema operativo de clúster que incluye el nodo Pause-Drain, Evict, actualizar a Windows Server 2016 y volver a unir el clúster original).|  No|   Sí|  No para clústeres de conmutación por error en Windows Server 2012. Sí, para clústeres de conmutación por error de Windows Server 2012 R2 con máquinas virtuales de Hyper-V o clústeres de conmutación por error de Windows Server 2012 R2 que ejecutan el rol de Servidor de archivos de escalabilidad horizontal. Vea [Cluster OS Rolling Upgrade](../failover-clustering/cluster-operating-system-rolling-upgrade.md) (Actualización gradual de sistema operativo de clúster).|
|Servicios de impresión y fax|    No|    No|    Sí (Printbrm.exe)|    No|
|Servicios de Escritorio remoto|    Sí, para todos los subroles, pero no se admite la granja de modo mixto|    Sí, para todos los subroles, pero no se admite la granja de modo mixto|    Sí|    No|
|Servidor web (IIS)|    Sí|    Sí|    Sí|    No|
|Experiencia con Windows Server Essentials|    Sí|    N/A: nueva característica|    Sí|    No|
|Windows Server Update Services|    Sí|    Sí|    Sí|    No|
|Carpetas de trabajo|    Sí|    Sí|    Sí|    Sí, en el clúster de WS 2012 R2, cuando se usa la [Actualización gradual de sistema operativo de clúster](../failover-clustering/cluster-operating-system-rolling-upgrade.md).|
