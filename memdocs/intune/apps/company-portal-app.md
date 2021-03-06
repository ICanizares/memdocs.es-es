---
title: Personalización de las aplicaciones del Portal de empresa de Intune, el sitio web del Portal de empresa y la aplicación de Intune
titleSuffix: Microsoft Intune
description: Aprenda a aplicar personalización de marca específica de la empresa a las aplicaciones del Portal de empresa de Intune, el sitio web del Portal de empresa y la aplicación de Intune.
keywords: ''
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 03/16/2020
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: apps
ms.localizationpriority: high
ms.technology: ''
ms.assetid: dec6f258-ee1b-4824-bf66-29053051a1ae
ms.reviewer: esthermsft
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: e6a3152966dee507cde690d9be8f5a7e210c7945
ms.sourcegitcommit: e2877d21dfd70c4029c247275fa2b38e76bd22b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2020
ms.locfileid: "80407753"
---
# <a name="how-to-customize-the-intune-company-portal-apps-company-portal-website-and-intune-app"></a>Personalización de las aplicaciones del Portal de empresa de Intune, el sitio web del Portal de empresa y la aplicación de Intune

Las aplicaciones del Portal de empresa, el sitio web del Portal de empresa y la aplicación de Intune en Android son los lugares en los que los usuarios acceden a los datos de la empresa y pueden realizar tareas comunes. Las tareas comunes pueden incluir la inscripción de dispositivos, la instalación de aplicaciones y la búsqueda de información (por ejemplo, para solicitar asistencia del departamento de TI). Además, permiten a los usuarios acceder de forma segura a los recursos de la empresa. La experiencia del usuario final ofrece varias páginas diferentes, como Inicio, Aplicaciones, Detalles de la aplicación, Dispositivos y Detalles del dispositivo. Para buscar rápidamente aplicaciones en el Portal de empresa, puede filtrar las aplicaciones en la página Aplicaciones.

## <a name="customizing-the-user-experience"></a>Personalización de la experiencia del usuario

Con la personalización de la experiencia del usuario final, podrá ofrecer una experiencia conocida y útil a los usuarios finales. Para ello, vaya al [Centro de administración de Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431), seleccione **Administración de inquilinos** > **Personalización** y, después, configure las opciones necesarias. Esta configuración se aplicará a las aplicaciones del Portal de empresa, el sitio web del Portal de empresa y la aplicación de Intune en Android.

## <a name="branding"></a>Personalización de marca

En la tabla siguiente se proporcionan los detalles de personalización de marca para la experiencia del usuario final:

| Nombre de campo | Más información |
|---|---|---|
| **Nombre de la organización** | Este nombre se muestra en toda la mensajería en la experiencia del usuario final. Se puede establecer para que se muestre en los encabezados, y también con el valor **Mostrar en encabezado**. La longitud máxima es de 40 caracteres. |
| **Color** | Elija **Estándar** para elegir entre cinco colores estándar. Elija **Personalizado** para seleccionar un color específico según un valor de código hexadecimal. |
| **Color del tema** | Establezca el color del tema para que se muestre en toda la experiencia del usuario final. Se establecerá automáticamente el color del texto en blanco o negro para que sea más visible en la parte superior del color del tema seleccionado. |
| **Mostrar en encabezado** | Seleccione si el encabezado de las experiencias del usuario final mostrará **Nombre y logotipo de empresa**, **Solo el logotipo de empresa** o **Solo el nombre de empresa**. En los cuadros de vista previa siguientes solo se muestran los logotipos, no el nombre.  |
| **Upload logo for theme color background** (Cargar logotipo para fondo de color del tema) | Cargue el logotipo que quiera mostrar encima del color del tema seleccionado. Para conseguir la mejor apariencia, cargue un logotipo con un fondo transparente. Puede ver el aspecto que tendrá en el cuadro de vista previa que se encuentra debajo de la opción.<p>Tamaño máximo de imagen: 400 x 400 píxeles<br>Tamaño máximo de archivo:   750 KB<br>Tipo de archivo: PNG, JPG o JPEG |
| **Upload logo for white or light background** (Cargar logotipo para fondo blanco o claro) | Cargue el logotipo que quiera mostrar encima de los fondos blancos o de color claro. Para conseguir la mejor apariencia, cargue un logotipo con un fondo transparente. Puede ver el aspecto que tendrá sobre un fondo blanco en el cuadro de vista previa que se encuentra debajo de la opción.<p>Tamaño máximo de imagen: 400 x 400 píxeles<br>Tamaño máximo de archivo: 750 KB<br>Tipo de archivo: PNG, JPG o JPEG |
| **Upload brand image** (Cargar imagen de marca) | Cargue una imagen que refleje la marca de su organización.<p><ul><li>Ancho de imagen recomendado: mayor que 1125 píxeles (como mínimo 650 píxeles)</li><li>Tamaño máximo de imagen: 1,3 MB</li><li>Tipo de archivo: PNG, JPG o JPEG</li><li>Se muestra en estas ubicaciones:</li><ul><li>Portal de empresa de iOS o iPadOS: imagen de fondo en la página de perfil del usuario.</li><li>Sitio web del Portal de empresa:   imagen de fondo en la página de perfil del usuario.</li><li>Aplicación de Intune para Android: en el cajón, como imagen de fondo en la página de perfil del usuario.</li></ul></ul> |

