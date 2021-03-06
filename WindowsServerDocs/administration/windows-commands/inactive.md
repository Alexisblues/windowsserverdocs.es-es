---
title: inactivo
description: Artículo de referencia para el comando inactivo, que marca la partición del sistema o la partición de arranque con el foco como inactivo en discos básicos de registro de arranque maestro (MBR).
ms.topic: reference
ms.assetid: f4fb4695-4e66-4166-b4ab-2c86a4605580
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: 50b9145b809eb7a0f8605a27db97b2c7ac36d539
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89037983"
---
# <a name="inactive"></a>inactivo

Marca la partición del sistema o la partición de arranque con el foco como inactivo en discos básicos de registro de arranque maestro (MBR).

Se debe seleccionar una partición de arranque o del sistema activa para que esta operación se realice correctamente. Use el comando [Select Partition Command](select-partition.md) para seleccionar la partición activa y cambiar el foco a ella.

> [!CAUTION]
> Si no existe una partición activa, puede que el equipo no se inicie. No marque una partición de sistema o de arranque como inactiva, a menos que sea un usuario con experiencia con un conocimiento exhaustivo de la familia de sistemas operativos Windows.<p>Si no puede iniciar el equipo después de marcar la partición de sistema o de arranque como inactiva, inserte el instalación de Windows CD en la unidad de CD-ROM, reinicie el equipo y, a continuación, repare la partición mediante los comandos **fixmbr** y **fixboot** de la consola de recuperación.
>
> Después de marcar la partición del sistema o la partición de arranque como inactiva, el equipo se inicia con la siguiente opción especificada en el BIOS, como la unidad de CD-ROM o un entorno de ejecución previo al arranque (PXE).

## <a name="syntax"></a>Sintaxis

```
inactive
```

### <a name="examples"></a>Ejemplos

```
inactive
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [seleccionar partición (comando)](select-partition.md)

- [Solución avanzada de problemas de arranque de Windows](/windows/client-management/advanced-troubleshooting-boot-problems)
