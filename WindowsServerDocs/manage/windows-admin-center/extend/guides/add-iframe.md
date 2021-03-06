---
title: Agregar un iFrame a una extensión de herramienta
description: 'Desarrollar una extensión de herramienta SDK del centro de administración de Windows (proyecto Honolulu): agregar un iFrame a una extensión de herramienta'
ms.topic: article
author: nwashburn-ms
ms.author: niwashbu
ms.date: 09/18/2018
ms.localizationpriority: medium
ms.openlocfilehash: da145d4ef3a58af51846d395081fb643af7c78ac
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87945112"
---
# <a name="add-an-iframe-to-a-tool-extension"></a>Agregar un iFrame a una extensión de herramienta

>Se aplica a: Windows Admin Center, versión preliminar de Windows Admin Center

En este artículo, se agregará un iFrame a una nueva extensión de herramienta vacía que se ha creado con la CLI del centro de administración de Windows.

## <a name="prepare-your-environment"></a>Preparación del entorno ##

Si todavía no lo ha hecho, siga las instrucciones de [desarrollo de una extensión de herramienta](../develop-tool.md) para preparar el entorno y crear una nueva extensión de herramienta vacía.

## <a name="add-a-module-to-your-project"></a>Agregar un módulo al proyecto ##

Agregue un nuevo [módulo vacío](add-module.md) al proyecto, en el que se agregará un iframe en el paso siguiente.

## <a name="add-an-iframe-to-your-module"></a>Agregar un iFrame al módulo ##

Ahora vamos a agregar un iFrame a ese nuevo módulo vacío que acabamos de crear.

En \src\app \, , vaya a la carpeta del módulo y Abra ```{!module-name}.component.html``` el archivo, que se encuentra con la siguiente Convención de nomenclatura:

| Value | Explicación | Nombre de archivo de ejemplo |
| ----- | ----------- | ------- |
| ```{!module-name}``` | Nombre del módulo (en minúsculas, espacios reemplazados por guiones) | ```manage-foo-works-portal.component.html``` |

Agregue el siguiente contenido al archivo HTML:

``` html
<div>
  <iframe  style="height: 850px;" src="https://www.bing.com"></iframe>
</div>
```

Es decir, ha agregado un iFrame a la extensión.  Después, puede [compilar y cargar](../develop-tool.md#build-and-side-load-your-extension) la extensión en el centro de administración de Windows para ver los resultados.

> [!Note]
> La configuración de la Directiva de seguridad de contenido (CSP) podría impedir que algunos sitios se representen en un iFrame dentro del centro de administración de Windows. Puede obtener más información al respecto [aquí](https://content-security-policy.com/).