> [!NOTE]
> Al instalar una aplicación iOS/iPadOS desde el Portal de empresa, el usuario recibirá un mensaje. Esto sucede cuando la aplicación iOS/iPadOS está vinculada a la tienda de aplicaciones, a un programa de compras por volumen (VPP) o a una aplicación de línea de negocio (LOB). El mensaje permite a los usuarios aceptar la acción o permitir la administración de la aplicación. El mensaje mostrará el nombre de la empresa o, cuando este no esté disponible, se mostrará **Portal de empresa**.

### <a name="brand-image-best-practices"></a>Procedimientos recomendados para la imagen de marca

La imagen de marca adecuada puede mejorar la confianza del usuario al proporcionarle un fuerte sentido de marca de la empresa. Estas son algunas sugerencias que puede tener en cuenta para adquirir, elegir y optimizar la imagen para los lugares de visualización.

- Póngase en contacto con el departamento de marketing o imágenes de la empresa. Es posible que ya tengan un conjunto aprobado de imágenes de marca. Es posible que también le ayuden a optimizar las imágenes según sea necesario.
- Considere tanto la composición horizontal como la vertical. La imagen debe tener suficiente espacio de fondo rodeando el punto focal. La imagen puede recortarse de forma diferente según el tamaño, la orientación y la plataforma del dispositivo.
- Evite usar una imagen estándar genérica. La imagen debe reflejar la marca de la empresa y resultar familiar a los usuarios. Si no tiene una, es mejor no usar ninguna que usar una imagen genérica que no aporte ningún significado para el usuario.
- Quite los metadatos que sean innecesarios. El archivo de imagen puede incluir metadatos, como el perfil de la cámara, la ubicación geográfica, el título, la leyenda, etc. Use una herramienta de optimización de imágenes para eliminar esta información y mantener la calidad al tiempo que cumple los límites de tamaño de archivo.

### <a name="brand-image-examples"></a>Ejemplos de imagen de marca

La siguiente imagen muestra un ejemplo de la imagen de marca en un iPhone:

<img alt="Screenshot of example iPhone branding image" src="./media/company-portal-app/company-portal-app-01.png" width="250">

A continuación se muestra un ejemplo de la imagen de marca en la aplicación de Intune para Android:

<img alt="Screenshot of example #1 for Intune app for Android branding image" src="./media/company-portal-app/company-portal-app-02.png" width="250">

<img alt="Screenshot of example #2 for Intune app for Android branding image" src="./media/company-portal-app/company-portal-app-03.png" width="250">

## <a name="support-information"></a>Información de soporte técnico

Escriba la información de soporte técnico de su organización para que los empleados puedan hacerles llegar sus preguntas. Esta información de soporte técnico se mostrará en las páginas **Soporte técnico**, **Ayuda y soporte técnico** y **Departamento de soporte técnico** en la experiencia del usuario final.

