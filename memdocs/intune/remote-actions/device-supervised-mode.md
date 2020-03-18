---
title: Activación del modo supervisado de iOS/iPadOS con Microsoft Intune
titleSuffix: ''
description: Obtenga más información sobre cómo activar el modo supervisado de iOS/iPadOS con Intune.
keywords: ''
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 02/15/2018
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: remote-actions
ms.localizationpriority: high
ms.technology: ''
ms.assetid: 8190814-07f0-42d8-9b3a-87c67dd2b7ed
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: 5d9b147a9a2c201cde798abcee30a212176cf268
ms.sourcegitcommit: 3d895be2844bda2177c2c85dc2f09612a1be5490
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2020
ms.locfileid: "79338050"
---
# <a name="turn-on-iosipados-supervised-mode"></a>Activación del modo supervisado de iOS/iPadOS


[!INCLUDE [azure_portal](../includes/azure_portal.md)]

El modo supervisado de Apple iOS/iPadOS ofrece a los administradores más opciones a la hora de administrar dispositivos Apple, lo que resulta útil para dispositivos corporativos implementados a escala. Por ejemplo, puede restringir AirDrop o evitar que los usuarios cambien el nombre del dispositivo. Para obtener una lista de opciones que requieren el modo supervisado, vea [Configuración de restricciones de dispositivos iOS de Microsoft Intune](../configuration/device-restrictions-ios.md).

Intune admite el modo supervisado como parte del [Programa de inscripción de dispositivos (DEP)](../enrollment/device-enrollment-program-enroll-ios.md) de Apple.

Para obtener una lista de controles de Apple que requieren supervisión, vea la [referencia de configuración de carga](http://help.apple.com/configurator/mac/2.4/#/cad5370d089) de Apple.

## <a name="turn-on-supervised-mode-during-enrollment"></a>Activación del modo supervisado durante la inscripción

En el [Centro de administración de Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431), puede activar el modo supervisado para los dispositivos cuando [crea un perfil de inscripción de Apple en DEP](../enrollment/device-enrollment-program-enroll-ios.md#create-an-apple-enrollment-profile). En **Configuración de administración de dispositivos**, active la casilla **Supervisado**.

## <a name="turn-on-supervised-mode-after-enrollment"></a>Activación del modo supervisado después de la inscripción

Después de la inscripción, la única manera de activar el modo supervisado es conectar un dispositivo iOS/iPadOS a un equipo Mac y [usar Apple Configurator](../enrollment/apple-configurator-enroll-ios.md), lo que restablece el dispositivo. Tras la inscripción, no es posible configurar el modo supervisado para un dispositivo en Intune.

## <a name="identify-a-supervised-device"></a>Identificación de un dispositivo supervisado

Para determinar si un dispositivo está supervisado, vea la pantalla de bloqueo o la página **Acerca de**:
- En la pantalla de bloqueo del dispositivo, se indicará **Este iPhone está administrado por "Nombre de la compañía"** .
- En la página **Acerca de** del dispositivo, se indicará **Este iPhone está supervisado. La empresa puede supervisar el tráfico de Internet y localizar este dispositivo**.

## <a name="next-steps"></a>Pasos siguientes

Para otras opciones de administración de dispositivos, vea [¿Qué es la administración de dispositivos de Microsoft Intune?](device-management.md)