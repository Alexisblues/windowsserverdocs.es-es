---
title: Aumentar las autenticaciones simultáneas procesadas por NPS
description: En este tema se proporcionan instrucciones sobre cómo configurar las autenticaciones simultáneas del servidor de directivas de redes en Windows Server 2016.
manager: brianlic
ms.topic: article
ms.assetid: 2d9cdada-0625-41c8-8248-a32259b03e47
ms.author: lizross
author: eross-msft
ms.openlocfilehash: 2b21f357204ab61434bd12ba9121fb45dc84570f
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87969432"
---
# <a name="increase-concurrent-authentications-processed-by-nps"></a>Aumentar las autenticaciones simultáneas procesadas por NPS

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

Puede usar este tema para obtener instrucciones sobre cómo configurar las autenticaciones simultáneas del servidor de directivas de redes.

Si instaló NPS del servidor \( de directivas \) de redes en un equipo que no sea un controlador de dominio y el NPS recibe un gran número de solicitudes de autenticación por segundo, puede mejorar el rendimiento de NPS aumentando el número de autenticaciones simultáneas permitidas entre el NPS y el controlador de dominio.

Para ello, debe editar la siguiente clave del registro:

`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Netlogon\Parameters`

Agregue un nuevo valor denominado **MaxConcurrentApi** y asígnele un valor comprendido entre 2 y 5.

>[!CAUTION]
>Si asigna un valor a **MaxConcurrentApi** que es demasiado alto, el NPS podría realizar una carga excesiva en el controlador de dominio.

Para obtener más información sobre la administración de NPS, consulte [administrar el servidor de directivas de redes](nps-manage-top.md).

Para obtener más información acerca de NPS, consulte [servidor de directivas de redes (NPS)](nps-top.md).