---

copyright:
  years: 2016
lastupdated:  "2016-10-14"

---

#	Utilización del plan Professional Per Capacity
{: #using_mobilefoundation_p4}

Con el plan Professional Per Capacity, los usuarios pueden crear cualquier número de aplicaciones móviles con varios sistemas operativos móviles.
Tras crear la instancia del servicio {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity, consulte el procedimiento siguiente para iniciarse en el uso del servicio.

## Requisitos previos
{: #prerequisites_p4}

Tenga en cuenta lo siguiente antes de configurar la instancia del servicio {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity.
* {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity solo se admite con planes de {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dashdbshort_notm}}: Enterprise Transactional (con soporte para OLTP).

* Deberá tener acceso a las credenciales de la instancia de servicio {{site.data.keyword.dashdbshort_notm}} antes de poder configurar los valores de su instancia de servicio {{site.data.keyword.mobilefoundation_short}}.

**Nota**: La instancia de servicio {{site.data.keyword.dashdbshort_notm}} puede existir en cualquier `Espacio` dentro de la `Organización` de {{site.data.keyword.Bluemix_notm}} o de cualquier otra `Organización` a la que tenga acceso. Asegúrese de que dispone de los permisos para acceder al `Espacio` donde existe la instancia del servicio {{site.data.keyword.dashdbshort_notm}}.


## Adición de la conexión de base de datos
{: #configure_dashdb_p4}

###  Primeros pasos
{: #firststeps_p4}

Tras crear la instancia del servicio {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity, siga el procedimiento siguiente para iniciarse en el uso del servicio.

### Configuración de la conexión con la instancia de servicio {{site.data.keyword.dashdbshort_notm}}
{: #connect_dashdb_p4}

Una vez que se haya creado la instancia de servicio {{site.data.keyword.mobilefoundation_short}}: Professional Per Capacity, podrá ver la página *Visión general*, donde deberá especificar la información de conexión de la instancia de servicio {{site.data.keyword.dashdbshort_notm}}: Enterprise Transactional.

1. Seleccione la `Organización` de {{site.data.keyword.Bluemix_notm}} donde existe la instancia del servicio {{site.data.keyword.dashdbshort_notm}}.

+ Seleccione el `Espacio` de {{site.data.keyword.Bluemix_notm}} donde existe la instancia del servicio {{site.data.keyword.dashdbshort_notm}}, en la lista de espacios disponible en la `Organización` seleccionada.

**Nota:** Si no ve la `Organización` y el `Espacio` donde existe su instancia del servicio {{site.data.keyword.dashdbshort_notm}} consulte si es miembro de la `Organización` y del `Espacio`.

+ Seleccione el `Nombre de servicio` y las `Credenciales` de {{site.data.keyword.dashdbshort_notm}} para conectarse con la instancia de servicio {{site.data.keyword.dashdbshort_notm}} existente.

+  Pruebe la conexión con la instancia del servicio {{site.data.keyword.dashdbshort_notm}}: Enterprise Transactional especificada.

+  Pulse **Añadir**. Esta acción crea las tablas necesarias en la instancia de servicio de base de datos de {{site.data.keyword.dashdbshort_notm}} configurada.

**Nota**: no puede cambiar la instancia de servicio {{site.data.keyword.dashdbshort_notm}} que está configurada para que la utilice la instancia del servicio {{site.data.keyword.mobilefoundation_short}}. No obstante, puede utilizar la misma instancia de servicio {{site.data.keyword.dashdbshort_notm}} en varias instancias de servicio {{site.data.keyword.mobilefoundation_short}}, ya que cada instancia de servicio {{site.data.keyword.mobilefoundation_short}} crea su propio esquema en la instancia de servicio {{site.data.keyword.dashdbshort_notm}} seleccionada.

* En varios segundos, puede acceder a la página `Visión general`, que le ofrece guías de aprendizaje y vídeos para ayudarle a aprender a utilizar el servicio {{site.data.keyword.mobilefoundation_short}}.

## Inicio del servidor de {{site.data.keyword.mobilefirst}}
{: #start_mobilefoundation_p4}

* Para iniciar {{site.data.keyword.mfserver_short_notm}} con los valores predeterminados, pulse **Iniciar servidor básico**.

* Esta selección suministra un {{site.data.keyword.mfserver_long_notm}} con la configuración siguiente:
    -  2 nodos con 1 GB de memoria cada uno. Este tamaño es correcto para realizar actividades de desarrollo, de pruebas no muy exigentes y cargas de trabajo de producción a pequeña escala.

    -	El `nombre de usuario` y la `contraseña` se generan de forma automática. Tiene acceso a ellos cuando el servidor está en ejecución.

Se inicia el proceso de suministro del servidor. Este proceso dura unos 10 minutos y un mensaje indica el progreso de la operación. Una vez finalizado, se muestra un panel de instrumentos en el que se puede ver lo siguiente:

  -	El estado del servidor que se ejecuta (estado, tamaño).

  -	Se ha creado la ruta para el servidor. Utilice esta ruta en su aplicación móvil para conectarse a {{site.data.keyword.mfserver_short_notm}}.

  -	Su `nombre de usuario` y `contraseña` personal para acceder a la {{site.data.keyword.mfp_oc_short_notm}}. La `contraseña` está oculta. Pulse el icono **Mostrar contraseña** para visualizarla.

*	Pulse **Iniciar consola** para abrir la {{site.data.keyword.mfp_oc_short_notm}}.


<!--This console runs inside the container.--> Con la consola, puede gestionar sus aplicaciones móviles, adaptadores y dispositivos móviles, utilizar su servidor como programa de fondo móvil, enviar notificaciones push, etc.

##  Adición de servidor de Mobile Analytics
{: #adding_analytics_server_p4}

 Ahora puede supervisar su aplicación móvil en el servidor de {{site.data.keyword.mobilefirst}} añadiendo un servidor de Mobile Analytics a la instancia de servicio de {{site.data.keyword.mobilefoundation_short}}.

 El plan Professional crea el servidor de Mobile Analytics en un grupo de contenedores, el usuario puede personalizar la configuración seleccionando el número de nodos de contenedores en el grupo de contenedores.

 Los usuarios también pueden adjuntar volúmenes a los contenedores para persistir datos. El volumen seleccionado no se puede cambiar. 20 GB es el espacio de compartición de archivos predeterminado disponible para el usuario. Si el usuario necesita espacio de almacenamiento adicional para persistir datos analíticos, necesitará adquirir compartición de archivos adicional y crear un volumen utilizando esta compartición de archivos. Puede seleccionar este nuevo volumen al desplegar el servidor de análisis.

 Para obtener más información sobre cómo añadir volúmenes a {{site.data.keyword.containerlong}}, consulte [Almacenamiento de un volumen utilizando el Panel de control de {{site.data.keyword.Bluemix_notm}} ](https://console.ng.bluemix.net/docs/containers/container_volumes_ui.html){: new_window}.

* Pulse **Añadir analíticas** para añadir el servidor de Mobile Analytics a la instancia de servicio de {{site.data.keyword.mobilefoundation_short}}.

* Puede elegir la configuración del servidor de Mobile Analytics; la configuración mínima admitida para el servidor de Mobile Analytics es de 2 nodos con 1 GB cada uno, puede elegir crear un servidor de Mobile Analytics con una configuración máxima de 32 nodos con 16 GB cada uno.

Se inicia el proceso de suministro. Este proceso dura unos 10 minutos y un mensaje indica el progreso de la operación.  

* Inicie la consola de MobileFirst Analytics desde {{site.data.keyword.mfp_oc_short_notm}}.

* El inicio de sesión único está habilitado entre {{site.data.keyword.mfserver_short_notm}} y el servidor de Mobile Analytics. El servidor de Mobile Analytics está configurado con las mismas claves de LTPA y credenciales de usuario que el servidor de {{site.data.keyword.mfserver_short_notm}}. Puede utilizar el mismo `nombre_usuario` y `contraseña` para iniciar sesión en la consola de Mobile Analytics como se solía iniciar sesión en {{site.data.keyword.mfp_oc_short_notm}}.

Para obtener más información sobre MobileFirst Analytics, puede consultar [MobileFirst Foundation Operational Analytics](https://mobilefirstplatform.ibmcloud.com/tutorials/en/foundation/8.0/analytics/).

**Nota:** El servidor de Mobile Analytics se elimina al suprimir la instancia de servicio de {{site.data.keyword.mobilefoundation_short}} o al intentar volver a crear {{site.data.keyword.mfserver_short_notm}}.

## Recreación del servidor de {{site.data.keyword.mobilefirst}}
{: #recreate_mobilefoundation_p4}

*	Pulse **Recrear** para volver a crear el servidor.

* Esta acción detiene el servidor existente y suprime los datos. Se crea una nueva instancia con una versión actualizada, si está disponible. Esta acción tarda unos minutos en completarse.

**Nota**: todos los datos de su instancia de servidor anterior, incluyendo la información sobre aplicaciones y adaptadores, se conserva en la instancia del servicio {{site.data.keyword.dashdbshort_notm}} configurada; estos datos se utilizan para volver a crear el servidor.

##	Ajuste de la configuración avanzada
{: #using_mfs_advanced_p4}

Utilice la opción **Iniciar servidor con configuración avanzada** en la página `Visión general` para crear el servidor con valores avanzados o personalizados. También puede actualizar los valores del servidor para personalizar su configuración desde el separador **Configuración**. {{site.data.keyword.mobilefoundation_short}} le ofrece acceso a algunos valores avanzados.

*	Desde el separador **Topología**, puede seleccionar el tamaño del servidor y el número de instancias de servidor que necesita. El valor predeterminado del servidor es de 1 GB, que es suficiente para el desarrollo y la realización de pruebas no muy exigentes.
  - Seleccione el tamaño correcto para su servidor en función de sus necesidades.

  - **Nodos** muestra el número de nodos que se han creado.

      - Se puede crear una granja de servidores de {{site.data.keyword.mobilefirst}} configurando el número de nodos aquí. La configuración mínima admitida es de 2 nodos con 1 GB cada uno y la configuración máxima es de 32 nodos con 16 GB cada uno.

Consulte la [Documentación de {{site.data.keyword.mobilefoundation_long}}](https://www.ibm.com/support/knowledgecenter/SSHS8R_8.0.0/wl_welcome.html){: new_window}, para obtener más detalles.
