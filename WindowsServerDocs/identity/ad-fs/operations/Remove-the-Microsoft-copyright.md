---
ms.assetid: c89a977c-b09f-44ec-be42-41e76a6cf3ad
title: Quitar el copyright de Microsoft
author: billmath
ms.author: billmath
manager: femila
ms.date: 05/31/2017
ms.topic: article
ms.openlocfilehash: ec7d9cb02508fc046ce3e8f0378e63c82eecca8d
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87949779"
---
# <a name="remove-the-microsoft-copyright"></a>Quitar el copyright de Microsoft



De forma predeterminada, las páginas AD FS contienen el copyright de Microsoft. Para quitar el copyright de las páginas que personalices, puedes usar el siguiente procedimiento.

![quitar Copyright](media/AD-FS-user-sign-in-customization/ADFS_Blue_Custom1.png)

## <a name="to-remove-the-microsoft-copyright"></a>Para quitar el copyright de Microsoft

1. Crea un tema personalizado basado en el predeterminado.

   ```powershell
   New-AdfsWebTheme –Name custom –SourceName default
   ```

2. Exporta el tema especificando la carpeta de salida.

   ```powershell
   Export-AdfsWebTheme -Name custom -DirectoryPath C:\CustomWebTheme
   ```

3. Busque el `Style.css` archivo que se encuentra en la carpeta de salida. Con el ejemplo anterior, la ruta de acceso sería`C:\CustomWebTheme\Css\Style.css.`

4. Abra el `Style.css` archivo con un editor como, por ejemplo, el Bloc de notas.

5. Busque el fragmento de `#copyright` y cámbielo por lo siguiente:

   ```css
   #copyright {color:#696969; display:none;}
   ```

6. Cree un tema personalizado basado en el nuevo `Style.css` archivo.

   ```powershell
   Set-AdfsWebTheme -TargetName custom -StyleSheet @{locale="";path="C:\customWebTheme\css\style.css"}
   ```

7. Activa el nuevo tema.

   ```powershell
   Set-AdfsWebConfig -ActiveThemeName custom
   ```

Ahora, ya no debe ver los derechos de autor en la parte inferior de la página de inicio de sesión.

![quitar Copyright](media/AD-FS-user-sign-in-customization/ADFS_Blue_Custom1a.png)

## <a name="additional-references"></a>Referencias adicionales
[Personalización de inicio de sesión de AD FS usuario](AD-FS-user-sign-in-customization.md)