| Nombre de campo | Longitud máxima | Más información |
|------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de contacto | 40 | Este nombre es la persona a la que acuden los usuarios cuando se ponen en contacto con el soporte técnico. |
| Número de teléfono | 20 | Este número permite que los usuarios llamen al servicio de soporte técnico. |
| Dirección de correo electrónico | 40 | Esta dirección de correo electrónico es donde los usuarios pueden enviar correos electrónicos para obtener soporte técnico. Debe especificar una dirección de correo electrónico válida en el formato `alias@domainname.com`. |
| Nombre del sitio web | 40 | Es el nombre descriptivo que se muestra en algunas ubicaciones correspondiente a la dirección URL que lleva al sitio web de soporte técnico. Si especifica una dirección URL de sitio web de soporte técnico y ningún nombre descriptivo, se muestra la propia dirección URL en las experiencias del usuario final.  |
| URL del sitio web | 150 | El sitio web de soporte técnico que usarán los usuarios. La dirección URL debe tener el formato `https://www.contoso.com`.  |
| Información adicional | 120 | Incluya aquí cualquier mensajería adicional relacionada con el soporte técnico para los usuarios. |

## <a name="configuration"></a>Configuración

En la siguiente tabla se proporcionan detalles de configuración adicionales:

| Nombre de campo | Longitud máxima | Más información |
|------------------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL de la declaración de privacidad | 79 | Configure la declaración de privacidad de su organización para que aparezca cuando los usuarios hacen clic en los vínculos de privacidad. Debe especificar una dirección URL válida en el formato `https://www.contoso.com`. |
| Privacy message in the Company Portal for (Mensaje de privacidad en el Portal de empresa para iOS o iPadOS) | 520 | Mantenga el valor predeterminado o establezca un mensaje personalizado para mostrar los elementos que la organización puede o no puede ver en los dispositivos iOS o iPad administrados. Puede usar Markdown para agregar viñetas, negritas, cursivas y vínculos. |
| Inscripción de dispositivos | No aplicable | Especifique si se debe solicitar a los usuarios que se inscriban en la administración de dispositivos móviles y cómo. Puede ver los detalles a continuación. |

### <a name="device-enrollment-setting-options"></a>Opciones de configuración de inscripción de dispositivos

> [!NOTE]
> La compatibilidad con la configuración de inscripción de dispositivos requiere que los usuarios finales tengan estas versiones del Portal de empresa:
> - Portal de empresa en iOS o iPadOS: versión 4.4 o posterior
> - Portal de empresa en Android: versión 5.0.4715.0 o posterior 

|    Opciones de inscripción de dispositivos    |    Descripción    |    Avisos de lista de comprobación    |    Notificación    |    Detalles de estado del dispositivo    |    Detalles de estado de la aplicación (de una aplicación que requiere inscripción)    |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------|-----------------------------|--------------------------------------------------------------------|
|    Disponible, con avisos    |    La experiencia predeterminada con avisos para inscribirse en todas las ubicaciones posibles.    |    Sí    |    Sí    |    Sí    |    Sí    |
|    Disponible, sin avisos    |    El usuario puede inscribirse a través del estado de los detalles de su dispositivo actual o de las aplicaciones que requieren inscripción.    |    No    |    No    |    Sí    |    Sí    |
|    No disponible    |    No hay ninguna manera de que se inscriban los usuarios.    |    No    |    No    |    No    |    No<sup>(1)</sup>    |

<sup>(1)</sup> **Problema conocido:** si establece las aplicaciones para que sea necesaria la inscripción para instalarse y también establece la inscripción de dispositivos en "No disponible", la aplicación Portal de empresa en Android seguirá indicando a los usuarios que se inscriban. Esto se quitará en breve.

> [!NOTE]
> Si usa Azure Government, se ofrecen registros de aplicaciones para que el usuario final decida cómo compartirá cuando inicie el proceso para pedir ayuda para un problema. Sin embargo, si no usa Azure Government, el Portal de empresa enviará registros de aplicaciones directamente a Microsoft cuando el usuario inicie el proceso de pedir ayuda con un problema. Si se envían los registros de aplicaciones a Microsoft, será más fácil solucionar los problemas.

