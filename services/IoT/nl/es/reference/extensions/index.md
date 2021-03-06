---

copyright:
  years: 2015, 2016
lastupdated: "2016-10-18"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Integraciones de servicios externos
{: #ref-index}

La integración de servicios externos le permite acceder a los datos y operaciones de terceros o servicios externos dentro de la organización de {{site.data.keyword.iot_full}}.

## Jasper
{: #jasper}

Jasper es una plataforma de administración y gestión de dispositivos SIM. Jasper está integrado en el panel de instrumentos de {{site.data.keyword.iot_short_notm}}, lo que hace posible administrar dispositivos Jasper a través de su panel de instrumentos de la organización de {{site.data.keyword.iot_short_notm}}.

### Operaciones soportadas para Jasper

La integración incorporada de Jasper que proporciona nuestra plataforma proporciona soporte para las siguientes operaciones de Jasper:

- Ver datos de Jasper generales
  - Muestra el estado, el plan de tarifas, el uso de datos mensual hasta la fecha, el uso de SMS mensual hasta la fecha, el uso de voz mensual hasta la fecha, los límites por exceso de datos, la fecha de añadido y la fecha de modificación.
- Cambiar el estado de activación de SIM.
  - Puede seleccionar entre Inventario, Preparado para la activación, Activado, Desactivado y Retirado.
- Ver uso de SIM
  - Muestra la fecha de inicio de ciclo, los datos totales y facturables, los SMS totales y facturables y la voz total y facturable.
  - La fecha de inicio del ciclo puede establecerse con un formato AAAA-MM-DD.
- Enviar SMS a SIM
- Cambiar el plan de tarifas

Puede acceder a las operaciones soportadas en los detalles de dispositivo de un dispositivo conectado a Jasper una vez que finalicen los siguientes pasos de configuración.

### API REST para Jasper
Para acceder a la API REST para Jasper, consulte la sección sobre la extensión Jasper de la documentación de [API REST HTTP de {{site.data.keyword.iot_short_notm}}](https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/Jasper_Extension). 

### Configuración para Jasper

Para conectar el servicio de Jasper a la organización de {{site.data.keyword.iot_short_notm}}, hay dos etapas de configuración que debe realizar en primer lugar. Primero, el {{site.data.keyword.iot_short_notm}} debe estar conectado al servicio de Jasper y, a continuación, se deben configurar los dispositivos de {{site.data.keyword.iot_short_notm}}.


1. Habilitar la extensión de Jasper. Para habilitar la integración de Jasper con su organización de {{site.data.keyword.iot_short_notm}}, lleve a cabo los pasos siguientes:
  1. Desde el panel de instrumentos de {{site.data.keyword.iot_short_notm}}, seleccione **Extensiones**.
  2. En la página **Extensiones**, pulse **Añadir ampliación**.
  3. Pulse **Añadir** junto a Jasper.
  4. Especifique su nombre de usuario, contraseña, clave de acceso e ID de dominio de Jasper.
  5. Pulse **Terminado**.

2. Configurar los dispositivos
Puede configurar los dispositivos que están conectados a la organización de {{site.data.keyword.iot_short_notm}} y a la cuenta de Jasper para que muestren datos desde Jasper en el panel de instrumentos de {{site.data.keyword.iot_short_notm}}.  
**Importante:** La configuración de Jasper no se puede aplicar como parte del proceso de Añadir dispositivo. Sólo se pueden configurar con Jasper los dispositivos conectados previamente.  
Para configurar los dispositivos conectados a Jasper, lleve a cabo los pasos siguientes:
 1. En el separador Dispositivos del panel de instrumentos de {{site.data.keyword.iot_short_notm}}, busque el dispositivo conectado a Jasper que se debe configurar.
 2. Seleccione el dispositivo para abrir la vista *Obtener detalles de dispositivo*.
 3. Desplácese hacia abajo hasta *Configuración de ampliación*.
 4. Escriba la configuración de ampliación utilizando el siguiente formato de JSON y, a continuación, pulse **Confirmar cambios** para guardar la configuración.  

```json  
    {
        "jasper": {
            "iccid": "string"
        }
    }

```

Cuando la organización se ha configurado correctamente, se muestra la sección *Ampliaciones* debajo de la sección *Configuración de ampliaciones* de la vista *Detalle de dispositivo*.

## AT&T
{: #att}

### Operaciones soportadas para AT&T

La ampliación de AT&T permite realizar las siguientes operaciones de AT&T:

- Ver datos de AT&T generales
  - Muestra el estado, el plan de tarifas, el uso de datos mensual hasta la fecha, el uso de SMS mensual hasta la fecha, el uso de voz mensual hasta la fecha, los límites por exceso de datos, la fecha de añadido y la fecha de modificación.
- Cambiar el estado de activación de SIM.
  - Puede seleccionar entre Inventario, Preparado para la activación, Activado, Desactivado y Retirado.
- Ver uso de SIM
  - Muestra la fecha de inicio de ciclo, los datos totales y facturables, los SMS totales y facturables y la voz total y facturable.
  - La fecha de inicio del ciclo puede establecerse con un formato AAAA-MM-DD.
- Enviar SMS a SIM
- Cambiar el plan de tarifas

### API REST para AT&T
Para acceder a la API REST para AT&T, consulte la sección sobre la extensión AT&de la [documentación de API REST HTTP de {{site.data.keyword.iot_short_notm}}](https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/AT&T_Extension). 

### Configuración para AT&T

Para conectar la organización de {{site.data.keyword.iot_short_notm}} a AT&T, debe completar la configuración de la organización y la configuración del dispositivo.

Para configurar la plataforma de {{site.data.keyword.iot_short_notm}}, lleve a cabo los pasos siguientes:

1. Habilitar la extensión de AT&T. Para habilitar la integración de AT&T con la organización de {{site.data.keyword.iot_short_notm}}, lleve a cabo los pasos siguientes:
  1. Desde el panel de instrumentos de {{site.data.keyword.iot_short_notm}}, seleccione **Extensiones**.
  2. En la página **Extensiones**, pulse **Añadir ampliación**.
  3. Pulse **Añadir** junto a AT&T.
  4. Especifique su nombre de usuario, contraseña, clave de acceso e ID de dominio de AT&T.
  5. Pulse **Terminado**.

Para conectar la organización de {{site.data.keyword.iot_short_notm}} con la cuenta de AT&T, hay dos etapas de configuración que debe realizar en primer lugar. Complete la configuración de organización y, a continuación, configure los dispositivos.


2. Configurar los dispositivos
Puede configurar los dispositivos conectados a la organización de {{site.data.keyword.iot_short_notm}} y a la cuenta de AT&T para que muestren datos de AT&T en el panel de instrumentos de {{site.data.keyword.iot_short_notm}}.  
**Importante:** La configuración de AT&T no se puede aplicar como parte del proceso Añadir dispositivo. Sólo se pueden configurar los dispositivos conectados anteriormente con AT&T.  
Para configurar los dispositivos conectados a AT&T, lleve a cabo los pasos siguientes:
 1. En el separador Dispositivos del panel de instrumentos de {{site.data.keyword.iot_short_notm}}, busque el dispositivo conectado a AT&T que se debe configurar.
 2. Seleccione el dispositivo para abrir la vista *Obtener detalles de dispositivo*.
 3. Desplácese hacia abajo hasta *Configuración de ampliación*.
 4. Escriba la configuración de ampliación utilizando el siguiente formato de JSON y, a continuación, pulse **Confirmar cambios** para guardar la configuración.  

```json  
    {
        "atnt": {
            "iccid": "string"
        }
    }

```

Cuando la organización se ha configurado correctamente, se muestra la sección *Ampliaciones* debajo de la sección *Configuración de ampliaciones* de la vista *Detalle de dispositivo*.

## Conector ARM mbed
{: #arm}

El conector ARM mbed le permite conectar el dispositivo ARM mbed a su {{site.data.keyword.iot_short_notm}}. La extensión ARM mbed permite el portal ARM mbed y el {{site.data.keyword.iot_short_notm}} para enviar y recibir datos del portal ARM mbed.

### Definir configuración


1. Habilitar la extensión de conector de ARM mbed. Para habilitar la extensión de conector de ARM mbed, lleve a cabo los pasos siguientes:
  1. Desde el panel de instrumentos de {{site.data.keyword.iot_short_notm}}, seleccione **Configuración** y vaya a **Extensiones**.
  2. En el menú **Extensiones**, pulse **Añadir ampliación**.
  3. Pulse **Añadir** junto a la extensión de conector de ARM mbed.
  4. Especifique su clave de acceso e ID de dominio de ARM mbed. Puede encontrarlos mediante el portal de ARM mbed en https://connector.mbed.com.
  5. Compruebe que las credenciales sean correctas pulsando el botón **Comprobar conexión**.
  6. Pulse **Terminado**.

### Formato de carga útil

Hay dos tipos de mensajes de entrada de la plataforma ARM mbed: notificaciones y respuestas asíncronas. El {{site.data.keyword.iot_short_notm}} puede enviar mandatos a los dispositivos que están conectados a la plataforma ARM mbed.

#### Notificaciones

Las notificaciones las generan cambios en los datos de dispositivo o de sensor. Una vez que {{site.data.keyword.iot_short_notm}} procesa el mensaje, es para el tema de sucesos de dispositivos de la misma manera que un dispositivo conectado directamente al {{site.data.keyword.iot_short_notm}}. El tipo de suceso utilizado para las notificaciones que se originan en dispositivos conectados a la plataforma ARM mbed es `notify`.

El ejemplo de código siguiente muestra el formato de carga útil para una notificación enviada por la API de la plataforma ARM mbed:

```
{
  "ep":<endpoint/deviceID>,
  "path":<resource path>,
  "ct":<content type>,
  "payload":<Base64 encoded payload>,
  "max-age":<how long the payload is valid, in seconds>
}
```

#### Respuestas asíncronas

Cuando el {{site.data.keyword.iot_short_notm}} envía un mandato a un dispositivo conectado a la plataforma ARM mbed, el dispositivo envía un mensaje de confirmación al {{site.data.keyword.iot_short_notm}}. Este mensaje de confirmación se denomina *respuesta asíncrona* y utiliza el tipo de suceso `asyncResponse`.

El ejemplo de código siguiente muestra el formato de carga útil para una respuesta asíncrona enviada por el servicio de nube de ARM mbed:

```
{
  "id":<transaction id>,
  "status":<200 is command was sucessfully executed. Check other HTTP response codes>,
  "ct":<content type>,
  "max-age":<how long the payload is valid, in seconds>,
  "payload":<base64 encoded payload>,
  "ep":<endpoint/deviceID affected by the command>,
  "path":<resource path affected by the command>
}
```

#### Envío de mandatos a la plataforma ARM mbed

El {{site.data.keyword.iot_short_notm}} puede enviar mandatos a dispositivos conectados a la plataforma ARM mbed. Los mandatos enviados a la plataforma ARM mbed deben utilizar el siguiente formato JSON.

```
{
  "method":<PUT or POST>,
  "deviceId":<endpoint/deviceId>,
  "resourceId":<resource path>,
  "payload": <Base64 encoded payload>
}
```
El método elegido distingue entre mayúsculas y minúsculas. El '/' inicial de la vía de acceso de recurso se debe omitir.


La carga útil debe publicarse en el tema siguiente:

```
iot-2/type/<device_type>/id/<deviceId>/cmd/<command_type>/fmt/<command_format>
```


## Orange
{: #orange}

La extensión de Orange le permite ver datos de la tarjeta SIM desde dispositivos que están conectados a {{site.data.keyword.iot_short_notm}} y que tienen una tarjeta SIM de Orange instalada.

https://developer.ibm.com/iotplatform/2016/03/30/watson-iot-platform-integration-with-orange-beta/

### Operaciones soportadas para Orange

Si tiene un dispositivo que está conectado a su servicio de {{site.data.keyword.iot_short_notm}} y que tiene una tarjeta SIM de Orange, puede utilizar la extensión de Orange para ver los siguientes datos de la tarjeta SIM:

- Número de serie de SIM
- Estado de activación
- Último cambio de estado
- Última renovación de estado
- Estado de la ubicación

### API REST para Orange
Para acceder a la API REST para Orange, consulte la sección sobre la extensión Orange en la [documentación de API REST HTTP de {{site.data.keyword.iot_short_notm}}](https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/Orange_Extension).

### Configuración para Orange

Para habilitar la extensión de Orange:

1. Desde el panel de instrumentos de {{site.data.keyword.iot_short_notm}}, seleccione **Extensiones**.
2. En la página **Extensiones**, pulse **Añadir ampliación**.
3. Pulse **Añadir** junto a la extensión de Orange.
4. Especifique el nombre de usuario y la contraseña de Orange.
6. Pulse **Terminado**.

Una vez que se haya habilitado la extensión de Orange, se debe configurar cada dispositivo con una tarjeta SIM de Orange para que visualice datos de la SIM de Orange.

1. En el separador Dispositivos del panel de instrumentos de {{site.data.keyword.iot_short_notm}}, busque el dispositivo SIM de Orange que se debe configurar.
2. Seleccione el dispositivo y desplácese hacia abajo hasta *Configuración de extensión*.
3. Escriba la configuración de ampliación utilizando el siguiente formato de JSON y, a continuación, pulse **Confirmar cambios** para guardar la configuración.

```  
    {
        "orange": {
            "serialnumber": "<número de serie de la SIM de Orange>"
        }
    }

```
Cuando la organización se ha configurado correctamente, se muestra la sección *Ampliaciones* debajo de la sección *Configuración de ampliaciones* de la vista *Detalle de dispositivo*.

## Almacenamiento de datos históricos
{: #historical_data}

La extensión de almacenamiento de datos históricos le permite ubicar y configurar servicios de almacenamiento de mensajes compatibles como, por ejemplo, [{{site.data.keyword.cloudantfull}}](../../cloudant_connector.html) o [{{site.data.keyword.messagehub_full}}](../../message_hub.html) para los datos de IoT.

## Paquetes personalizados de gestión de dispositivos
{: #device_mgmt}

La gestión de dispositivos es una característica principal de la {{site.data.keyword.iot_short_notm}}; sin embargo, se puede ampliar para desarrollar funciones adicionales.

La extensión de gestión de dispositivos le permite instalar funciones personalizadas para la gestión de dispositivos. Para obtener más información sobre las funciones de gestión de dispositivos personalizadas, consulte [extensiones personalizadas de gestión de dispositivos](../../devices/device_mgmt/custom_actions.html){: new_window}.

## Blockchain
{: #blockchain}

{{site.data.keyword.iot_short_notm}} con blockchain permite a los dispositivos de IoT proporcionar datos a transacciones de blockchain, lo que almacena los datos en el libro mayor inmutable de blockchain y los utiliza en reglas empresariales de contratos inteligentes. {{site.data.keyword.iot_short_notm}} correlaciona datos de dispositivo en el formato de datos que necesita el contrato inteligente de blockchain y los pasa a un tejido de blockchain para almacenarlos en el libro mayor de blockchain.

### Operaciones soportadas para Blockchain
- Desencadenar actualizaciones de contratos inteligentes con sucesos de dispositivo.
- Ejecutar la lógica empresarial de contratos inteligentes para actualizar el estado de libro mayor con datos de sucesos de dispositivos.
- Supervisar el blockchain, las transacciones y el estado del libro mayor con la IU de supervisión.

### Configuración para Blockchain

La integración de blockchain de {{site.data.keyword.iot_short_notm}} es una oferta de servicios que no está activada de forma predeterminada en {{site.data.keyword.iot_short_notm}}. Para activar la característica en el entorno, lleve a cabo los pasos siguientes:
 1. Desde el panel de control de {{site.data.keyword.iot_short_notm}}, **Extensiones**.
 2. Pulse el enlace **Más información** que hay junto a la extensión de Blockchain para ir a la página IoT Blockchain Services Offering.
 3. Rellene y envíe la solicitud de solicitud de servicio.   
La aprobación de servicio normalmente tarda, aproximadamente, un día. Una vez que se haya aprobado la solicitud, recibirá un correo electrónico con instrucciones sobre cómo activar la integración de blockchain en la organización de {{site.data.keyword.iot_short_notm}}.
 5. Vuelva al panel de instrumentos de {{site.data.keyword.iot_short_notm}} para que la organización finalice la configuración. Para obtener más información, consulte [Integración de blockchain de {{site.data.keyword.iot_short_notm}}](../../bl_blockchain_integration.html).

## The Weather Company
{: #weathercompany}

La extensión Weather Company combina información meteorológica con los dispositivos existentes de {{site.data.keyword.iot_short_notm}}. La información meteorológica de The Weather Company aparece en la vista de detalles del dispositivo si se ha realizado una solicitud Update Location mediante la API, o si el dispositivo ya ha establecido su ubicación mediante un mensaje de gestión de dispositivos.

**Nota:** Sólo los dispositivos gestionados pueden definir sus propias ubicaciones. Todos los dispositivos no gestionados deben tener sus ubicaciones establecidas manualmente mediante la API. Para obtener más información sobre cómo configurar una ubicación de dispositivo, consulte [Solicitudes Update Location](../../devices/device_mgmt/index.html#update-location).

### API REST para The Weather Company
Para acceder a la API REST para The Weather Company, consulte la sección sobre
Device Location Weather en la [documentación de API REST HTTP de {{site.data.keyword.iot_short_notm}}](https://docs.internetofthings.ibmcloud.com/swagger/v0002.html#!/Device_Location_Weather).

### Datos meteorológicos

Para ver los datos meteorológicos recuperados para una ubicación de dispositivo, busque el dispositivo en el panel **Dispositivos** y púlselo. En la vista de dispositivos detallada, desplácese hacia abajo hasta la sección **Extensiones**. Se enumerarán los siguientes datos meteorológicos:

- Información meteorológica actual.
- Temperatura actual.
- Temperatura máxima y mínima prevista.
- Humedad relativa.
- Presión.
- Visibilidad.
- Velocidad del viento.
- Dirección del viento.
- Latitud.
- Longitud.

<!-- Weather data from The Weather Company extension can be retrieved by using the API. For information on the Weather Company API, see [The Weather Company API documentation](https://docs.internetofthings.ibmcloud.com/swagger/ext-twc.html). -->
