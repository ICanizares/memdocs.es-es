---
title: 'Comprobación del éxito o error de las líneas de base de seguridad en Microsoft Intune: Azure | Microsoft Docs'
description: Compruebe el estado de error, conflicto y éxito al implementar líneas base de seguridad para usuarios y dispositivos en MDM de Microsoft Intune. Vea cómo solucionar problemas mediante registros de cliente y las características de informes en Intune.
keywords: ''
author: brenduns
ms.author: brenduns
manager: dougeby
ms.date: 04/01/2020
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: protect
ms.localizationpriority: high
ms.technology: ''
ms.assetid: ''
ms.reviewer: laarrizz
ms.suite: ems
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: b9208c07b35aa7830cfe702604a6dabbcb41ab9f
ms.sourcegitcommit: a4ec80c5dd51e40f3b468e96a71bbe29222ebafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2020
ms.locfileid: "82693432"
---
# <a name="monitor-security-baseline-and-profiles-in-microsoft-intune"></a>Supervisión de la línea base de seguridad y los perfiles en Microsoft Intune

Intune ofrece varias opciones para supervisar las líneas base de seguridad. Puede supervisar el perfil de las líneas de base de seguridad que se aplica a los usuarios y dispositivos. También puede supervisar la línea de base real y todos los dispositivos que coinciden (o no) con los valores recomendados.

Este artículo le guiará a través de ambas opciones de supervisión.

Las [líneas de base de seguridad en Intune](security-baselines.md) proporcionan más detalles sobre la característica de las líneas de base de seguridad en Microsoft Intune.

## <a name="monitor-the-baseline-and-your-devices"></a>Supervisión de la línea base y los dispositivos

Al supervisar una línea base, obtiene conclusiones sobre el estado de seguridad de los dispositivos según las recomendaciones de Microsoft. Puede ver estas conclusiones en el panel Información general de la línea base de seguridad en la consola de Intune.  Los datos tardan hasta 24 horas en aparecer después de asignar una línea base en primer lugar. Los cambios posteriores tardan hasta seis horas en aparecer.

Para ver los datos de supervisión de la línea base y de los dispositivos, inicie sesión en el [Centro de administración de Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431). Luego, seleccione **Seguridad de los puntos de conexión** > **Líneas base de seguridad**, seleccione una línea base y vea el panel **Información general**.

El panel de **Información general** proporciona dos métodos para supervisar el estado:

- **Vista de dispositivo**: resumen de cuántos dispositivos están en cada categoría de estado para la línea base.
- **Por categoría**: vista que muestra cada categoría en la línea base e incluye el porcentaje de dispositivos por cada grupo de estado y por cada categoría de línea base.

Cada dispositivo se representa mediante uno de los siguientes estados (que se usan tanto en la vista de *dispositivo* como en las vistas *por categoría*):

- **Coincide con la línea de base**: todas las configuraciones de la línea base coinciden con la configuración recomendada.
- **No coincide con la línea de base**: los valores predeterminados de una o más opciones de la línea base se modificaron en la línea de base original. Los valores predeterminados de cada línea de base de seguridad son los valores recomendados para esa línea de base.

  > [!NOTE]
  > Al crear o editar un perfil de base de referencia, cualquier cambio que se realice en un valor predeterminado o en un valor de configuración genera el estado *No coincide con la línea de base*. Si necesita ayuda para determinar la configuración que se cambió, póngase en contacto con Soporte técnico de Microsoft. 

- **Configuración errónea**: al menos un valor de configuración no está configurado correctamente. Este estado significa que la configuración está en un estado de conflicto, error o pendiente.
- **No aplicable**: al menos un valor de configuración no es aplicable.

### <a name="device-view"></a>Vista de dispositivo

El panel Información general muestra un resumen basado en gráficos de cuántos dispositivos tienen un estado específico para la línea base; **Posición de línea de base de seguridad para los dispositivos Windows 10 asignados**.

![Comprobación del estado de los dispositivos](./media/security-baselines-monitor/overview.png)

Cuando un dispositivo tiene un estado diferente en distintas categorías en la línea base, el dispositivo se representa mediante un único estado. El estado que representa el dispositivo se toma de la orden de precedencia siguiente: **Configuración errónea**, **No coincide con la línea de base**, **No aplicable** y **Coincide con la línea de base**.

Por ejemplo, si un dispositivo tiene un valor de configuración clasificado como *Configuración errónea* y uno o más valores clasificados como *No coincide con la línea de base*, el dispositivo se clasificará como *Configuración errónea*.

Puede hacer clic en el gráfico para obtener detalles y ver una lista de dispositivos con distintos estados. Después, puede seleccionar dispositivos concretos de esa lista para ver detalles concretos. Por ejemplo:

- Seleccione **Configuración del dispositivo**  y elija el perfil con un estado de error:

  ![Ver el estado de un perfil](./media/security-baselines-monitor/device-configuration-profile-list.png)

- Seleccione el perfil con error. Se muestra una lista de todas las configuraciones del perfil y su estado. Ahora, puede desplazarse para encontrar la configuración que produce el error:

  ![Visualización de la configuración que causa el error](./media/security-baselines-monitor/profile-with-error-status.png)

Use este informe para ver cualquier configuración de un perfil que está provocando un problema. Obtenga también más detalles sobre las directivas y los perfiles implementados en los dispositivos.

> [!NOTE]
> Cuando se establece una propiedad en **No configurada** en la línea de base, la configuración se omite y no se aplican restricciones. La propiedad no se muestra en los informes.

### <a name="per-category-view"></a>Vista por categoría

