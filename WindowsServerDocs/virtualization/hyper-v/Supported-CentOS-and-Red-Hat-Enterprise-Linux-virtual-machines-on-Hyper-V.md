---
title: Compatibilidad con máquinas virtuales de alta y Red Hat Enterprise Linux en Hyper-V
description: Enumera las versiones de los servicios de integración de Linux para las distribuciones admitidas y Red Hat Enterprise
ms.topic: article
ms.assetid: 4bf8783d-dee5-4b3e-8cce-2b11b117c189
author: danihalfin
ms.author: vichen
ms.date: 04/06/2020
ms.openlocfilehash: acccb41bca9ffc30267fbb49cbf765286c6d8f81
ms.sourcegitcommit: 68444968565667f86ee0586ed4c43da4ab24aaed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87989322"
---
# <a name="supported-centos-and-red-hat-enterprise-linux-virtual-machines-on-hyper-v"></a>Compatibilidad con máquinas virtuales de alta y Red Hat Enterprise Linux en Hyper-V

>Se aplica a: Windows Server 2019, Hyper-V Server 2019, Windows Server 2016, Hyper-V Server 2016, Windows Server 2012 R2, Hyper-V Server 2012 R2, Windows 10, Windows 8.1

Los siguientes mapas de distribución de características indican las características que se encuentran en las versiones integradas y descargables de Linux Integration Services. Los problemas conocidos y las soluciones alternativas para cada distribución se muestran después de las tablas.

