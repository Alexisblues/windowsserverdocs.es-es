---
title: Configuración de una máquina virtual con una controladora SCSI para poder enchufar y desconectar el almacenamiento en caliente
description: Versión en línea del texto de esta regla de Analizador de procedimientos recomendados.
manager: dongill
ms.author: kathydav
ms.topic: article
ms.assetid: 511e1172-aeef-463d-b5dd-2bffae411ff1
author: kbdazure
ms.date: 8/16/2016
ms.openlocfilehash: 0b914b2d250bbcb4c5e795ec778dde8db91613ec
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87948466"
---
# <a name="configure-a-virtual-machine-with-a-scsi-controller-to-be-able-to-hot-plug-and-hot-unplug-storage"></a>Configuración de una máquina virtual con una controladora SCSI para poder enchufar y desconectar el almacenamiento en caliente

>Se aplica a: Windows Server 2016



*Para obtener más información sobre los análisis y los procedimientos recomendados, consulte* [analizador de procedimientos recomendados](https://go.microsoft.com/fwlink/?LinkId=122786).

|Propiedad|Detalles|
|-|-|
|**Sistema operativo**|Windows Server 2016|
|**Producto/Característica**|Hyper-V|
|**Gravedad**|Advertencia|
|**Categoría**|Configuración|

En las secciones siguientes, cursiva indica el texto de la interfaz de usuario que aparece en la herramienta de Analizador de procedimientos recomendados para este problema.

## <a name="issue"></a>Incidencia

*Se encontró una máquina virtual que no está configurada con una controladora SCSI.*

## <a name="impact"></a>Impacto

*No podrá conectar en caliente o desconectar el almacenamiento para las siguientes máquinas virtuales:*

\<list of virtual machine names>

La capacidad de conectar y desconectar el almacenamiento en caliente facilita la administración de las necesidades de almacenamiento de una máquina virtual sin necesidad de tiempo de inactividad. Las máquinas virtuales sin controladores SCSI deben apagarse para poder agregar o quitar almacenamiento.

## <a name="resolution"></a>Resolución

*Si no necesita conectar en caliente o desconectar el almacenamiento para esta máquina virtual, no es necesario realizar ninguna acción. De lo contrario, apague la máquina virtual y agregue una controladora SCSI a la configuración.*

Para usar una controladora SCSI para el almacenamiento de conexión y desconexión en caliente, el sistema operativo invitado debe ejecutar la versión actual de Integration Services.