El panel Información general muestra un gráfico de cada categoría para la línea base; **Posición de línea de base de seguridad por categoría**.  Esta vista muestra cada categoría desde la línea base e identifica el porcentaje de dispositivos que pertenecen a una clasificación de estado para cada una de esas categorías.

![Vista de estado por categoría](./media/security-baselines-monitor/monitor-baseline-per-category.png)

El estado **Coincide con la línea de base** no se muestra hasta que el 100 % de los dispositivos de esa categoría informen de ese estado.

Se puede ordenar la vista por categoría según cada columna seleccionando el icono de flecha arriba y abajo en la parte superior de la columna.

## <a name="monitor-the-profile"></a>Supervisión del perfil

La supervisión del perfil proporciona conclusiones sobre el estado de implementación de los dispositivos, pero no el estado de seguridad según las recomendaciones de la línea de base.

1. En Intune, seleccione **Líneas base de seguridad**> seleccione una línea de base > **Profiles created** (Perfiles creados).

2. Seleccione un perfil. En **Información general**, la imagen muestra cuántos dispositivos y usuarios tienen asignado este perfil:

   ![Visualización del número de dispositivos y usuarios que tienen asignado el perfil de líneas de base de seguridad](./media/security-baselines-monitor/existing-profile-overview.png)

3. En **Administrar** > **Propiedades**, se muestra una lista de todas las configuraciones de la línea de base. También puede cambiar cualquiera de estas configuraciones:

   ![Visualización y actualización de la configuración en el perfil de las líneas de base de seguridad](./media/security-baselines-monitor/manage-settings.png)

4. En **Monitor**, puede ver el estado de implementación del perfil en dispositivos individuales, el estado de cada usuario y el estado de cada valor de configuración en la línea de base:

   ![Visualización de diferentes opciones de supervisión para un perfil de las líneas de base de seguridad](./media/security-baselines-monitor/monitor-status-options.png)

## <a name="view-endpoint-security-configurations-per-device"></a>Visualización de configuraciones de seguridad de los puntos de conexión por dispositivo

Vea detalles sobre las configuraciones de seguridad que se aplican a un dispositivo individual, lo que puede ayudarle a aislar los valores configurados incorrectamente.

1. Inicie sesión en el [Centro de administración de Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431).

2. Vaya a **Dispositivos** > **Todos los dispositivos** y seleccione el dispositivo que quiera ver.

3. En la categoría *Supervisión*, seleccione **Configuración de seguridad de los puntos de conexión** para ver la lista de configuraciones de seguridad que se aplican a ese dispositivo.

4. Puede seleccionar una configuración de seguridad de los puntos de conexión para profundizar y ver detalles adicionales sobre la evaluación de esa configuración de seguridad en el dispositivo.

## <a name="troubleshoot-using-per-setting-status"></a>Solución de problemas utilizando el estado por valor de configuración

Ha implementado una línea de base de seguridad, pero el estado de implementación muestra un error. Los pasos siguientes ofrecen algunas instrucciones sobre cómo solucionar el error.

1. En Intune, seleccione **Líneas base de seguridad**> seleccione una línea de base > **Profiles created** (Perfiles creados).

2. Seleccione un perfil > **Monitor** > **Estado por valor**.

3. La tabla muestra todas las configuraciones y el estado de cada valor de configuración. Seleccione la columna **Error** o la columna **Conflicto** para ver el valor de configuración que causa el error.

### <a name="mdm-diagnostic-information"></a>Información de diagnóstico MDM

Ahora conoce el valor de configuración problemático. El siguiente paso es averiguar por qué este valor de configuración está causando un error o conflicto.

En dispositivos con Windows 10, hay un informe de detalles de diagnóstico integrado de MDM. Este informe incluye valores predeterminados, valores actuales, enumera la directiva, muestra si se implementa en el dispositivo o el usuario, etc. Use este informe para ayudar a determinar por qué el valor de configuración está causando un conflicto o error.

1. En el dispositivo, vaya a **Configuración** > **Cuentas** > **Obtener acceso a trabajo o escuela**.

2. Seleccione la cuenta > **Información** > **Advanced Diagnostic Report (Informe de diagnóstico avanzado)**  > **Crear informe**.

3. Elija **Exportar** y abra el archivo generado.

4. En el informe, busque el error o el valor de configuración conflictivo en las diferentes secciones del informe.

  Por ejemplo, busque en las secciones **Enrolled configuration sources and target resources** (Recursos de destino y orígenes de configuración inscritos) o **Unmanaged policies** (Directivas no administradas). Puede hacerse una idea de por qué está causando un error o conflicto.

En [Diagnose MDM failures in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) (Diagnósticos de errores MDM en Windows 10) se proporciona más información sobre este informe integrado.

> [!TIP]
>
> - Algunas configuraciones también enumeran el GUID. Puede buscar este GUID en el registro local (regedit) para cualquier valor establecido.
> - Los registros del Visor de eventos también pueden incluir alguna información de error sobre el valor de configuración problemático (**Visor de eventos** > **Registros de aplicaciones y servicios** > **Microsoft** > **Windows** > **DeviceManagement-Enterprise-Diagnostics-Provider** > **Admin**).

## <a name="next-steps"></a>Pasos siguientes

- [Más información sobre las líneas de base de seguridad](security-baselines.md)
- [Evitación de conflictos](security-baselines.md#avoid-conflicts)
- [Supervisar perfiles de dispositivo](../configuration/device-profile-monitor.md) 
- [Problemas comunes y sus soluciones](../configuration/device-profile-troubleshoot.md)
- [Solución de problemas de directivas y perfiles en Intune](../configuration/troubleshoot-policies-in-microsoft-intune.md)