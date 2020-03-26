---
title: 'Restricción de las características de los dispositivos mediante directivas en Microsoft Intune: Azure | Microsoft Docs'
description: Agregue un perfil de dispositivo para restringir características en dispositivos Android, macOS, iOS, iPadOS, Windows Phone y Windows 10 en Microsoft Intune
keywords: ''
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 02/18/2020
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: configuration
ms.localizationpriority: high
ms.technology: ''
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: 28cf0b8bffc06a0b5a56165c1e9eeab780c453c7
ms.sourcegitcommit: 3d895be2844bda2177c2c85dc2f09612a1be5490
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2020
ms.locfileid: "79361827"
---
# <a name="configure-device-restriction-settings-in-microsoft-intune"></a>Configurar restricciones de dispositivos en Microsoft Intune



Intune incluye directivas de restricción de dispositivos que ayudan a los administradores a controlar dispositivos Android, iOS/iPadOS, macOS y Windows. Estas restricciones permiten controlar una amplia variedad de configuraciones y características para proteger los recursos de la organización. Por ejemplo, los administradores pueden:

- Permitir o bloquear la cámara del dispositivo
- Controlar el acceso a Google Play, las tiendas de aplicaciones, la visualización de documentos y los juegos
- Bloquear aplicaciones integradas o crear una lista de aplicaciones permitidas o prohibidas
- Permitir o impedir la copia de seguridad de archivos en la nube y en cuentas de almacenamiento
- Establecer una longitud mínima de contraseña y bloquear las contraseñas poco seguras

Estas características están disponibles en Intune y el administrador puede configurarlas. Intune usa "perfiles de configuración" para crear y personalizar estas configuraciones para las necesidades de su organización. Después de agregar estas características en un perfil, puede insertar o implementar el perfil en los dispositivos de su organización.

En este artículo se muestra cómo crear un perfil de restricciones de dispositivos. También puede ver todas las opciones de configuración disponibles para las distintas plataformas.

## <a name="create-the-profile"></a>Creación del perfil

1. Inicie sesión en el [Centro de administración de Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Seleccione **Dispositivos** > **Perfiles de configuración** > **Crear perfil**.
3. Escriba las propiedades siguientes:

    - **Nombre**: escriba un nombre descriptivo para la directiva. Asígnele un nombre a las directivas para que pueda identificarlas de manera sencilla más adelante. Por ejemplo, un nombre de directiva válido es **iOS/iPadOS: Bloquear la cámara en los dispositivos**.
    - **Descripción**: escriba una descripción para la directiva. Esta configuración es opcional pero recomendada.
    - **Plataforma**: seleccione la plataforma de los dispositivos. Las opciones son:  

        - **Android**
        - **Android Enterprise**
        - **iOS/iPadOS**
        - **macOS**
        - **Windows Phone 8.1**
        - **Windows 8.1 y versiones posteriores**
        - **Windows 10 y versiones posteriores**

    - **Tipo de perfil**: Seleccione **Restricciones de dispositivos**.

        Para crear un perfil de restricciones de dispositivos para dispositivos Windows 10 Team, como Surface Hub, elija **Restricciones de dispositivos (Windows 10 Team)** .

4. Dependiendo de la plataforma que haya elegido, las opciones que pueda configurar serán diferentes. Elija la plataforma para la configuración detallada:

    - [Configuración de Android](device-restrictions-android.md)
    - [Configuración de Android Enterprise](device-restrictions-android-for-work.md)
    - [Configuración de iOS/iPadOS](device-restrictions-ios.md)
    - [Configuración de macOS](device-restrictions-macos.md)
    - [Configuración de Windows Phone 8.1](device-restrictions-windows-phone-8-1.md)
    - [Windows 8.1](device-restrictions-windows-8-1.md)
    - [Configuración de Windows 10](device-restrictions-windows-10.md)
    - [Configuración de Windows 10 Team](device-restrictions-windows-10-teams.md)
    - [Configuración de Windows Holographic for Business](device-restrictions-windows-holographic.md)

5. Cuando haya terminado, seleccione **Aceptar** > **Crear** para guardar los cambios.

El perfil se crea y se muestra en la lista de perfiles.

## <a name="next-steps"></a>Pasos siguientes

Una vez creado el perfil, está listo para asignarlo. Después, [asigne el perfil](device-profile-assign.md) y [supervise el estado](device-profile-monitor.md).

<!--  Removing image as part of design review; retaining source until we known the disposition.

## Example of device restriction settings

In this high-level example, you'll create a device restriction policy that blocks the use of the built-in camera app on Android devices.

![How to disable the camera on Android devices](./media/device-restrictions-configure/disable-android-camera.png)

-->