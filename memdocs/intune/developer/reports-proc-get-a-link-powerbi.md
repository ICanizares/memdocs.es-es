---
title: Conectarse al Almacenamiento de datos con Power BI
titleSuffix: Microsoft Intune
description: Puede descargar un archivo para su uso con Microsoft Power BI que le permite cargar informes interactivos generados de forma dinámica para el inquilino de Microsoft Intune.
keywords: Almacenamiento de datos de Intune
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 01/03/2020
ms.topic: reference
ms.service: microsoft-intune
ms.subservice: developer
ms.localizationpriority: medium
ms.technology: ''
ms.assetid: 5E5A35D3-88F8-441B-8A0B-C5D7A1E5137B
ms.reviewer: aanavath
ms.suite: ems
search.appverid: MET150
ms.custom: intune-classic
ms.collection: M365-identity-device-management
ms.openlocfilehash: d6dfba55c8e516e2e689513f063d56f5a43d52d9
ms.sourcegitcommit: 7f17d6eb9dd41b031a6af4148863d2ffc4f49551
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "79359890"
---
# <a name="connect-to-the-data-warehouse-with-power-bi"></a>Conectarse al Almacenamiento de datos con Power BI

[!INCLUDE [azure_portal](../includes/azure_portal.md)]

Puede usar la aplicación de cumplimiento de Power BI para cargar informes interactivos generados de forma dinámica para el inquilino de Intune. También puede cargar los datos del inquilino de Power BI mediante el vínculo de OData. Intune proporciona opciones de conexión al inquilino, de modo que puede consultar los siguientes ejemplos de informes y gráficos relacionados con dichas opciones:  

- Dispositivos
- Inscripción
- Directiva de protección de aplicaciones
- Directiva de cumplimiento
- Perfiles de configuración de dispositivos
- Actualizaciones de software
- Registros de inventario de dispositivos

También se resaltan las tendencias de la inscripción, el cumplimiento, el perfil de configuración de dispositivos y las actualizaciones de software. Los gráficos e informes de ejemplo aplican al lienzo filtros fáciles de usar. Para usar filtros avanzados, vea el panel **Filtro** de Power BI Desktop.

En los pasos siguientes se muestra cómo descargar el archivo de Power BI y cómo usar el vínculo de OData con Power BI.

[!INCLUDE [reports-credential-reqs](../includes/reports-credential-reqs.md)]

## <a name="install-power-bi"></a>Instalar Power BI

