---
title: Crear el objeto de directiva de grupo Publicación de hash para BranchCache
description: Este tema forma parte de la guía de implementación de BranchCache para Windows Server 2016, que muestra cómo implementar BranchCache en los modos de caché distribuida y hospedada para optimizar el uso del ancho de banda WAN en las sucursales.
manager: brianlic
ms.topic: get-started-article
ms.assetid: c3d33bed-83ef-4eb8-acf9-0719ecb4a931
ms.author: lizross
author: eross-msft
ms.openlocfilehash: ade42b3ff690e3c813c750609fb0b21b9999a85f
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87971882"
---
# <a name="create-the-branchcache-hash-publication-group-policy-object"></a>Crear el objeto de directiva de grupo Publicación de hash para BranchCache

>Se aplica a: Windows Server (canal semianual), Windows Server 2016

Puede usar este procedimiento para crear la publicación de hash de BranchCache directiva de grupo objeto (GPO).

El requisito mínimo para realizar este procedimiento es la pertenencia al grupo **Admins. del dominio** o grupo equivalente.

> [!NOTE]
> Antes de realizar este procedimiento, debe crear la unidad organizativa para servidores de archivos de BranchCache y mover los servidores de archivos a la unidad organizativa. Para obtener más información, vea [Habilitar la publicación de hash para servidores de archivos de miembros de dominio](../../branchcache/deploy/Enable-Hash-Publication-for-Domain-Member-File-Servers.md).

### <a name="to-create-the-branchcache-hash-publication-group-policy-object"></a>Para crear la publicación de hash de BranchCache directiva de grupo objeto

1.  Abra Windows PowerShell, escriba **mmv** y presione ENTRAR. Se abrirá Microsoft Management Console (MMC).

2.  En MMC, en el menú **Archivo**, haga clic en **Agregar o quitar complemento**. Se abre el cuadro de diálogo **Agregar o quitar complementos**.

3.  En **Agregar o quitar complementos**, en **Complementos disponibles**, haga doble clic en **Administración de directivas de grupo** y, a continuación, haga clic en **Aceptar**.

4.  En MMC de Administración de directivas de grupo, expanda la ruta de acceso a la unidad organizativa para servidores de archivos de BranchCache que creó previamente. Por ejemplo, si el bosque se denomina example.com, el dominio se denomina example1.com y la unidad organizativa se denomina servidores de archivos de BranchCache, expanda la ruta de acceso siguiente: **Directiva de grupo Management**, **Forest: example.com**, **Domains**, **example1.com**, **BranchCache file servers**.

5.  Haga clic con el botón secundario en **servidores de archivos de BranchCache**y, a continuación, haga clic en **crear un GPO en este dominio y vincularlo aquí**. Se abre el cuadro de diálogo **Nuevo GPO**. En **nombre**, escriba un nombre para el nuevo GPO. Por ejemplo, si desea que el nombre del objeto sea Publicación de hash para BranchCache, escriba **Publicación de hash para BranchCache**. Haga clic en **Aceptar**.



