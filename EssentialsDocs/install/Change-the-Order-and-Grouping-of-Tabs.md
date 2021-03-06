---
title: Cambiar el orden y la agrupación de las fichas
description: Describe cómo usar Windows Server Essentials
ms.date: 10/03/2016
ms.topic: article
ms.assetid: 79a417fd-1b3e-47ab-ae33-bb1faf95c86d
author: nnamuhcs
ms.author: coreyp
manager: dongill
ms.openlocfilehash: 37b443a90ebdb2c6042596747f6c364fafe073a7
ms.sourcegitcommit: 04637054de2bfbac66b9c78bad7bf3e7bae5ffb4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2020
ms.locfileid: "87838084"
---
# <a name="change-the-order-and-grouping-of-tabs"></a>Cambiar el orden y la agrupación de las fichas

>Se aplica a: Windows Server 2016 Essentials, Windows Server 2012 R2 Essentials, Windows Server 2012 Essentials

Puede cambiar el orden de las pestañas del Panel para que la suya sea la primera (a la izquierda) de la fila de pestañas. Para ello necesitará agregar una entrada al registro. También puede modificar la agrupación de las pestañas agregando entradas al registro. El orden de las pestañas puede ser su pestaña principal seguida de las pestañas integradas de Microsoft, después sus otras pestañas y finalmente las pestañas de terceros.

## <a name="change-the-order-of-the-tabs-in-the-dashboard"></a>Cambiar el orden de las pestañas en el Panel
 Es necesario que agregue el identificador del complemento que se muestre en su pestaña para que el registro defina el orden.

#### <a name="to-display-your-tab-first-in-the-list-of-tabs"></a>Para que su pestaña aparezca la primera de la lista

1.  En el equipo de referencia. haga clic en **Inicio**, escriba **regedit** y después presione **Entrar**.

2.  En el panel izquierdo, expanda **HKEY_LOCAL_MACHINE**, **SOFTWARE**, **Microsoft** y finalmente **Windows Server**. Si la clave **OEM** no existe, siga los pasos que se indican a continuación para crearla:

    1.  Haga clic con el botón secundario en **Windows Server**, seleccione **Nuevo** y a continuación haga clic en **Clave**.

    2.  Escriba **OEM** como nombre de la clave.

3.  Haga clic con el botón secundario en **OEM**, seleccione **Nuevo** y a continuación haga clic en **Valor de cadena**.

4.  Escriba **DashboardMainTabID** como el nombre de la clave y a continuación pulse **Entrar**.

5.  Haga clic con el botón secundario sobre la nueva cadena en el panel derecho y a continuación haga clic en **Modificar**.

6.  Escriba el GUID que se haya definido para la pestaña de nivel superior y pulse **Entrar**.

     Para obtener más información acerca de la creación e identificación de pestañas de nivel superior, consulte [Cómo crear una pestaña de nivel superior](/previous-versions/windows/server-essentials/gg513957(v=msdn.10)) en el SDK de Soluciones de Windows Server.

7.  Guarde los cambios realizados en el registro.

8.  También deberá incluir el GUID de la pestaña principal de nivel superior en la lista de identificadores de agrupaciones de pestañas. Para ello, siga los pasos indicados en **Cómo cambiar la agrupación de las pestañas en el Panel**.

## <a name="change-the-grouping-of-tabs-in-the-dashboard"></a>Cómo cambiar la agrupación de las pestañas en el Panel
 Para asegurarse de que las pestañas estén agrupadas y aparezcan en la lista de pestañas integradas de Microsoft, agregue los identificadores al registro.

#### <a name="to-change-the-grouping-of-tabs"></a>Para cambiar la agrupación de las pestañas

1.  Si regedit no se abre, haga clic en **Inicio**, escriba **regedit** y a continuación pulse **Entrar**.

2.  En el panel izquierdo, expanda **HKEY_LOCAL_MACHINE**, **SOFTWARE**, **Microsoft** y finalmente **Windows Server**.

3.  Haga clic con el botón secundario en **OEM**, seleccione **Nuevo** y haga clic en **Clave**.

4.  Escriba **DashboardAddins** como el nombre de la clave y a continuación pulse **Entrar**.

5.  Haga clic con el botón secundario en **DashboardAddins**, seleccione **Nuevo** y a continuación haga clic en **Valor de cadena**.

6.  Escriba el identificador GUID de la pestaña como el nombre de la cadena. No es necesario ningún valor.

7.  Repita los pasos 5 y 6 para cada una de las pestañas y subpestañas.

8.  Guarde los cambios realizados en el registro.

## <a name="see-also"></a>Consulte también
 [Crear y personalizar la imagen](Creating-and-Customizing-the-Image.md) [personalizaciones adicionales](Additional-Customizations.md) [preparar la imagen para probar la implementación de](Preparing-the-Image-for-Deployment.md) [la experiencia del cliente](Testing-the-Customer-Experience.md)