---
ms.assetid: da035189-e87f-4597-9933-49bf391a8d5d
title: Adición del vínculo a la página principal
author: billmath
ms.author: billmath
manager: femila
ms.date: 05/31/2017
ms.topic: article
ms.openlocfilehash: 4bd64d19f5e203086c4a5576f331fde9d1b33cf7
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87954291"
---
# <a name="add-home-link"></a>Adición del vínculo a la página principal

Para agregar el vínculo de inicio que se muestra en la \- Página de inicio de sesión, use el siguiente cmdlet de Windows PowerShell y la siguiente sintaxis.


![Agregar vínculo de inicio](media/AD-FS-user-sign-in-customization/ADFS_Blue_Custom2.png)


`Set-AdfsGlobalWebContent -HomeLink https://fs1.contoso.com/home/ -HomeLinkText Home `


> [!IMPORTANT]
> El parámetro `linkText` de este cmdlet solo es obligatorio si usa un valor distinto del predeterminado, que es *Home*. La ventaja de usar el valor predeterminado es que las páginas están localizadas para todas las configuraciones regionales de los clientes. después de personalizar la página de inicio \- de sesión, la personalización tiene precedencia, por lo que debe personalizarla para todos los idiomas que desee admitir.

## <a name="additional-references"></a>Referencias adicionales
[Personalización de inicio de sesión de AD FS usuario](AD-FS-user-sign-in-customization.md)
