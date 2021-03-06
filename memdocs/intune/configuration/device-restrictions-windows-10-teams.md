---
title: Restricciones de dispositivos de Microsoft Intune para Windows 10 Team
titleSuffix: ''
description: Obtenga información sobre las restricciones de dispositivos disponibles para dispositivos que ejecutan Windows 10 Team.
keywords: ''
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 3/6/2018
ms.topic: reference
ms.service: microsoft-intune
ms.subservice: configuration
ms.localizationpriority: medium
ms.technology: ''
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: 31457667612617bb573ddfb145ed26f70de33159
ms.sourcegitcommit: 7f17d6eb9dd41b031a6af4148863d2ffc4f49551
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "79361658"
---
# <a name="microsoft-intune-windows-10-team-device-restriction-settings"></a>Configuración de restricciones de dispositivos Windows 10 Team de Microsoft Intune

En este artículo, se muestran las opciones de configuración de restricciones de dispositivos de Microsoft Intune que puede configurar para los dispositivos que ejecutan Windows 10 Team.

## <a name="apps-and-experience"></a>Aplicaciones y experiencia

- **Reactivar pantalla cuando hay alguien en la sala**: permite que el dispositivo se active automáticamente cuando su sensor detecta alguien en la sala.
- **Información sobre la reunión en la pantalla de inicio de sesión**: habilite esta opción para elegir la información que se muestra en el icono de reuniones de la pantalla de bienvenida. Puede:
  - **Mostrar solo el organizador y la hora**
  - **Mostrar el organizador, la hora y el asunto (asunto oculto para reuniones privadas)**
- **URL de imagen de fondo de pantalla de inicio de sesión**: habilite esta opción para mostrar un fondo personalizado en la pantalla de **bienvenida** de los dispositivos Windows 10 Team desde la dirección URL que especifique.<br>La imagen debe tener el formato PNG y la dirección URL debe comenzar con **https://** .

## <a name="azure-operational-insights"></a>Azure Operational Insights

- **Azure Operational Insights**: parte del conjunto de aplicaciones Microsoft Operations Manager, Azure Operational Insights recopila, almacena y analiza datos de archivos de registro de dispositivos con Windows 10 Team.
Para conectarse a Azure Operational Insights, debe especificar un **identificador del área de trabajo** y una **clave del área de trabajo**.

## <a name="maintenance"></a>Mantenimiento

- **Ventana de mantenimiento para actualizaciones**: configura la ventana de cuándo pueden tener lugar actualizaciones en el dispositivo. Puede configurar la **hora de inicio** de la ventana y la **duración en horas** (de 1 a 5 horas).

## <a name="wireless-projection"></a>Proyección inalámbrica

- **PIN para proyección inalámbrica**: especifica si debe escribir un PIN para poder usar las funcionalidades de proyección inalámbrica del dispositivo.
- **Proyección inalámbrica de Miracast**: seleccione esta opción si quiere permitir que el dispositivo Windows 10 Team use los dispositivos habilitados para Miracast para proyectar.
- **Canal de proyección inalámbrica de Miracast**: seleccione el canal de Miracast que se usa para establecer la conexión.

## <a name="next-steps"></a>Pasos siguientes

Use la información descrita en [Configuración de restricciones de dispositivos en Microsoft Intune](device-restrictions-configure.md) para guardar y asignar el perfil a los usuarios y dispositivos.
