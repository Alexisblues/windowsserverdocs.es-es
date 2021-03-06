---
title: No se deben configurar puertos serie en máquinas virtuales de generación 2
description: Versión en línea del texto de esta regla de Analizador de procedimientos recomendados.
manager: dongill
ms.author: kathydav
ms.topic: article
ms.assetid: 87061193-dd3f-4398-aa5d-4cee83cadfa3
author: kbdazure
ms.date: 8/16/2016
ms.openlocfilehash: b842adcb098a76edc6c42020dd87f8f3e224d9bd
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87938984"
---
# <a name="serial-ports-should-not-be-configured-on-generation-2-virtual-machines"></a>No se deben configurar puertos serie en máquinas virtuales de generación 2

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
*Una o varias máquinas virtuales de generación 2 tienen un puerto serie configurado.*

## <a name="impact"></a>**Impacto**
*El rendimiento puede verse afectado en las siguientes máquinas virtuales:*

\<list of virtual machines>

## <a name="resolution"></a>**Resolución**
*Si esto es intencionado, no es necesario realizar ninguna otra acción. En caso contrario, considere la posibilidad de usar el administrador de Hyper-V o Windows PowerShell para quitar la cadena de conexión de los puertos serie de la máquina virtual.*