Los controladores de Integration Services de Red Hat Enterprise Linux integrados para Hyper-V (disponible desde Red Hat Enterprise Linux 6,4) son suficientes para que los invitados de Red Hat Enterprise Linux ejecuten con dispositivos sintéticos de alto rendimiento en hosts de Hyper-V. Estos controladores integrados están certificados por Red Hat para este uso. Las configuraciones certificadas se pueden ver en esta página web de Red Hat: [Catálogo de certificados de Red Hat](https://access.redhat.com/ecosystem/search/#/ecosystem/Red%20Hat%20Enterprise%20Linux?sort=sortTitle%20asc&vendors=Microsoft&category=Server). No es necesario descargar e instalar los paquetes de Integration Services Linux desde el centro de descarga de Microsoft y, si lo hace, puede limitar su compatibilidad con Red Hat, tal como se describe en el artículo 1067 de Red Hat Knowledgebase: [Red Hat knowledgebase 1067](https://access.redhat.com/articles/1067).

Debido a posibles conflictos entre la compatibilidad con LIS integrada y la compatibilidad con LIS descargable al actualizar el kernel, deshabilite las actualizaciones automáticas, desinstale los paquetes descargables de LIS, actualice el kernel, reinicie y, a continuación, instale la versión de LIS más reciente y vuelva a iniciarlo.

> [!NOTE]
> La información de certificación oficial Red Hat Enterprise Linux está disponible a través del [portal de clientes de Red Hat](https://access.redhat.com/ecosystem/search/#/category/Server?sort=sortTitle%20asc&query=windows%20server&ecosystem=Red%20Hat%20Enterprise%20Linux).

En esta sección:

* [RHEL/7 serie 8. x](#rhelcentos-8x-series)

* [RHEL/la serie 7. x](#rhelcentos-7x-series)

* [RHEL/la serie 6. x](#rhelcentos-6x-series)

* [RHEL/la serie 5. x](#rhelcentos-5x-series)

* [Notas](#notes)

## <a name="table-legend"></a>Leyenda de tabla

* La **compilación en** LIS se incluye como parte de esta distribución de Linux. Los números de versión del módulo de kernel para el LIS integrado (como se muestra en **lsmod**, por ejemplo) son diferentes del número de versión del paquete de descarga de lis proporcionado por Microsoft. Un error de coincidencia no indica que el LIS integrado no está actualizado.

* &#10004;: característica disponible

* (*en blanco*): característica no disponible

## <a name="rhelcentos-8x-series"></a>RHEL/7 serie 8. x

|       **Característica**     |       **Versión de Windows Server**      |       **8.1**     |       **8.0**     |
|-----------------------|---------------------------------------|-------------------|-------------------|
|       **Disponibilidad**        |   |   |
|       **[Principal](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#core)**      | 2019, 2016, 2012 R2 | &#10004; | &#10004;
|       Windows Server 2016 hora precisa       | 2019, 2016 | &#10004; | &#10004;
|       **[Redes](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#networking)**      |   |  |
|       Tramas gigantes        | 2019, 2016, 2012 R2 | &#10004; | &#10004;|
|       Etiquetado y Troncalización de VLAN       | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       Migración en vivo      | 2019, 2016, 2012 R2 | &#10004; | &#10004;|
|       Inyección de IP estática     |  2019, 2016, 2012 R2 | &#10004; Nota 2 | &#10004; Nota 2|
|       vRSS     | 2019, 2016, 2012 R2 | &#10004; | &#10004;|
|       Segmentación y descarga de sumas de comprobación TCP | 2019, 2016, 2012 R2 | &#10004;|  &#10004; |
|       SR-IOV  | 2019, 2016 |  &#10004;   | &#10004; |
|       **[Storage](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#storage)** |  |  |
|       Cambiar el tamaño de VHDX  | 2019, 2016, 2012 R2 | &#10004; | &#10004; |
|       Canal de fibra virtual | 2019, 2016, 2012 R2 | &#10004; Nota 3  | &#10004; Nota 3 |
|       Copia de seguridad de máquinas virtuales en vivo  | 2019, 2016, 2012 R2 | Nota &#10004; 5 | Nota &#10004; 5|
|       Compatibilidad con TRIM | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       WWN SCSI | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       **[Memory](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#memory)** | |  |
|       Compatibilidad con el kernel PAE  | 2019, 2016, 2012 R2 |  N/D | N/D
|       Configuración de la brecha de MMIO  | 2019, 2016, 2012 R2 | &#10004; | &#10004;  |
|       Memoria dinámica: agregar en caliente | 2019, 2016, 2012 R2  | &#10004; Nota 8, 9, 10 | &#10004; Nota 8, 9, 10 |
|       Memoria dinámica: globos | 2019, 2016, 2012 R2 | &#10004; Nota 8, 9, 10 | &#10004; Nota 8, 9, 10 |
|       Tamaño de memoria en tiempo de ejecución | 2019, 2016  | &#10004;  | &#10004; |
|       **[Cámara](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#video)** | | |
|       Dispositivo de vídeo específico de Hyper-V | 2019, 2016, 2012 R2 | &#10004;   | &#10004; |
|       **[Varios](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#miscellaneous)** | | |
|       Par clave-valor  | 2019, 2016, 2012 R2 | &#10004;   | &#10004;  |
|       Interrupción no enmascarable | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       Copia de archivos de host a invitado | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       comando lsvmbus | 2019, 2016, 2012 R2 | &#10004;  | &#10004; |
|       Sockets de Hyper-V | 2019, 2016 | &#10004;  | &#10004; |
|       Acceso directo/DDA de PCI | 2019, 2016 | &#10004; | &#10004; |
| **[Máquinas virtuales de generación 2](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#generation-2-virtual-machines)** | |  |
|       Arranque mediante UEFI | 2019, 2016, 2012 R2 |  Nota &#10004; 14  | Nota &#10004; 14
|       Arranque seguro | 2019, 2016 |  &#10004; |  &#10004; |


## <a name="rhelcentos-7x-series"></a>RHEL/la serie 7. x

Esta serie solo tiene kernels de 64 bits.


|                                                                 **Característica**                                                                  |     **Versión de Windows Server**     |                             **7,5-7.8**                             |                             **7.3-7.4**                             |                             **7.0-7.2**                             |     **7,5-7.8**     |       **7.4**       |       **7.3**       |       **7.2**       |       **7.1**       |        **7.0**         |
|----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|---------------------------------------------------------------------|---------------------------------------------------------------------|---------------------------------------------------------------------|---------------------|---------------------|---------------------|---------------------|---------------------|------------------------|
|                                                               **Disponibilidad**                                                               |                                    | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) |      Integrado       |      Integrado       |      Integrado       |      Integrado       |      Integrado       |        Integrado        |
|                          **[Principal](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#core)**                          | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                      Windows Server 2016 hora precisa                                                       |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                                                                     |                     |                     |                     |                     |                     |                        |
|                    **[Redes](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#networking)**                    |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                                 Tramas gigantes                                                                 | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                          Etiquetado y Troncalización de VLAN                                                           | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                                Migración en vivo                                                                | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                             Inyección de IP estática                                                              |     2019, 2016, 2012 R2      |                           &#10004; Nota 2                           |                           &#10004; Nota 2                           |                           &#10004; Nota 2                           |   &#10004; Nota 2   |   &#10004; Nota 2   |   &#10004; Nota 2   |   &#10004; Nota 2   |   &#10004; Nota 2   |    &#10004; Nota 2     |
|                                                                     vRSS                                                                     |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |                        |
|                                                    Segmentación y descarga de sumas de comprobación TCP                                                    | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |                        |
|                                                                    SR-IOV                                                                    |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                                                                     |      &#10004;       |      &#10004;       |      &#10004;       |                     |                     |                        |
|                       **[Storage](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#storage)**                       |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                                 Cambiar el tamaño de VHDX                                                                  |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |                     |                        |
|                                                            Canal de fibra virtual                                                             |        2019, 2016, 2012 R2         |                           &#10004; Nota 3                           |                           &#10004; Nota 3                           |                           &#10004; Nota 3                           |   &#10004; Nota 3   |   &#10004; Nota 3   |   &#10004; Nota 3   |   &#10004; Nota 3   |   &#10004; Nota 3   |    &#10004; Nota 3     |
|                                                         Copia de seguridad de máquinas virtuales en vivo                                                          |        2019, 2016, 2012 R2         |                           Nota &#10004; 5                           |                           Nota &#10004; 5                           |                           Nota &#10004; 5                           |  &#10004; Nota 4, 5  | &#10004; Nota 4, 5  | &#10004; Nota 4, 5  | &#10004; Nota 4, 5  | &#10004; Nota 4, 5  |   &#10004; Nota 4, 5   |
|                                                                 Compatibilidad con TRIM                                                                 |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |                     |                        |
|                                                                   WWN SCSI                                                                   |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |                     |                     |                     |                     |                        |
|                        **[Memory](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#memory)**                        |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                              Compatibilidad con el kernel PAE                                                              | 2019, 2016, 2012 R2 |                                 N/D                                 |                                 N/D                                 |                                 N/D                                 |         N/D         |         N/D         |         N/D         |         N/D         |         N/D         |          N/D           |
|                                                          Configuración de la brecha de MMIO                                                           |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                           Memoria dinámica: agregar en caliente                                                           |     2019, 2016, 2012 R2      |                       &#10004; Nota 8, 9, 10                        |                       &#10004; Nota 8, 9, 10                        |                       &#10004; Nota 8, 9, 10                        | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 8, 9, 10 |
|                                                         Memoria dinámica: globos                                                          |     2019, 2016, 2012 R2      |                       &#10004; Nota 8, 9, 10                        |                       &#10004; Nota 8, 9, 10                        |                       &#10004; Nota 8, 9, 10                        | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 9, 10 | &#10004; Nota 8, 9, 10 |
|                                                            Tamaño de memoria en tiempo de ejecución                                                             |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |                     |                     |                     |                     |                     |                        |
|                         **[Cámara](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#video)**                         |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                        Dispositivo de vídeo específico de Hyper-V                                                         | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                 **[Varios](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#miscellaneous)**                 |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                                Par clave-valor                                                                | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                            Interrupción no enmascarable                                                            |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |
|                                                         Copia de archivos de host a invitado                                                         |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |                        |
|                                                               comando lsvmbus                                                                | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |                     |                     |                     |                     |                     |                        |
|                                                               Sockets de Hyper-V                                                                |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |                     |                     |                     |                     |                     |                        |
|                                                             Acceso directo/DDA de PCI                                                              |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                                                                     |      &#10004;       |      &#10004;       |      &#10004;       |                     |                     |                        |
| **[Máquinas virtuales de generación 2](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#generation-2-virtual-machines)** |                                    |                                                                     |                                                                     |                                                                     |                     |                     |                     |                     |                     |                        |
|                                                               Arranque mediante UEFI                                                                |        2019, 2016, 2012 R2         |                          Nota &#10004; 14                           |                          Nota &#10004; 14                           |                          Nota &#10004; 14                           |  Nota &#10004; 14   |  Nota &#10004; 14   |  Nota &#10004; 14   |  Nota &#10004; 14   |  Nota &#10004; 14   |    Nota &#10004; 14    |
|                                                                 Arranque seguro                                                                  |             2019, 2016             |                              &#10004;                               |                              &#10004;                               |                              &#10004;                               |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |      &#10004;       |        &#10004;        |


## <a name="rhelcentos-6x-series"></a>RHEL/la serie 6. x

El kernel de 32 bits para esta serie es PAE habilitado. No hay compatibilidad integrada con LIS para RHEL/la funcionalidad 6.0-6.3.

|  **Característica**  | **Versión de Windows Server** |  **6.7-6.10** |  **6.4-6.6** | **6.0-6.3** |   **6,10, 6,9, 6,8**   |       **6,6, 6,7**        |          **6,5**          |          **6.4**           |
|---------------|----------------------------|---------------|--------------|-------------|------------------------|---------------------------|----------------------------|---------------------------|
|  **Disponibilidad** |   | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) |        Integrado        |         Integrado          |         Integrado          |          Integrado          |
|  **[Principal](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#core)** | 2019, 2016, 2012 R2 |  &#10004; | &#10004;  | &#10004;  | &#10004; | &#10004; | &#10004;| &#10004; |
|  Windows Server 2016 hora precisa | 2019, 2016 | |  | |  |  |   |   |
|  **[Redes](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#networking)**  | |   |  | |  |  |   |  |
|  Tramas gigantes | 2019, 2016, 2012 R2 | &#10004; |  &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
|  Etiquetado y Troncalización de VLAN | 2019, 2016, 2012 R2 | &#10004; Nota 1 | &#10004; Nota 1 | &#10004; Nota 1 | &#10004; Nota 1 | &#10004; Nota 1|  &#10004; Nota 1 |&#10004; Nota 1 |
|  Migración en vivo | 2019, 2016, 2012 R2 | &#10004; | &#10004; | &#10004;| &#10004; | &#10004; | &#10004;  | &#10004; |
|  Inyección de IP estática |  2019, 2016, 2012 R2 | &#10004; Nota 2 |  &#10004; Nota 2  | &#10004; Nota 2 | &#10004; Nota 2 | &#10004; Nota 2 | &#10004; Nota 2  | &#10004; Nota 2 |
|  vRSS  | 2019, 2016, 2012 R2 | &#10004; | &#10004; |  &#10004; | &#10004; | &#10004;  |   |   |
|  Segmentación y descarga de sumas de comprobación TCP | 2019, 2016, 2012 R2 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004;  |   |    |
|  SR-IOV   | 2019, 2016 |    |  |   |   |   |   |  |
|  **[Storage](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#storage)**  |  |   |   |  | |  |  | |
|  Cambiar el tamaño de VHDX | 2019, 2016, 2012 R2| &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |  |
|  Canal de fibra virtual  | 2019, 2016, 2012 R2 |  &#10004; Nota 3  | &#10004; Nota 3  | &#10004; Nota 3  | &#10004; Nota 3 | &#10004; Nota 3  | &#10004; Nota 3  |    |
|  Copia de seguridad de máquinas virtuales en vivo | 2019, 2016, 2012 R2 | Nota &#10004; 5  | Nota &#10004; 5  | Nota &#10004; 5 | &#10004; Nota 4, 5 | &#10004; Nota 4, 5 | &#10004; Nota 4, 5, 6 | &#10004; Nota 4, 5, 6 |
|  Compatibilidad con TRIM  | 2019, 2016, 2012 R2  | &#10004; | &#10004; | &#10004; | &#10004; |  |  |  |
|  WWN SCSI  | 2019, 2016, 2012 R2  | &#10004; | &#10004;  | &#10004;  |  |   |  |  |
|  **[Memory](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#memory)** | |  | | |  | |  |  |
|  Compatibilidad con el kernel PAE | 2019, 2016, 2012 R2 | &#10004;  | &#10004;  | &#10004; | &#10004; |  &#10004;  |  &#10004; |  &#10004; |
|  Configuración de la brecha de MMIO  | 2019, 2016, 2012 R2 | &#10004;  | &#10004;  | &#10004;  |  &#10004;  | &#10004;  |  &#10004; |  &#10004; |
|  Memoria dinámica: agregar en caliente | 2019, 2016, 2012 R2 |  &#10004; Nota 7, 9, 10  | &#10004; Nota 7, 9, 10 | &#10004; Nota 7, 9, 10 | &#10004; Nota 7, 9, 10 | &#10004; Nota 7, 8, 9, 10 | &#10004; Nota 7, 8, 9, 10 | |
|  Memoria dinámica: globos | 2019, 2016, 2012 R2 | &#10004; Nota 7, 9, 10  | &#10004; Nota 7, 9, 10  | &#10004; Nota 7, 9, 10 | &#10004; Nota 7, 9, 10 |  &#10004; Nota 7, 9, 10   |  &#10004; Nota 7, 9, 10   | &#10004; Nota 7, 9, 10, 11 |
| Tamaño de memoria en tiempo de ejecución | 2019, 2016  |  |   |  |  | |  |  |
| **[Cámara](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#video)** || | | |  |  |  | |
| Dispositivo de vídeo específico de Hyper-V | 2019, 2016, 2012 R2 | &#10004;  | &#10004;  | &#10004;  | &#10004; | &#10004; | &#10004; | |
| **[Varios](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#miscellaneous)** |  |  |  |   |  | |  |  |
| Par clave-valor | 2019, 2016, 2012 R2 | &#10004; | &#10004;| &#10004; | &#10004; Nota 12 | &#10004; Nota 12 | &#10004; Nota 12, 13 | &#10004; Nota 12, 13 |
| Interrupción no enmascarable | 2019, 2016, 2012 R2 | &#10004;  | &#10004;  | &#10004; | &#10004; | &#10004;  |  &#10004;| &#10004; |
| Copia de archivos de host a invitado | 2019, 2016, 2012 R2 | &#10004;  |  &#10004; | &#10004; | &#10004; | &#10004; | |  |
| comando lsvmbus | 2019, 2016, 2012 R2 |  &#10004; |  &#10004;  |  &#10004; |   |   |    |  |
| Sockets de Hyper-V | 2019, 2016  | &#10004;  |  &#10004;  |  &#10004; |  |   |   |  |
| Acceso directo/DDA de PCI | 2019, 2016 | &#10004;  | |   |  |  | |   |
| **[Máquinas virtuales de generación 2](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#generation-2-virtual-machines)** | |  | | | | | | |
| Arranque mediante UEFI  | 2012 R2 |  |  |  |  |  | |
|  |2019, 2016 | Nota &#10004; 14 | Nota &#10004; 14| Nota &#10004; 14 |    Nota &#10004; 14    |  | |  |
|Arranque seguro| 2019, 2016|  ||  |  |  | ||



## <a name="rhelcentos-5x-series"></a>RHEL/la serie 5. x

Esta serie tiene disponible un kernel PAE de 32 bits compatible. No hay compatibilidad integrada con LIS para RHEL/acalta antes 5,9.


|                                                                 **Característica**                                                                  |     **Versión de Windows Server**     |                              5,2-5,11                              |                            **5.2-5.11**                             |    **5,9-5,11**     |
|----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|---------------------------------------------------------------------|---------------------------------------------------------------------|-----------------------|
|                                                               **Disponibilidad**                                                               |                                    | [LIS 4,3](https://www.microsoft.com/download/details.aspx?id=55106) | [LIS 4,1](https://www.microsoft.com/download/details.aspx?id=51612) |       Integrado        |
|                          **[Principal](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#core)**                          | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                      Windows Server 2016 hora precisa                                                       |             2019, 2016             |                                                                     |                                                                     |                       |
|                    **[Redes](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#networking)**                    |                                    |                                                                     |                                                                     |                       |
|                                                                 Tramas gigantes                                                                 | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                          Etiquetado y Troncalización de VLAN                                                           | 2019, 2016, 2012 R2 |                           &#10004; Nota 1                           |                           &#10004; Nota 1                           |    &#10004; Nota 1    |
|                                                                Migración en vivo                                                                | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                             Inyección de IP estática                                                              |     2019, 2016, 2012 R2      |                           &#10004; Nota 2                           |                           &#10004; Nota 2                           |    &#10004; Nota 2    |
|                                                                     vRSS                                                                     |        2019, 2016, 2012 R2         |                                                                     |                                                                     |                       |
|                                                    Segmentación y descarga de sumas de comprobación TCP                                                    | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                       |
|                                                                    SR-IOV                                                                    |             2019, 2016             |                                                                     |                                                                     |                       |
|                       **[Storage](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#storage)**                       |                                    |                                                                     |                                                                     |                       |
|                                                                 Cambiar el tamaño de VHDX                                                                  |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                       |
|                                                            Canal de fibra virtual                                                             |        2019, 2016, 2012 R2         |                           &#10004; Nota 3                           |                           &#10004; Nota 3                           |                       |
|                                                         Copia de seguridad de máquinas virtuales en vivo                                                          |        2019, 2016, 2012 R2         |                         Nota &#10004; 5, 15                         |                           Nota &#10004; 5                           | &#10004; Nota 4, 5, 6 |
|                                                                 Compatibilidad con TRIM                                                                 |        2019, 2016, 2012 R2         |                                                                     |                                                                     |                       |
|                                                                   WWN SCSI                                                                   |        2019, 2016, 2012 R2         |                                                                     |                                                                     |                       |
|                        **[Memory](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#memory)**                        |                                    |                                                                     |                                                                     |                       |
|                                                              Compatibilidad con el kernel PAE                                                              | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                          Configuración de la brecha de MMIO                                                           |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                           Memoria dinámica: agregar en caliente                                                           |     2019, 2016, 2012 R2      |                                                                     |                                                                     |                       |
|                                                         Memoria dinámica: globos                                                          |     2019, 2016, 2012 R2      |                     &#10004; Nota 7, 9, 10, 11                      |                     &#10004; Nota 7, 9, 10, 11                      |                       |
|                                                            Tamaño de memoria en tiempo de ejecución                                                             |             2019, 2016             |                                                                     |                                                                     |                       |
|                         **[Cámara](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#video)**                         |                                    |                                                                     |                                                                     |                       |
|                                                        Dispositivo de vídeo específico de Hyper-V                                                         | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                       |
|                 **[Varios](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#miscellaneous)**                 |                                    |                                                                     |                                                                     |                       |
|                                                                Par clave-valor                                                                | 2019, 2016, 2012 R2 |                              &#10004;                               |                              &#10004;                               |                       |
|                                                            Interrupción no enmascarable                                                            |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |       &#10004;        |
|                                                         Copia de archivos de host a invitado                                                         |        2019, 2016, 2012 R2         |                              &#10004;                               |                              &#10004;                               |                       |
|                                                               comando lsvmbus                                                                | 2019, 2016, 2012 R2 |                                                                     |                                                                     |                       |
|                                                               Sockets de Hyper-V                                                                |             2019, 2016             |                                                                     |                                                                     |                       |
|                                                             Acceso directo/DDA de PCI                                                              |             2019, 2016             |                                                                     |                                                                     |                       |
| **[Máquinas virtuales de generación 2](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md#generation-2-virtual-machines)** |                                    |                                                                     |                                                                     |                       |
|                                                               Arranque mediante UEFI                                                                |        2019, 2016, 2012 R2         |                                                                     |                                                                     |                       |
|                                                                 Arranque seguro                                                                  |             2019, 2016             |                                                                     |                                                                     |                       |

## <a name="notes"></a>Notas

1. Para esta versión de RHEL/versión, el etiquetado de VLAN funciona pero no la Troncalización de VLAN.

2. Es posible que la inyección de direcciones IP estáticas no funcione si se ha configurado el administrador de red para un adaptador de red sintético determinado en la máquina virtual. Para un funcionamiento sin problemas de la inyección de direcciones IP estáticas, asegúrese de que el administrador de red esté desactivado completamente o se haya desactivado para un adaptador de red específico a través de su archivo ifcfg-ethX.

3. En Windows Server 2012 R2 al usar dispositivos de canal de fibra virtual, asegúrese de que se ha rellenado el número de unidad lógica 0 (LUN 0). Si LUN 0 no se ha rellenado, es posible que una máquina virtual de Linux no pueda montar los dispositivos de canal de fibra de forma nativa.

4. En el caso de LIS integrado, debe instalarse el paquete de "los demonios de HyperV" para esta funcionalidad.

5. Si hay identificadores de archivo abiertos durante una operación de copia de seguridad de una máquina virtual activa, en algunos casos, los VHD de copia de seguridad podrían tener que someterse a una comprobación de coherencia del sistema de archivos (fsck) en la restauración. Las operaciones de copia de seguridad en directo pueden producir errores silenciosamente si la máquina virtual tiene un dispositivo iSCSI conectado o un almacenamiento conectado directamente (también conocido como disco de acceso directo).

6. Aunque se prefiere la descarga de Linux Integration Services, la compatibilidad con la copia de seguridad en vivo para RHEL/la versión 5,9-5.11/6.4/6.5 también está disponible a través [de los fundamentos de copia de seguridad de Hyper-V para Linux](https://github.com/LIS/backupessentials/tree/1.0).

7. La compatibilidad con memoria dinámica solo está disponible en las máquinas virtuales de 64 bits.

8. La compatibilidad con la adición en caliente no está habilitada de forma predeterminada en esta distribución. Para habilitar la compatibilidad con la adición en caliente, debe agregar una regla de udev en/etc/udev/rules.d/como se indica a continuación:

   1. Cree un archivo **/etc/udev/rules.d/100-Balloon.rules**. Puede usar cualquier otro nombre que desee para el archivo.

   2. Agregue el siguiente contenido al archivo:`SUBSYSTEM=="memory", ACTION=="add", ATTR{state}="online"`

   3. Reinicie el sistema para habilitar la compatibilidad con la adición en caliente.

   Mientras que la descarga de Linux Integration Services crea esta regla en la instalación, la regla también se quita cuando se desinstala LIS, por lo que la regla debe volver a crearse si se necesita memoria dinámica después de la desinstalación.

9. Se puede producir un error en las operaciones de memoria dinámica si el sistema operativo invitado se está ejecutando demasiado bajo en la memoria. A continuación se indican algunas prácticas recomendadas:

   * La memoria de inicio y la memoria mínima deben ser iguales o mayores que la cantidad de memoria que el proveedor de distribución recomienda.

   * Las aplicaciones que tienden a consumir toda la memoria disponible en un sistema se limitan a consumir hasta el 80 por ciento de la RAM disponible.

10. Si utiliza Memoria dinámica en un sistema operativo Windows Server 2016 o Windows Server 2012 R2, especifique la **memoria de inicio**, la **memoria mínima**y los parámetros de **memoria máxima** en múltiplos de 128 megabytes (MB). Si no lo hace, pueden producirse errores de adición en caliente y es posible que no vea ningún aumento de la memoria en un sistema operativo invitado.

11. Ciertas distribuciones, incluidas las que usan LIS 4,0 y 4,1, solo ofrecen soporte técnico y no proporcionan soporte técnico para agregarlos en caliente. En este escenario, se puede usar la característica de memoria dinámica si se establece el parámetro de memoria de inicio en un valor que es igual al parámetro de memoria máxima. Esto hace que toda la memoria necesaria se agregue en caliente a la máquina virtual en el momento del arranque y, posteriormente, en función de los requisitos de memoria del host, Hyper-V puede asignar o desasignar libremente la memoria del invitado mediante el uso de globos. Configure la **memoria de inicio** y la **memoria mínima** en o por encima del valor recomendado para la distribución.

12. Para habilitar la infraestructura de pares clave-valor (KVP), instale el paquete RPM de hypervkvpd o HyperV-daemons desde su ISO de RHEL. También se puede instalar el paquete directamente desde repositorios RHEL.

13. Es posible que la infraestructura de pares clave-valor (KVP) no funcione correctamente sin una actualización de software de Linux. Póngase en contacto con el proveedor de distribución para obtener la actualización de software en caso de que vea problemas con esta característica.

14. En las máquinas virtuales con Windows Server 2012 R2 de segunda generación 2, el arranque seguro está habilitado de forma predeterminada y algunas máquinas virtuales Linux no se iniciarán a menos que se deshabilite la opción de arranque seguro. Puede deshabilitar el arranque seguro en la sección **firmware** de la configuración de la máquina virtual en el **Administrador de Hyper-V** o puede deshabilitarla mediante PowerShell:

    ```Powershell
    Set-VMFirmware -VMName "VMname" -EnableSecureBoot Off
    ```

    La descarga de Integration Services de Linux se puede aplicar a las máquinas virtuales de generación 2 existentes, pero no a la capacidad de generación 2.

15. En Red Hat Enterprise Linux o de la 5,2, 5,3 y 5,4, la funcionalidad de inmovilización del sistema de archivos no está disponible, por lo que la copia de seguridad de máquinas virtuales en directo tampoco está disponible.

Consulte también

* [Set-VMFirmware](/powershell/module/hyper-v/set-vmfirmware?view=win10-ps)

* [Máquinas virtuales Debian admitidas en Hyper-V](Supported-Debian-virtual-machines-on-Hyper-V.md)

* [Oracle Linux compatibles con máquinas virtuales en Hyper-V](Supported-Oracle-Linux-virtual-machines-on-Hyper-V.md)

* [Máquinas virtuales de SUSE compatibles en Hyper-V](Supported-SUSE-virtual-machines-on-Hyper-V.md)

* [Máquinas virtuales de Ubuntu admitidas en Hyper-V](Supported-Ubuntu-virtual-machines-on-Hyper-V.md)

* [Máquinas virtuales de FreeBSD compatibles en Hyper-V](Supported-FreeBSD-virtual-machines-on-Hyper-V.md)

* [Descripciones de características de máquinas virtuales Linux y FreeBSD en Hyper-V](Feature-Descriptions-for-Linux-and-FreeBSD-virtual-machines-on-Hyper-V.md)

* [Prácticas recomendadas para ejecutar Linux en Hyper-V](Best-Practices-for-running-Linux-on-Hyper-V.md)

* [Certificación de hardware de Red Hat](https://hardware.redhat.com/&quicksearch=Microsoft)