> [!NOTE]
> De acuerdo con la directiva de Microsoft y de Apple, no vendemos a terceros los datos recopilados por nuestro servicio por ningún motivo.

## <a name="company-portal-derived-credentials-for-iosipados-devices"></a>Credenciales derivadas del Portal de empresa para dispositivos iOS o iPadOS

Intune admite las credenciales derivadas de tarjeta de verificación de identidad personal (PIV) o de tarjeta de acceso común (CAC) en colaboración con los proveedores de credenciales DISA Purebred, Entrust Datacard e Intercede. Los usuarios finales tendrán que realizar más pasos tras inscribir su dispositivo iOS/iPadOS para verificar sus identidades en la aplicación Portal de empresa. Para que las credenciales derivadas se habiliten para los usuarios, primero se configurará un proveedor de credenciales para el inquilino y, seguidamente, se establecerá como destino un perfil que use credenciales derivadas para usuarios o dispositivos.

> [!NOTE]
> El usuario verá instrucciones sobre las credenciales derivadas según el vínculo que se haya especificado a través de Intune.

Para obtener más información sobre las credenciales derivadas de dispositivos iOS/iPadOS, vea [Uso de credenciales derivadas en Microsoft Intune](../protect/derived-credentials.md).

## <a name="dark-mode-for-iosipados-company-portal"></a>Modo oscuro para el Portal de empresa de iOS o iPadOS

El modo oscuro está disponible para el Portal de empresa de iOS o iPadOS. Los usuarios pueden descargar aplicaciones, administrar sus dispositivos y obtener soporte técnico de TI en la combinación de colores de su elección en función de la configuración del dispositivo. El Portal de empresa de iOS o iPadOS hará coincidir automáticamente la configuración del dispositivo del usuario final con el modo oscuro o claro.

## <a name="windows-company-portal-keyboard-shortcuts"></a>Métodos abreviados de teclado del Portal de empresa de Windows

Los usuarios finales pueden desencadenar acciones de navegación, aplicación y dispositivo en el Portal de empresa de Windows mediante métodos abreviados de teclado (aceleradores).

Los siguientes métodos abreviados de teclado están disponibles en la aplicación del Portal de empresa de Windows.

| Área | Descripción | Método abreviado de teclado |
|:------------------:|:--------------:|:-----------------:|
| Menú de navegación | Navegación | Alt+M |
|  | Inicio | Alt+H |
|  | Todas las aplicaciones | Alt+A |
|  | Aplicaciones instaladas | Alt+I |
|  | Enviar comentarios | Alt+F |
|  | Mi perfil | Alt+U |
|  | Configuración | Alt+T |
| Página principal, icono de dispositivo | Cambiar nombre | F2 |
|  | Quitar | Ctrl+D o Eliminar |
|  | Comprobar acceso | Ctrl+M o F9 |
| Detalles del dispositivo | Cambiar nombre | F2 |
|  | Quitar | Ctrl+D o Eliminar |
|  | Comprobar acceso | Ctrl+M o F9 |
| Detalles de la aplicación | Instalar | Ctrl+I |
| Dispositivos | Disponible | Ctrl+D |

Los usuarios finales también podrán ver los accesos directos disponibles en la aplicación Portal de empresa de Windows.

![Captura de pantalla de los accesos directos disponibles en el Portal de empresa de Windows](./media/company-portal-app/company-portal-app-04.png)

## <a name="user-self-service-device-actions-from-the-company-portal"></a>Acciones de dispositivo de autoservicio de usuario desde el Portal de empresa

Los usuarios pueden realizar acciones en sus dispositivos locales o remotos mediante la aplicación del Portal de empresa, el sitio web o la aplicación Intune en Android. Las acciones que puede realizar un usuario varían según la plataforma y la configuración del dispositivo. En todos los casos, las acciones de dispositivo remoto solo las puede realizar el usuario primario del dispositivo.

