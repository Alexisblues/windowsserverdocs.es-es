---
title: Información general sobre OpenSSH para Windows
description: Información general sobre las herramientas de OpenSSH que usan los administradores de Linux y otras plataformas distintas de Windows para la administración multiplataforma de sistemas remotos.
ms.date: 01/07/2019
contributor: damaerteMSFT
author: maertendmsft
ms.type: conceptual
ms.openlocfilehash: 1c0686d7bbe6e78baf924919c6733b733fe65f64
ms.sourcegitcommit: 53d526bfeddb89d28af44210a23ba417f6ce0ecf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2020
ms.locfileid: "87879498"
---
# <a name="openssh-in-windows"></a>OpenSSH en Windows

OpenSSH es la versión de código abierto de las herramientas de Secure Shell (SSH) que usan los administradores de Linux y otras que no son de Windows para la administración de distintas plataformas de sistemas remotos.
OpenSSH se ha agregado a Windows a partir del otoño de 2018 y se incluye en Windows 10 y Windows Server 2019.

SSH se basa en una arquitectura de cliente y servidor en la que el sistema en el que está trabajando el usuario es el cliente y el sistema remoto que se está administrando es el servidor.
OpenSSH incluye una variedad de componentes y herramientas diseñados para proporcionar un acercamiento seguro y sencillo a la administración remota del sistema, incluidos:

* sshd.exe, que es el componente del servidor SSH que debe estar en ejecución en el sistema que se administra de forma remota.
* ssh.exe, que es el componente de cliente de SSH que se ejecuta en el sistema local del usuario.
* ssh-keygen.exe genera, administra y convierte las claves de autenticación para SSH.
* ssh-agent.exe almacena las claves privadas que se usan para la autenticación de clave pública.
* ssh-add.exe agrega las claves privadas a la lista permitida por el servidor.
* ssh-keyscan.exe ayuda a recopilar las claves de host SSH públicas de varios hosts.
* sftp.exe es el servicio que proporciona el protocolo de transferencia de archivos seguro y se ejecuta a través de SSH.
* scp.exe es una utilidad de copia de archivos que se ejecuta en SSH.

La documentación de esta sección se centra en cómo se usa OpenSSH en Windows, incluida la instalación, así como los casos de uso y configuración específicos de Windows. Estos son los temas:

Puedes consultar documentación detallada adicional sobre las características comunes de OpenSSH en [OpenSSH.com](https://www.openssh.com/manual.html).

Los desarrolladores del proyecto OpenBSD administran el [proyecto de código abierto de OpenSSH](https://www.openssh.com) maestro.
La bifurcación de Microsoft de este proyecto se encuentra en [GitHub](https://github.com/PowerShell/openssh-portable).
Tus comentarios sobre Windows OpenSSH son bienvenidos y puedes enviárnoslos mediante la creación de incidencias de GitHub en nuestro [repositorio de OpenSSH de GitHub](https://github.com/PowerShell/openssh-portable).
