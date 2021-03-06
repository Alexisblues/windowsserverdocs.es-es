---
title: logman update cfg
description: Artículo de referencia del comando Logman Update cfg, que actualiza las propiedades de un recopilador de datos de configuración existente.
ms.topic: reference
ms.assetid: 9da4e8b4-3be5-42d3-b0b4-c429630c35c4
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
ms.openlocfilehash: b4a952819f4fd2ffe9be6a188fd07db933117667
ms.sourcegitcommit: 96d46c702e7a9c3a321bbbb5284f73911c7baa3c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "89036541"
---
# <a name="logman-update-cfg"></a>logman update cfg

> Se aplica a: Windows Server (canal semianual), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2 y Windows Server 2012

Actualiza las propiedades de un recopilador de datos de configuración existente.

## <a name="syntax"></a>Sintaxis

```
logman update cfg <[-n] <name>> [options]
```

### <a name="parameters"></a>Parámetros


| Parámetro | Descripción |
| --------- | ----------- |
| -s `<computer name>` | Ejecuta el comando en el equipo remoto especificado. |
| -config `<value>` | Especifica el archivo de configuración que contiene opciones de comando. |
| [-n] `<name>` | Nombre del objeto de destino. |
| -[-] u `<user [password]>` | Especifica el usuario que se va a ejecutar como. Al escribir un \* para la contraseña, se solicita la contraseña. La contraseña no se muestra cuando se escribe en la solicitud de contraseña. |
| -m `<[start] [stop] [[start] [stop] [...]]>` | Cambios en el inicio o detención manual en lugar de una hora de inicio o de finalización programada. |
| -RF `<[[hh:]mm:]ss>` | Ejecuta el recopilador de datos durante el período de tiempo especificado. |
| -b `<M/d/yyyy h:mm:ss[AM|PM]>` | Comienza a recopilar datos en el momento especificado. |
| -e `<M/d/yyyy h:mm:ss[AM|PM]>` | Finaliza la recopilación de datos en el momento especificado. |
| -Si `<[[hh:]mm:]ss>` | Especifica el intervalo de ejemplo para los recopiladores de datos del contador de rendimiento. |
| -o `<path|dsn!log>` | Especifica el archivo de registro de salida o el DSN y el nombre del conjunto de registros en una base de datos SQL. |
| -[-] r | Repite el recopilador de datos diariamente a las horas de inicio y finalización especificadas. |
| -[-] a | Anexa un archivo de registro existente. |
| -[-] permitir | Sobrescribe un archivo de registro existente. |
| -[-] v `<nnnnnn|mmddhhmm>` | Adjunta información de versión del archivo al final del nombre del archivo de registro. |
| -[-] RC `<task>` | Ejecuta el comando especificado cada vez que se cierra el registro. |
| -[-] máx. `<value>` | Tamaño máximo del archivo de registro en MB o número máximo de registros para los registros de SQL. |
| -[-] CNF `<[[hh:]mm:]ss>` | Cuando se especifica Time, crea un nuevo archivo cuando ha transcurrido el tiempo especificado. Cuando no se especifica Time, crea un archivo nuevo cuando se supera el tamaño máximo. |
| -y | Responde afirmativamente a todas las preguntas sin preguntar. |
| -[-] ni | Habilita (-o) o deshabilita la consulta de interfaz de red (-ni). |
| -REG `<path [path [...]]>` | Especifica los valores del registro que se van a recopilar. |
| -gestión `<query [query [...]]>` | Especifica los objetos WMI que se van a recopilar mediante el lenguaje de consulta SQL. |
| -FTC `<path [path [...]]>` | Especifica la ruta de acceso completa a los archivos que se van a recopilar. |
| /? | Muestra la ayuda contextual. |

#### <a name="remarks"></a>Observaciones

- Donde [-] aparece en la lista, al agregar un guion adicional (-) se anula la opción.

### <a name="examples"></a>Ejemplos

Para actualizar un recopilador de datos de configuración llamado *cfg_log*, para recopilar la clave del registro `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Currentverion\` , escriba:

```
logman update cfg cfg_log -reg HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Currentverion\
```

## <a name="additional-references"></a>Referencias adicionales

- [Clave de sintaxis de línea de comandos](command-line-syntax-key.md)

- [Logman Create cfg (comando)](logman-create-cfg.md)

- [Logman (comando)](logman.md)
