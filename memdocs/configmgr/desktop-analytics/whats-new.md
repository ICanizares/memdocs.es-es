---
title: Novedades de Análisis de escritorio
titleSuffix: Configuration Manager
description: Resumen de las nuevas características de la última versión mensual del servicio en la nube Análisis de escritorio.
ms.date: 03/12/2020
ms.prod: configuration-manager
ms.technology: configmgr-analytics
ms.topic: conceptual
ms.assetid: fa300181-86cb-4afe-8fbf-895a7572378d
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: be314aee43e93b5e3d264c70626e2f0b85e8e7f3
ms.sourcegitcommit: bbf820c35414bf2cba356f30fe047c1a34c5384d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "81706383"
---
# <a name="whats-new-in-desktop-analytics"></a>Novedades de Análisis de escritorio

Conozca las novedades mensuales de Análisis de escritorio.

> [!TIP]
> El lanzamiento de cada actualización mensual puede tardar hasta tres días. Algunas características pueden lanzarse a lo largo de varias semanas y pueden no estar disponibles para todos los clientes durante la primera semana.

Para obtener una notificación cuando se actualice esta página, copie y pegue la siguiente dirección URL en su lector de fuentes RSS: `https://docs.microsoft.com/api/search/rss?search=%22what%27s+new+in+desktop+analytics+-+Configuration+Manager%22&locale=en-us`
<!-- a locale is required for the RSS search string -->

## <a name="march-2020"></a>Marzo de 2020

### <a name="support-for-multiple-hierarchies"></a>Compatibilidad con varias jerarquías

<!-- 4814075, 6079184 -->

Ahora puede conectar varias jerarquías de Configuration Manager a un único inquilino de Azure Active Directory con un único identificador comercial para Análisis de escritorio. El portal clasifica los dispositivos de diferentes jerarquías y mejora las experiencias de los planes de implementación y los pilotos globales.

- Al configurar el proyecto piloto global, si incluye recopilaciones que contienen más del 20 % del total de dispositivos inscritos, el portal muestra una advertencia.
- Al crear un plan de implementación, si selecciona recopilaciones para varias jerarquías, el portal muestra una advertencia.

> [!NOTE]
> La compatibilidad con varias jerarquías requiere la versión 1910 o posterior de Configuration Manager.

Vea los siguientes artículos para más información:

- [Piloto global](deploy-pilot.md#bkmk_GlobalPilot)
- [Creación de planes de implementación](create-deployment-plans.md)

### <a name="identify-compatibility-safeguards"></a>Identificación de medidas de seguridad de compatibilidad

<!-- 5746559 -->

Los datos de compatibilidad de Windows clasifican algunas aplicaciones y controladores con una *medida de seguridad*, lo que puede hacer que la actualización a Windows 10 no se realice correctamente o se revierta. Análisis de escritorio ahora puede ayudarle a identificar estas medidas de seguridad de antemano para que pueda corregir el recurso antes de implementar la actualización. Para más información, consulte [Evaluación de compatibilidad: Medidas de seguridad](compat-assessment.md#safeguards).

## <a name="january-2020"></a>Enero de 2020

### <a name="additional-app-usage-detail"></a>Información adicional sobre el uso de la aplicación

<!-- 5533890 -->

Cuando se selecciona una aplicación para ver más información, el panel de detalles muestra ahora información de uso adicional. Puede usar estos datos para comprender el alcance de la instalación de una aplicación, así como para ver los dispositivos en los que los usuarios usan la aplicación con regularidad. Para obtener más información, vea [Acerca de los recursos: uso de la aplicación](about-assets.md#usage).

### <a name="provide-feedback-on-desktop-analytics"></a>Comentarios sobre Análisis de escritorio

<!-- 5451636 -->

Para compartir sus comentarios sobre Análisis de escritorio, seleccione el icono **Enviar una sonrisa** en la parte superior derecha del portal. Para obtener más información, vea [Compartir comentarios sobre el producto](get-support.md#bkmk_feedback).

## <a name="october-2019"></a>Octubre de 2019

### <a name="improvements-to-compatibility-recommendations"></a>Mejoras de las recomendaciones de compatibilidad

<!-- 3594545 -->

Análisis de escritorio proporciona ahora detalles adicionales cuando detecta que la actualización de Windows quitará de forma total o parcial una aplicación o un controlador. Para más información, consulte [Evaluación de compatibilidad](compat-assessment.md#asset-is-removed-during-upgrade).

### <a name="migrate-from-windows-analytics-to-existing-tenant"></a>Migración de Windows Analytics a un inquilino existente

<!-- 5202803 -->

Ahora puede migrar entradas de un área de trabajo de Windows Analytics existente después de incorporarlas a Análisis de escritorio.

## <a name="september-2019"></a>Septiembre de 2019

### <a name="migrate-inputs-from-windows-analytics"></a>Migración de entradas de Windows Analytics

<!-- 4252663 -->

Durante la incorporación, ahora puede migrar entradas de un área de trabajo de Windows Analytics existente.

### <a name="offboard-from-desktop-analytics"></a>Anulación de la incorporación de Análisis de escritorio

<!-- 4972396 -->

Si configuró Análisis de escritorio en el entorno, pero quiere dejar de usar el servicio, ahora puede cerrar la cuenta. Si cambia de opinión en 90 días, puede volver a activarla. Para más información, consulte [Cierre de la cuenta](account-close.md).

## <a name="august-2019"></a>Agosto de 2019

### <a name="reset-your-account"></a>Restablecimiento de la cuenta

<!-- 3733897 -->

Si configuró Análisis de escritorio en el entorno, pero quiere empezar de nuevo con la incorporación y la inscripción, ahora puede restablecerlo. Para más información sobre el proceso, consulte [Restablecimiento de la cuenta](account-reset.md).

### <a name="automatic-upgrade-decision-of-system-and-store-apps"></a>Decisión de actualización automática de las aplicaciones del sistema y de la tienda

<!-- 3587232 -->

Para ayudar a reducir el trabajo de anotar las aplicaciones destacadas, determinados tipos de aplicaciones se marcan automáticamente como *No importante*. La decisión de actualizar el plan de implementación de estas aplicaciones también se marca como *Preparado*. Las siguientes aplicaciones son compatibles y deben seguir funcionando después de actualizar Windows:

- Aplicaciones del sistema y componentes publicados por Microsoft

- Aplicaciones administradas y actualizadas desde Microsoft Store

Para más información, consulte [Decisión de actualización automática de las aplicaciones del sistema y de la tienda](about-assets.md#bkmk_plan-autoapp).

## <a name="whats-new-in-configuration-manager"></a>Novedades de Configuration Manager

Los documentos de Análisis de escritorio siempre hacen referencia a la funcionalidad de la versión más reciente de la rama actual de Configuration Manager. Para más información sobre los últimos cambios de Configuration Manager, consulte los siguientes artículos:

<!-- - [What's new in version 1910](../core/plan-design/changes/whats-new-in-version-1910.md#bkmk_da) -->

- [Novedades de la versión 1906](../core/plan-design/changes/whats-new-in-version-1906.md#bkmk_da)
