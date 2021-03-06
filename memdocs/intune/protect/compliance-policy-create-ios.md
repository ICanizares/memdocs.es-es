---
title: 'Configuración de cumplimiento de dispositivos iOS/iPadOS en Microsoft Intune: Azure | Microsoft Docs'
description: Vea una lista de todas las opciones que puede usar al configurar el cumplimiento de dispositivos iOS/iPadOS en Microsoft Intune. Requerir un correo electrónico, comprobar dispositivos liberados o modificados, establecer una versión mínima o máxima permitida de sistema operativo, establecer restricciones de contraseña, incluida la inactividad del dispositivo y la longitud de contraseña, restringir aplicaciones y mucho más.
keywords: ''
author: brenduns
ms.author: brenduns
manager: dougeby
ms.date: 02/07/2020
ms.topic: reference
ms.service: microsoft-intune
ms.subservice: protect
ms.localizationpriority: medium
ms.technology: ''
ms.assetid: 3cfb8222-d05b-49e3-ae6f-36ce1a16c61d
ms.reviewer: samyada
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: d9da6870caed61917d8093e2dd25882cec72d987
ms.sourcegitcommit: 7f17d6eb9dd41b031a6af4148863d2ffc4f49551
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "79353260"
---
# <a name="iosipados-settings-to-mark-devices-as-compliant-or-not-compliant-using-intune"></a>Configuración de iOS/iPadOS para marcar los dispositivos como compatibles o no compatibles con Intune

En este artículo se enumeran y describen las distintas opciones de configuración de cumplimiento que se pueden establecer en dispositivos iOS/iPadOS en Intune. Como parte de la solución de administración de dispositivos móviles (MDM), use estas opciones para requerir un correo electrónico, marcar los dispositivos liberados (descodificados) como no compatibles, establecer un nivel de amenaza permitido, configurar la expiración de las contraseñas y mucho más.

Esta característica se aplica a:

- iOS
- iPadOS

Como administrador del servicio Intune, use esta configuración de cumplimiento para proteger mejor los recursos de la organización. Para más información sobre las directivas de cumplimiento y lo que hacen, vea [Introducción a las directivas de cumplimiento](device-compliance-get-started.md).

## <a name="before-you-begin"></a>Antes de comenzar