Instale la versión más reciente de [Power BI Desktop](https://aka.ms/intune/datawarehouseapi/installpowerbi). Para más información, vea [Power BI Desktop](https://powerbi.microsoft.com/desktop).

## <a name="load-the-data-and-reports-using-the-power-bi-intune-compliance-data-warehouse-app"></a>Cargar los datos e informes con la aplicación de almacenamiento de datos de cumplimiento de Power BI Intune

La aplicación [Cumplimiento de Intune (almacenamiento de datos)](https://aka.ms/intune/datawarehouseapi/getpowerbiapp) de Power BI contiene información para el inquilino y un conjunto de informes creados previamente basados en el modelo de datos de Almacenamiento de datos.

1. Vaya a la página **AppSource** de la aplicación [Cumplimiento de Intune (almacenamiento de datos)](https://aka.ms/intune/datawarehouseapi/getpowerbiapp) para empezar el proceso de instalación.
2. Haga clic en el botón **Obtenerla ahora** y luego en **Continuar**.
3. Cuando se le pida que instale la aplicación de Power BI, haga clic en **Instalar**.
4. Una vez completada la instalación, haga clic en el icono **Cumplimiento de Intune (Data Warehouse)** de la aplicación.
5. Haga clic en el botón **Conectar**. Se muestra el cuadro de diálogo **Connect to Intune Compliance (Data Warehouse)** (Conectarse a Cumplimiento de Intune [almacenamiento de datos]).
6. Presione el botón **Iniciar sesión**.
7. Inicie sesión con una cuenta de usuario que tenga acceso al almacén de datos de Intune para el inquilino que tiene informes que quiere ver.
8. Para ver el panel de información incluido, haga clic en la pestaña **Paneles** y, luego, en el panel **Información general de cumplimiento**.
9. Para ver todos los informes disponibles, haga clic en la pestaña **Informes** y luego en el informe **Cumplimiento V1.0**. Navegue por las páginas del informe haciendo clic en las pestañas de la parte inferior.
10. Para que sea fácil navegar a estos informes más adelante, haga clic en la estrella junto al informe **Cumplimiento V1.0** y así el informe se agregará a los favoritos de Power BI.

Si lo prefiere, puede instalar la aplicación desde el portal de Intune:

1. Inicie sesión en Azure Portal y seleccione **Supervisión y administración** > **Intune**. También puede buscar recursos para Intune.
2. Abra la hoja **Configurar el almacenamiento de datos de Intune**.
3. Seleccione **Obtener aplicación de Power BI** para acceder a informes de Power BI creados previamente para el inquilino en el explorador y poder compartirlos.
4. Siga los pasos anteriores del 2 al 10.

## <a name="load-the-data-in-power-bi-using-the-odata-link"></a>Cargar los datos en Power BI mediante el vínculo de OData

Con un cliente autenticado en Azure AD, la dirección URL de OData se conecta al punto de conexión de RESTful en la API de Almacenamiento de datos que expone el modelo de datos al cliente de informes. Siga estas instrucciones para usar Power BI Desktop para conectarse y crear sus propios informes. No hace falta que se limite a Power BI Desktop, ya que puede usar la herramienta de análisis que prefiera con la dirección URL de OData, siempre y cuando el cliente admita la autenticación de OAUTH2.0 y el estándar de OData v4.0.

1. Inicie sesión en [Intune](https://go.microsoft.com/fwlink/?linkid=2090973).
2. Haga clic en **Set up Intune Data Warehouse** (Configurar Data Warehouse de Intune) en la sección **Otras tareas** a la derecha de la hoja de información general. Abra la hoja **Intune Data Warehouse** (Data Warehouse de Intune).
3. Recupere la dirección URL de fuente personalizada desde la hoja de informes; por ejemplo:<br>
    `https://fef.{yourinfo}.manage.microsoft.com/ReportingService/DataWarehouseFEService/dates?api-version=v1.0`
4. Abra **Power BI Desktop**.
5. Elija **Archivo** > **Obtener datos**. Seleccione **Fuente OData**.
6. Elija **Básica**.
7. Escriba o pegue la **URL de OData** en el cuadro de dirección URL.
8. Seleccione **Aceptar**.
9. Si no se ha autenticado en Azure AD para el inquilino desde el cliente de Power BI Desktop, escriba sus credenciales. Para obtener acceso a los datos, debe realizar la autorización con Azure Active Directory (Azure AD) mediante OAuth 2.0.  
    1. Seleccione **Cuenta de organización**.  
    2. Escriba su nombre de usuario y su contraseña.  
    3. Seleccione **Iniciar sesión**.  
    4. Seleccione **Conectar**.  
10. Seleccione **Cargar**.

## <a name="next-steps"></a>Pasos siguientes

Puede encontrar respuestas a preguntas sobre su entorno, como el número de dispositivos inscritos por día durante la última semana. Puede obtener una visión general de los inquilinos y los clientes de Intune mediante los informes de Power BI de almacenamiento de datos de Intune, que se obtienen en la hoja de Azure. Además, Intune proporciona diversas formas adicionales de ampliar o reutilizar los datos. Power BI y la API de almacenamiento de datos de Intune proporcionan también otras funciones, como por ejemplo:

<!-- - You can use Power BI Desktop to create additional report types with your data. For example, you could create a custom chart representing the ratio of device manufactures in your enterprise. For more information about creating custom reports with Power BI and the Intune Data Warehouse, see `BLOG POST ON POWER BI`. -->
- Los datos de inquilino están organizados de una manera que le ayuda a obtener información a partir de los datos. Para obtener más información sobre cómo se organizan los datos, vea [Data Warehouse Data Model](reports-ref-data-model.md) (Modelo de datos de Almacenamiento de datos).
- También puede acceder a los datos desde una interfaz RESTful e incorporarlos a su aplicación. Para obtener más información, consulte [Get data from the Intune Data Warehouse API with a REST client (Obtener datos de la API de almacenamiento de datos con un cliente de REST)](reports-proc-data-rest.md).
