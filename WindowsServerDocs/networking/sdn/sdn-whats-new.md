---
title: Novedades de SDN para Windows Server
description: En este tema se proporciona información sobre las nuevas características de redes definidas por software para Windows Server 1709
manager: grcusanz
ms.topic: get-started-article
ms.assetid: efad919b-e9e7-4a0c-b373-e68a092f93b5
ms.author: anpaul
author: AnirbanPaul
ms.date: 10/02/2018
ms.openlocfilehash: bcf4923ec25aba66484ec384c8895d877aba0069
ms.sourcegitcommit: dfa48f77b751dbc34409aced628eb2f17c912f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/07/2020
ms.locfileid: "87962149"
---
# <a name="whats-new-in-sdn-for-windows-server-2019"></a>Novedades de SDN para Windows Server 2019

>Se aplica a: Windows Server (Canal semianual)


|                         **Característica**                          |                                                                                                                                                                                         **Descripción**                                                                                                                                                                                         | **Nueva/actualizada** |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| [Redes cifradas](vnet-encryption/sdn-vnet-encryption.md) | El cifrado de red virtual permite el cifrado del tráfico de red virtual entre máquinas virtuales que se comunican entre sí dentro de subredes marcadas como "cifrado habilitado". También utiliza la Seguridad de la capa de transporte de datagrama (DTLS) en la subred virtual para cifrar los paquetes. DTLS protege frente a las interceptaciones, alteraciones y falsificaciones realizadas por cualquier persona con acceso a la red física. |       Nuevo       |
|    [Auditoría de Firewall](security/sdn-firewall-auditing.md)    |                                                                                            La auditoría de Firewall es una nueva funcionalidad para el Firewall de SDN en Windows Server 2019. Al habilitar el Firewall de SDN, se registra cualquier flujo procesado por las reglas de Firewall de SDN (ACL) que tienen habilitado el registro.                                                                                            |       Nuevo       |
| [Emparejamiento de redes virtuales](vnet-peering/sdn-vnet-peering.md)  |                                                                                                                      El emparejamiento de redes virtuales permite conectar dos redes virtuales sin problemas. Una vez emparejadas, para fines de conectividad, las redes virtuales aparecen como una sola.                                                                                                                      |       Nuevo       |
|           [Medición de salida](manage/sdn-egress.md)            |                  Esta nueva característica de Windows Server 2019 permite a SDN ofrecer medidores de uso para las transferencias de datos de salida. Con esta característica agregada, la controladora de red mantiene una lista de permitidos por Virtual Network de todos los intervalos de direcciones IP que se usan en SDN y tiene en cuenta que cualquier paquete enlazado a un destino que no esté incluido en uno de estos intervalos para facturar las transferencias de datos de salida.                   |       Nuevo       |

---



