---
title: Conversión de un disco dinámico en un disco básico
description: Describe cómo convertir un disco dinámico en un disco básico.
ms.date: 12/18/2019
ms.topic: article
author: JasonGerend
manager: brianlic
ms.author: jgerend
ms.openlocfilehash: 3ffaf5db818377a3c75fda98255e7881fe6731aa
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87936014"
---
# <a name="change-a-dynamic-disk-back-to-a-basic-disk"></a>Conversión de un disco dinámico en un disco básico

> **Se aplica a:** Windows 10, Windows 8.1, Windows Server (Canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

En este tema se describe cómo eliminar todo el contenido de un disco dinámico y luego convertirlo en un disco básico. Los discos dinámicos han quedado en desuso en Windows y no se recomienda su uso. En su lugar, se recomienda usar discos básicos o la tecnología más reciente de [Espacios de almacenamiento](https://support.microsoft.com/help/12438/windows-10-storage-spaces) si se quiere agrupar discos en volúmenes de mayor tamaño. Si quieres crear una imagen espejo del volumen desde el que se inicia Windows, es posible que quieras usar un controlador RAID de hardware, como por ejemplo, el incluido en muchas placas base.

> [!WARNING]
> Para convertir un disco dinámico en un disco básico, debes eliminar todos los volúmenes del disco, lo que borra de forma permanente todos los datos del disco. Asegúrate de realizar copias de seguridad de todos los datos que quieras conservar antes de proceder.

## <a name="to-change-a-dynamic-disk-back-to-a-basic-disk-by-using-disk-management"></a>Para cambiar un disco dinámico por un disco básico mediante Administración de discos

1.  Realiza una copia de seguridad de todos los volúmenes del disco que quieras convertir de dinámicos a básicos.

2. Abre Administración de discos con permisos de administrador.

   Una manera fácil de hacerlo es escribir **Administración de equipos** en el cuadro de búsqueda de la barra de tareas, seleccionar y mantener pulsado (o hacer clic con el botón derecho) **Administración de equipos** y, después, seleccionar **Ejecutar como administrador** > **Sí**. Cuando se abra Administración de equipos, ve a **Almacenamiento** > **Administración de discos**.

2.  En Administración de discos, selecciona y mantén pulsado (o haz clic con el botón derecho) cada volumen del disco dinámico que quieras convertir en un disco básico y luego haz clic en **Eliminar volumen**.

3.  Cuando todos los volúmenes del disco se hayan eliminado, haz clic con el botón derecho en el disco y luego haz clic en **Convertir en disco básico**.

## <a name="to-change-a-dynamic-disk-back-to-a-basic-disk-by-using-a-command-line"></a>Para cambiar un disco dinámico por un disco básico mediante una línea de comandos

1.  Realiza una copia de seguridad de todos los volúmenes del disco que quieras convertir de dinámicos a básicos.

2.  Abra un símbolo del sistema y escriba `diskpart`.

3.  En el símbolo del sistema **DISKPART**, escribe `list disk`. Anota el número del disco que quieras convertir a básico.

4.  En el símbolo del sistema **DISKPART**, escribe `select disk <disknumber>`.

5.  En el símbolo del sistema **DISKPART**, escribe `detail disk`.

6.  Para cada volumen del disco, en el símbolo de sistema **DISKPART**, escribe `select volume= <volumenumber>` y luego escribe `delete volume`.

7.  En el símbolo de sistema **DISKPART**, escribe `select disk <disknumber>` y especifica el número del disco que quieres convertir en un disco básico.

8.  En el símbolo del sistema **DISKPART**, escribe `convert basic`.

| Value  | Descripción |
| --- | --- |
| **list disk**                         | Muestra una lista de discos e información sobre ellos, como su tamaño, la cantidad de espacio disponible, si se trata de un disco básico o dinámico y si el disco utiliza el estilo de partición de Registro de arranque maestro (MBR) o Tabla de particiones GUID (GPT). El disco marcado con un asterisco (*) tiene el foco. |
| **select disk** <em>disknumber</em>   | Selecciona el disco especificado, donde <em>disknumber</em> es el número de disco y el que recibe el foco.  |
| **detail disk** <em>disknumber</em>   | Muestra las propiedades del disco seleccionado y los volúmenes del mismo.  |
| **select volume** <em>disknumber</em> | Selecciona el volumen especificado, donde <em>disknumber</em> es el número de volumen y el que recibe el foco. Si no se especifica ningún volumen, el comando **select** muestra el volumen actual con el foco. Puedes especificar el volumen por número, letra de unidad o ruta de acceso de punto de montaje. En un disco básico, si seleccionas un volumen, este también recibe el foco de partición correspondiente. |
| **delete volume**                     | Elimina el volumen seleccionado. No puedes eliminar el volumen del sistema, el volumen de arranque o cualquier otro volumen que incluya el archivo de paginación activo o de volcado (volcado de memoria). |
| **convert basic** | Convierte un disco dinámico vacío en un disco básico.  |

## <a name="additional-considerations"></a>Consideraciones adicionales

-   El disco no debe incluir ningún volumen o dato antes de cambiarlo por un disco básico. Si quieres conservar los datos, realiza una copia de seguridad de los mismos o muévelos a otro volumen antes de convertir el disco en un disco básico.
-   Una vez que cambies un disco dinámico por un disco básico, solo puedes crear particiones y unidades lógicas en dicho disco.

## <a name="additional-references"></a>Referencias adicionales

-   [Notación de sintaxis de línea de comandos](/previous-versions/orphan-topics/ws.11/cc742449(v=ws.11))
