---
title: Virtualización de recuperación de bosque de AD
ms.author: iainfou
author: iainfoulds
manager: daveba
ms.date: 08/09/2018
ms.topic: article
ms.assetid: c49b40b2-598d-49aa-85b4-766bce960e0d
ms.openlocfilehash: aa6598c2a033147928d05c8175886c1c2425b4cd
ms.sourcegitcommit: 1dc35d221eff7f079d9209d92f14fb630f955bca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "88938055"
---
# <a name="active-directory-forest-recovery-virtualization"></a>Virtualización de recuperación de bosque de Active Directory

>Se aplica a: Windows Server 2016, Windows Server 2012 y 2012 R2, Windows Server 2008 y 2008 R2

En este tema se describe la característica de clonación de controladores de dominio virtualizados en Windows Server 2016, 2012 R2 y 2012.

## <a name="using-virtualized-domain-controller-cloning-to-expedite-forest-recovery"></a>Uso de la clonación de controladores de dominio virtualizados para acelerar la recuperación de bosques

La clonación de controladores de dominio virtualizados (DC) simplifica y agiliza el proceso de instalación de controladores de dominio virtualizados adicionales en un dominio, especialmente en ubicaciones centralizadas, como centros de recursos en los que varios controladores de dominio se ejecutan en hipervisores. Después de restaurar un controlador de dominio virtual en cada dominio desde una copia de seguridad, los controladores de dominio adicionales de cada dominio se pueden poner en línea rápidamente mediante el proceso de clonación de controladores de dominio virtualizados. Puede preparar el primer controlador de dominio virtualizado que se va a recuperar, cerrarlo y, a continuación, copiar el disco duro virtual tantas veces como sea necesario para crear controladores de dominio virtualizados clonados para compilar el dominio.

Los requisitos para la clonación de controladores de dominio virtualizados son:

- El hipervisor debe ser compatible con VM-GenerationID. Hyper-V en Windows Server 2016, 2012 y Windows 8 es un ejemplo de un hipervisor que admite VM-GenerationID. Consulte con el proveedor del hipervisor si se admite VM-GenerationID.
- El controlador de dominio virtualizado que se usa como origen para la clonación debe ejecutar Windows Server 2016 o 2012 y ser miembro del grupo controladores de dominio clonables.
- El emulador de PDC debe ejecutar Windows Server 2016 o 2012. Puede clonar el emulador de PDC si está virtualizado.

Para obtener instrucciones paso a paso acerca de cómo realizar la clonación de controladores de dominio virtualizados, consulte [Introducción a la virtualización de Active Directory Domain Services (AD DS) (nivel 100)](../Introduction-to-Active-Directory-Domain-Services-AD-DS-Virtualization-Level-100.md). Para obtener más información sobre cómo funciona la clonación de controladores de dominio virtualizados, consulte [referencia técnica de controladores de dominio virtualizados (nivel 300)](../deploy/virtual-dc/virtualized-domain-controller-technical-reference--level-300-.md).

## <a name="next-steps"></a>Pasos siguientes

- [Recuperación del bosque de AD: requisitos previos](AD-Forest-Recovery-Prerequisties.md)
- [Recuperación de bosque de AD: diseño de un plan de recuperación de bosque personalizado](AD-Forest-Recovery-Devising-a-Plan.md)
- [Recuperación del bosque de AD: identificación del problema](AD-Forest-Recovery-Identify-the-Problem.md)
- [Recuperación del bosque de AD: determinar cómo recuperar](AD-Forest-Recovery-Determine-how-to-Recover.md)
- [Recuperación de bosque de AD: realizar la recuperación inicial](AD-Forest-Recovery-Perform-initial-recovery.md)
- [Recuperación del bosque de AD: procedimientos](AD-Forest-Recovery-Procedures.md)
- [Recuperación de bosque de AD: preguntas más frecuentes](AD-Forest-Recovery-FAQ.md)
- [Recuperación de bosque de AD: recuperación de un solo dominio en un bosque de varios dominios](AD-Forest-Recovery-Single-Domain-in-Multidomain-Recovery.md)
- [Recuperación de bosque de AD: recuperación de bosque con controladores de dominio de Windows Server 2003](AD-Forest-Recovery-Windows-Server-2003.md)
