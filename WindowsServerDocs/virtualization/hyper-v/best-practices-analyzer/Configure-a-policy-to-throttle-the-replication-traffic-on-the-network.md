---
title: Configurar una directiva para limitar el tráfico de replicación en la red
description: Versión en línea del texto de esta regla de Analizador de procedimientos recomendados.
manager: dongill
ms.author: kathydav
ms.topic: article
ms.assetid: 82cb1aef-cdc3-4d0a-88d4-ef497ab79606
author: kbdazure
ms.date: 8/16/2016
ms.openlocfilehash: dcee85911ebcc93e935a7df30d43768a15978ece
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87957182"
---
# <a name="configure-a-policy-to-throttle-the-replication-traffic-on-the-network"></a>Configurar una directiva para limitar el tráfico de replicación en la red

>Se aplica a: Windows Server 2016

Para más información sobre los análisis y los procedimientos recomendados, vea [Ejecución de análisis del Analizador de procedimientos recomendados y administración de los resultados de los análisis](https://go.microsoft.com/fwlink/p/?LinkID=223177).

|Propiedad|Detalles|
|-|-|
|**Sistema operativo**|Windows Server 2016|
|**Producto/Característica**|Hyper-V|
|**Gravedad**|Advertencia|
|**Categoría**|Configuración|

En las secciones siguientes, cursiva indica el texto de la interfaz de usuario que aparece en la herramienta de Analizador de procedimientos recomendados para este problema.

## <a name="issue"></a>Incidencia
*Es posible que no haya un límite en la cantidad de ancho de banda de red que puede consumir la replicación.*

## <a name="impact"></a>Impacto
*El ancho de banda de red podría estar completamente dominado por el tráfico de replicación, lo que afecta a otras actividades de red críticas. Esto afecta a los siguientes puertos:*

\<list of virtual machines>

## <a name="resolution"></a>Resolución
*Si usa otro método para limitar el tráfico de red, puede pasarlo por alto. De lo contrario, use el editor de directiva de grupo para configurar una directiva que limitará el tráfico de red al puerto pertinente del servidor réplica.*