- **Retirar**: quita el dispositivo de la administración de Intune. En el sitio web o la aplicación Portal de empresa, esto se muestra como **Quitar**.
- **Borrar**: esta acción inicia un restablecimiento del dispositivo. En el sitio web del Portal de empresa, se muestra como **Restablecer** o como **Restablecimiento de la configuración de fábrica** en la aplicación del Portal de empresa de iOS o iPadOS.
- **Cambiar nombre**: esta acción cambia el nombre del dispositivo que el usuario puede ver en el Portal de empresa. No cambia el nombre del dispositivo local, solo la lista del Portal de empresa.
- **Sincronizar**: esta acción inicia una inserción en el repositorio del dispositivo en el servicio Intune. Esto se muestra como **Comprobar estado** en el Portal de empresa.
- **Bloqueo remoto**: bloquea el dispositivo y requiere un PIN para desbloquearlo.
- **Restablecer código de acceso**: esta acción se usa para restablecer el código de acceso del dispositivo. En los dispositivos iOS/iPadOS, se quitará el código de acceso y se solicitará al usuario final que especifique uno nuevo en la configuración. En los dispositivos Android compatibles, Intune genera un nuevo código de acceso que se muestra temporalmente en el Portal de empresa.
- **Recuperación de clave**: esta acción se utiliza para recuperar una clave de recuperación personal para dispositivos macOS cifrados desde el sitio web Portal de empresa. 

### <a name="self-service-actions"></a>Acciones de autoservicio

Algunas plataformas y configuraciones no realizar permiten acciones de autoservicio en el dispositivo. En la tabla siguiente se ofrecen más detalles sobre las acciones de autoservicio:

|  | Windows 10<sup>(3)</sup> | iOS/iPadOS<sup>(3)</sup> | MacOS<sup>(3)</sup> | Android<sup>(3)</sup> |
|----------------------|--------------------------|-------------------|-----------------------------------|-------------------------|
| Retirar | Disponible<sup>(1)</sup> | Disponible | Disponible | Disponible<sup>(7)</sup> |
| Eliminación de datos | Disponible | Disponible<sup>(5)</sup> | N/D | Disponible<sup>(7)</sup> |
| Cambiar nombre<sup>(4)</sup> | Disponible | Disponible | Disponible | Disponible |
| Sincronización | Disponible | Disponible | Disponible | Disponible |
| Bloqueo remoto | Solo en Windows Phone | Disponible | Disponible | Disponible |
| Restablecer el código de acceso | Solo en Windows Phone | Disponible<sup>(8)</sup> | N/D | Disponible<sup>(6)</sup> |
| Recuperación de claves | N/D | N/D | Disponible<sup>(2)</sup> | N/D |

<sup>(1)</sup> La función **Retirar** siempre está bloqueada en los dispositivos Windows unidos a Azure AD.<br>
<sup>(2)</sup> **Recuperación de claves** para MacOS solo está disponible a través del portal web.<br>
<sup>(3) </sup> Todas las acciones remotas se deshabilitan si se usa una inscripción del administrador de inscripción de dispositivos.<br>
<sup>(4)</sup> **Cambiar nombre** solo cambia el nombre del dispositivo en la aplicación Portal de empresa o en el portal web, no en el dispositivo.<br>
<sup>(5)</sup> **Borrar** no está disponible en los dispositivos iOS o iPadOS inscritos por el usuario.<br>
<sup>(6)</sup> **Restablecer el código de acceso** no se admite en algunas configuraciones de Android y Android Enterprise. Para más información, consulte [Restablecimiento o eliminación del código de acceso de un dispositivo en Intune](../remote-actions/device-passcode-reset.md).<br>
<sup>(7)</sup> **Retirar** y **Borrar** no están disponibles en escenarios de propietario del dispositivo Android Enterprise (COPE, COBO, COSU).<br> 
<sup>(8)</sup> **Restablecer el código de acceso** no se admite en los dispositivos iOS o iPadOS inscritos por el usuario.

## <a name="next-steps"></a>Pasos siguientes

- [Agregar aplicaciones](apps-add.md)