[Crear una directiva de cumplimiento](create-compliance-policy.md#create-the-policy). Para **Plataforma**, seleccione **iOS/iPadOS**.

## <a name="email"></a>Correo electrónico

- **Requerir que los dispositivos móviles tengan un perfil de correo electrónico administrado**:  
  - **Sin configurar** (*valor predeterminado*): no se evalúa el cumplimiento o incumplimiento de esta opción de configuración.
  - **Requerir**: si selecciona esta opción, los dispositivos que no tienen un perfil de correo electrónico administrado por Intune se considerarán no compatibles. Un dispositivo no puede tener un perfil de correo administrado si no tiene correctamente definido el destino, o si el usuario configura manualmente la cuenta de correo electrónico en el dispositivo.

  El dispositivo se considera no compatible en estas situaciones:  
  - El perfil de correo electrónico se asigna a un grupo de usuarios distinto del grupo de usuarios al que va dirigido la directiva de cumplimiento.
  - El usuario ya tiene configurada una cuenta de correo electrónico en el dispositivo que coincide con el perfil de correo electrónico de Intune implementado en dicho dispositivo. Intune no puede sobrescribir el perfil configurado por el usuario e Intune no puede administrarlo. Para que sea compatible, el usuario final debe quitar la configuración de correo existente. De este modo, Intune puede instalar el perfil de correo electrónico administrado.  

Para más información sobre los perfiles de correo, vea [Configurar el acceso al correo electrónico corporativo mediante perfiles de correo electrónico con Microsoft Intune](../configuration/email-settings-configure.md).

## <a name="device-health"></a>Estado de dispositivos

- **Dispositivos con Jailbreak**:  
  - **Sin configurar** (*valor predeterminado*): no se evalúa el cumplimiento o incumplimiento de esta opción de configuración.
  - **Bloquear**: marcar los dispositivos raíz (con jailbreak) como no conformes.  

- **Requerir que el dispositivo tenga el nivel de amenaza del dispositivo** *(iOS 8.0 y versiones más recientes)* :  
  use esta opción para hacer que la evaluación del riesgo sea una condición para el cumplimiento. Elija el nivel de amenaza permitido:  
  - **Sin configurar** (*valor predeterminado*): no se evalúa el cumplimiento o incumplimiento de esta opción de configuración.
  - **Protegido**: esta opción es la más segura y significa que el dispositivo no puede tener ninguna amenaza. Si se detecta cualquier nivel de amenaza en el dispositivo, se evaluará como no compatible.
  - **Bajo**: el dispositivo se evalúa como conforme si solo hay amenazas de nivel bajo. Cualquier valor por encima coloca al dispositivo en un estado de no conformidad.
  - **Medio**: el dispositivo se evalúa como conforme si las amenazas presentes en él son de nivel bajo o medio. Si se detecta que el dispositivo tiene amenazas de nivel alto, se determina como no conforme.
  - **Alto**: esta opción es la menos segura, ya que permite que todos los niveles de amenaza. Quizás sea útil si utiliza esta solución solo con fines informativos.

## <a name="device-properties"></a>Propiedades de dispositivos

### <a name="operating-system-version"></a>Versión de sistema operativo  

- **Versión mínima del sistema operativo** *(iOS 8.0 y versiones más recientes)* :  
  Cuando un dispositivo no cumple el requisito de versión mínima del sistema operativo, se notifica como no compatible. Además, se mostrará un vínculo con información sobre cómo actualizar el sistema. El usuario final puede elegir actualizar su dispositivo. Después, puede acceder a los recursos de la empresa.

- **Versión máxima del sistema operativo** *(iOS 8.0 y versiones más recientes)* :  
  Cuando un dispositivo usa una versión de sistema operativo posterior a la de la regla, se bloquea el acceso a los recursos de la empresa. Se pide al usuario final que se ponga en contacto con el administrador de TI. El dispositivo no podrá acceder a los recursos de la empresa mientras no cambie una regla para permitir la versión de sistema operativo.

- **Versión de compilación mínima del sistema operativo** *(iOS 8.0 y versiones más recientes)* :  
  cuando Apple publica actualizaciones de seguridad, habitualmente se actualiza el número de compilación, no la versión del sistema operativo. Use esta característica para escribir un número de compilación mínimo permitido en el dispositivo.

- **Versión de compilación máxima del sistema operativo** *(iOS 8.0 y versiones más recientes)* :  
  cuando Apple publica actualizaciones de seguridad, habitualmente se actualiza el número de compilación, no la versión del sistema operativo. Use esta característica para escribir un número de compilación máximo permitido en el dispositivo.

## <a name="system-security"></a>Seguridad del sistema

### <a name="password"></a>Contraseña

> [!NOTE]
> Después de aplicar una directiva de configuración o cumplimiento en un dispositivo iOS/iPadOS, cada 15 minutos se pedirá al usuario que establezca un código de acceso y se le seguirá pidiendo hasta que se establezca un código de acceso. Si se establece un código de acceso para el dispositivo iOS/iPadOS, se iniciará automáticamente el proceso de cifrado. El dispositivo permanecerá cifrado hasta que se deshabilite el código de acceso.

- **Requerir una contraseña para desbloquear dispositivos móviles**:  
  - **Sin configurar** (*valor predeterminado*): no se evalúa el cumplimiento o incumplimiento de esta opción de configuración.  
  - **Requerir**: los usuarios deben introducir una contraseña para poder acceder al dispositivo. Los dispositivos iOS/iPadOS que usan una contraseña están cifrados.

- **Contraseñas sencillas**:  
  - **Sin configurar** (*valor predeterminado*): los usuarios pueden crear contraseñas sencillas como **1234** o **1111**.
  - **Bloquear**: los usuarios no puedan crear contraseñas sencillas, como **1234** o **1111**. 

- **Longitud mínima de la contraseña**:  
  especifique el número mínimo de dígitos o caracteres que debe tener la contraseña.  

- **Tipo de contraseña requerida**:  
  elija si una contraseña debe tener solo caracteres **numéricos** o si es necesario combinar números y otros caracteres (**alfanuméricos**).

- **Número de caracteres no alfanuméricos en la contraseña**:  
  escriba el número mínimo de caracteres especiales, como `&`, `#`, `%`, `!`, etc., que se deben incluir en la contraseña. 

  Para establecer un número mayor, es necesario que el usuario cree una contraseña más compleja.

- **Máximo de minutos tras bloqueo de pantalla antes de solicitar la contraseña** *(iOS 8.0 y versiones más recientes)* :  
  especifique el tiempo que debe pasar después de bloquear la pantalla antes de que un usuario deba escribir una contraseña para acceder al dispositivo. Las opciones incluyen el valor predeterminado *Sin configurar*, *Inmediatamente*, y entre *1 minuto* y *4 horas*.

- **Máximo de minutos de inactividad hasta que se bloquea la pantalla**:  
  Escriba el tiempo de inactividad antes de que el dispositivo bloquee la pantalla. Las opciones incluyen el valor predeterminado *Sin configurar*, *Inmediatamente*, y entre *1 minuto* y *15 minutos*.

- **Expiración de la contraseña (días)** :  
  seleccione el número de días que faltan para que expire la contraseña y se deba crear una nueva. 

- **Número de contraseñas anteriores que no se pueden reutilizar** *(iOS 8.0 y versiones más recientes)* :   
  escriba el número de contraseñas usadas previamente que no se pueden volver a usar.

### <a name="device-security"></a>Seguridad de dispositivos

- **Aplicaciones restringidas**:  
  Puede restringir aplicaciones si agrega sus identificadores de lote a la directiva. Si un dispositivo tiene instalada la aplicación, el dispositivo se marca como no compatible.

  - **Nombre de la aplicación**: escriba un nombre descriptivo que ayude a identificar el identificador de lote.
  - **Identificador de lote de aplicaciones**: escriba el identificador de lote único asignado por el proveedor de la aplicación. Para buscar el identificador de lote, consulte [Cómo buscar el identificador de lote para una aplicación iOS/iPadOS](https://support.microsoft.com/help/4294074/how-to-find-the-bundle-id-for-an-ios-app) (abre otro sitio web de Microsoft).  

## <a name="next-steps"></a>Pasos siguientes

- [Agregar acciones para dispositivos no compatibles](actions-for-noncompliance.md) y [usar etiquetas de ámbito para filtrar directivas](../fundamentals/scope-tags.md).
- [Supervisar las directivas de cumplimiento](compliance-policy-monitor.md).
- Vea [Configuración de directivas de cumplimiento para dispositivos macOS](compliance-policy-create-mac-os.md).
