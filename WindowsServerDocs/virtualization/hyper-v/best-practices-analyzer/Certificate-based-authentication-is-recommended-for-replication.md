---
title: Se recomienda la autenticación basada en certificados para la replicación
description: Versión en línea del texto de esta regla de Analizador de procedimientos recomendados.
manager: dongill
ms.author: kathydav
ms.topic: article
ms.assetid: d931cc57-414f-4bdf-9ebd-08fd5e22b19d
author: kbdazure
ms.date: 8/16/2016
ms.openlocfilehash: ec5415d0bdad10c4b0f4f0560141dd290eca8e36
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87954502"
---
# <a name="certificate-based-authentication-is-recommended-for-replication"></a>Se recomienda la autenticación basada en certificados para la replicación

>Se aplica a: Windows Server 2016

Para más información sobre los análisis y los procedimientos recomendados, vea [Ejecución de análisis del Analizador de procedimientos recomendados y administración de los resultados de los análisis](https://go.microsoft.com/fwlink/p/?LinkID=223177).

|Propiedad|Detalles|
|-|-|
|**Sistema operativo**|Windows Server 2016|
|**Producto/Característica**|Hyper-V|
|**Gravedad**|Advertencia|
|**Categoría**|Configuración|

En las secciones siguientes, cursiva indica el texto de la interfaz de usuario que aparece en la herramienta de Analizador de procedimientos recomendados para este problema.

## <a name="issue"></a>**Problema**
*Una o varias máquinas virtuales seleccionadas para la replicación están configuradas para la autenticación Kerberos.*

## <a name="impact"></a>**Impacto**
*El tráfico de red de replicación del servidor principal al servidor de replicación no está cifrado. Esto afecta a las siguientes máquinas virtuales:*

\<list of virtual machines>

## <a name="resolution"></a>**Resolución**
*Si se usa otro método para realizar el cifrado, puede pasarlo por alto. De lo contrario, modifique la configuración de la máquina virtual para elegir autenticación basada en certificados.*



