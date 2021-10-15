---
title: Administración de activos de centros de datos
description: Información general sobre la administración de activos del centro de datos de Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fafba29a25c5b01fa37d091fb210185a98365192
ms.sourcegitcommit: b228be59e13ae2e05ba85f65c1d4648fef5e9260
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2021
ms.locfileid: "60356393"
---
# <a name="datacenter-asset-management"></a>Administración de activos de centros de datos

Los centros de datos de Microsoft están hechos de varios componentes físicos y virtuales, cada uno de los cuales se conoce como un activo. El grupo de ingeniería operaciones e innovación en la nube de Microsoft (CO+I) sigue procesos estandarizados seguros para la implementación, el seguimiento y el desmantelamiento de activos físicos y virtuales.

## <a name="supply-chain-integrity"></a>Integridad de la cadena de suministro

La protección de activos comienza por proteger la cadena de suministro. Microsoft se compromete a mantener la integridad de la cadena de suministro y la seguridad de la cadena de suministro de un extremo a otro. Los proveedores siguen estrictos procedimientos de cadena de custodia al transportar nuestros componentes de nube para reducir el riesgo de alteración y manipulación. Todo el material entrante y saliente es cuidadosamente inspeccionado y supervisado para garantizar la integridad de los componentes y el firmware.

Normalmente, las entregas de componentes del sistema de información a centros de datos de Microsoft se programan. En el caso de las entregas no programadas, Microsoft inspecciona exhaustivamente y garantiza que están aprobadas para su entrada en una sala de equipos de Microsoft antes de la entrada física. Cuando un componente del sistema de información entra en el edificio, el equipo de administración de activos compara el elemento recibido con el vale al que se hace referencia y examina el dispositivo en la herramienta de administración de activos. Todos los componentes del sistema de información recibidos o enviados son rastreados por la herramienta de vales de flujo de trabajo y en los registros de envío de la herramienta de administración de activos. Se prohíbe a los visitantes usar portátiles personales y teléfonos móviles (excepto para llamadas de emergencia y tomar notas), aunque se les permite en el entorno de producción (colocaciones). Está prohibido conectar teléfonos móviles a un dispositivo o tomar fotos por directiva de centro de datos. Si el equipo que entra en el centro de datos se usa con fines de mantenimiento, el equipo requiere la aprobación de administración de centros de datos en el sistema de herramientas de acceso a centros de datos.

## <a name="asset-inventory"></a>Inventario de activos

Microsoft requiere que todos los recursos del centro de datos se contabilicen y tengan un propietario designado. Los propietarios son responsables de mantener la información actualizada para sus activos físicos y virtuales. Cuando se agregan nuevos recursos físicos a un centro de datos, se firman, examinan, etiquetan de forma única y se registran en los sistemas de control de inventario. Las herramientas de supervisión automatizadas facilitan el seguimiento de los activos físicos y virtuales.

## <a name="asset-maintenance"></a>Mantenimiento de activos

Microsoft tiene dos equipos que proporcionan diferentes tipos de mantenimiento de activos: el entorno crítico (CE) y los equipos de servicios de sitio. El equipo de CE proporciona administración de instalaciones para sistemas eléctricos, mecánicos y físicos que componen la infraestructura operativa de la instalación. También programan, realizan, documentan y revisan todas las actividades de mantenimiento realizadas en componentes CE. Los centros de datos de Microsoft dependen de un sistema de administración de mantenimiento computarizado para administrar las programaciones de mantenimiento y las órdenes de trabajo. El equipo de Servicios de sitio proporciona servicios a todos los activos de servicio en línea de Microsoft ubicados en los centros de datos de Microsoft. Además, el equipo de Servicios de sitio proporciona soporte técnico local y servicio de corrección de interrupción para los activos pertenecientes a los servicios de aprovisionamiento de propiedades desde el centro de datos.

## <a name="asset-classification"></a>Clasificación de activos

Los activos de Microsoft , incluidos los datos, se clasifican de acuerdo con Enterprise directrices de taxonomía de datos. Estas directrices promueven la normalización en toda la empresa y se revisan y actualizan anualmente. Los estándares de clasificación de activos y protección de activos describen los procedimientos de seguridad que los empleados deben seguir al interactuar con cada activo. Los clientes se consideran propietarios de sus datos almacenados en el entorno de nube de Microsoft. Los recursos de datos clasificados como contenido del cliente o datos del cliente están protegidos por los procedimientos de seguridad aplicables.

Microsoft considera que toda la documentación se categoriza como un activo del sistema. El equipo de Servicios de sitio es responsable de clasificar sus activos y emplear las medidas de seguridad asociadas de acuerdo con los estándares de clasificación de activos y protección de activos, así como los requisitos adicionales definidos por el equipo de servicio.

Los propietarios de activos deben asignar a sus activos una clasificación de activos, sin excepción. En entornos de centros de datos de Microsoft, los activos se refieren a servidores y dispositivos de red. Otros medios digitales como unidades flash USB, discos duros externos o CD/DVD no se usan para la operación de servicios. Los medios no digitales no se usan en centros de datos.

## <a name="media-storage"></a>Almacenamiento multimedia

Los activos de medios digitales de Microsoft se almacenan de forma física y segura en salas de colocación de centros de datos de Microsoft. Existen varias capas de controles de acceso físico y videovigilancia para proteger y supervisar estos activos. Cuando los activos multimedia digitales llegan al final de su ciclo de vida, se borran, purgan o se destruyen mediante métodos coherentes con NIST SP 800-88 antes de su eliminación. El [artículo de destrucción de dispositivos portadores de datos](assurance-data-bearing-device-destruction.md) trata el proceso de eliminación segura de activos.

## <a name="media-transport"></a>Transporte multimedia

Microsoft restringe las actividades de transporte de activos al personal autorizado mediante protecciones de cadena de custodia. El uso de bloqueos, sellados a prueba de manipulaciones y validación necesaria del inventario de activos garantiza que solo el personal autorizado participe en el transporte de activos.

Todos los medios que se transportan desde centros de datos de Microsoft requieren un seguimiento preciso. Microsoft se ha contratado con varios proveedores aprobados para proporcionar servicios de envío seguro. El transporte seguro comienza con un inventario preciso y una cadena de custodia. En la ubicación de entrega, el personal aprobado de la compañía de transporte debe presenciar la eliminación del sello a prueba de manipulaciones y el desbloqueo del contenedor. El personal de recepción realiza un inventario del envío y envía un mensaje que confirma la recepción de los activos. Microsoft también tiene contratos con un proveedor para proporcionar la destrucción de equipos. Según la clasificación de activos, es necesario destruir algunos equipos en el sitio.

El transporte de medios digitales de Microsoft fuera del espacio controlado por seguridad requiere la supervisión de dos miembros del equipo operaciones del centro de datos. Los activos se acompañan y supervisan continuamente por el personal autorizado hasta que se destruyen.

El equipo de administración de centros de datos controla la entrega y eliminación de componentes del sistema de información a través de los vales que se rastrean en la herramienta de vales. Los propietarios del sistema autorizan la entrega y eliminación de componentes del sistema de información.

## <a name="asset-retention"></a>Retención de activos

Los activos propiedad de Microsoft se conservan según corresponda en función de los requisitos de retención establecidos por Corporate Records Management, la clasificación de activos o los requisitos contractuales. Para obtener más información acerca de la retención de datos, vea [Data retention, deletion, and destruction in Microsoft 365](assurance-data-retention-deletion-and-destruction-overview.md).
