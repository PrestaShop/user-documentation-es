# Correo electrónico

Tu tienda envía muchos mensajes desde que se inicia el proceso de registro hasta la realización de un pedido. Desde aquí puedes configurar cómo se enviarán los mensajes, y cuáles son los mensajes que fueron enviados.

## Correo electrónico <a id="Correoelectr&#xF3;nico-Correoelectr&#xF3;nico"></a>

La primera sección de la página se presenta con una lista de todos los correos electrónicos que fueron enviados desde PrestaShop, con el destinatario, la plantilla utilizada, el idioma del mensaje, el asunto del correo electrónico y el estado de la acción.

![](../../../.gitbook/assets/54265539.png)

## Correo electrónico <a id="Correoelectr&#xF3;nico-Correoelectr&#xF3;nico.1"></a>

Aquí es donde se decide cómo se envían y reciben tus e-mails.

El formulario tiene tres grupos de opciones:

![](../../../.gitbook/assets/54265542.png)

*  **Enviar e-mail a**. Este es un ajuste de front-end. Al final del proceso de compra, un cliente puede dejar un mensaje a tu personal de trabajo. Puedes optar por establecer quién recibirá estos mensajes enviados por tus clientes, seleccionando una de las opciones disponibles en la lista desplegable. Para añadir más direcciones, debes dirigirte a Parámetros de la tienda &gt; Contactos.
* Parámetros de correo electrónico: cómo son enviados técnicamente los correos electrónicos. Selecciona una de las tres opciones disponibles. Véase más abajo para obtener más información.
* Formato de correo electrónico: cómo son enviados visualmente los correos electrónicos. Selecciona una de las tres opciones disponibles. Véase más abajo para obtener más información.
* **Registro de emails**. Desactiva esta opción si ya no quieres hacer un seguimiento de los correos enviados por tu tienda, como se muestra en la sección de correo electrónico anterior.

### Configuración técnica <a id="Correoelectr&#xF3;nico-Configuraci&#xF3;nt&#xE9;cnica"></a>

Configurar PrestaShop para enviar correos electrónicos a tus clientes. Nosotros te aconsejamos que consulte a tu proveedor de alojamiento web para determinar qué ajustes de configuración utilizar para esta funcionalidad. Las opciones disponibles son:

* **Nunca enviar correos electrónicos \(utilizar para hacer pruebas\)**. Utiliza esta configuración para realizar pruebas. Una vez que tu tienda es pública, nunca debes utilizar esta configuración.
* **Utilizar la función mail\(\) de PHP \(recomendado; funciona en la mayoría de los casos\)**. Esta es la opción recomendada por defecto. En el caso de que ésta no funcione, entonces utiliza la opción SMTP.
* **Establecer mis propios parámetros SMTP. SÓLO para usuarios avanzados**. En este caso, aparece una nueva sección, con más campos para rellenar. La información para completar estos campos debe ser proporcionada por tu proveedor de hosting: nombre del dominio mail, servidor SMTP, usuario SMTP, etc. Asegúrate de transcribir exactamente la información que tu proveedor de hosting te indique.

La información de configuración SMTP debe ser proporcionada por una de estas entidades:

* Tu administrador del sistema,
* Tu host,
* Tu ISP,
* Tu proveedor de correo electrónico.

![](../../../.gitbook/assets/54265544.png)

Tu proveedor de alojamiento web puede indicarte si tu nombre de usuario es obligatorio o no, así como proporcionarte información sobre tu contraseña y el cifrado a utilizar.

Por ejemplo, en el caso de Gmail \(el servicio de correo electrónico ofrecido por Google\), debes introducir una información similar a la siguiente:

* Servidor SMTP: [smtp.gmail.com](http://smtp.gmail.com)
* Usuario SMTP: [mi.nombre.de.usuario@gmail.com](mailto:mi.nombre.de.usuario@gmail.com) \(ejemplo\)
* Contraseña SMTP: RT22UE87 \(ejemplo\)
* Cifrado: SSL
* Port: 465

### Configuración visual <a id="Correoelectr&#xF3;nico-Configuraci&#xF3;nvisual"></a>

Hay dos formatos disponibles para los correos electrónicos: HTML es el más agradable visualmente, pero puede que no funcione en todas partes; el formato texto es visualmente monótono, pero funciona en todas partes.

Puedes optar por utilizar sólo uno de los dos, o ambos. Se recomienda que utilices ambos formatos.

## Comprobar la configuración de correo electrónico <a id="Correoelectr&#xF3;nico-Comprobarlaconfiguraci&#xF3;ndecorreoelectr&#xF3;nico"></a>

Una vez que ha configurado tu dirección de correo electrónico utilizando uno de los dos métodos disponibles, introduce tu propia dirección de correo electrónico en esta sección, a continuación, haz clic en el botón "Enviar un email de prueba a".  
Ahora compruebea la bandeja de entrada de la dirección especificada, para verificar que has recibido el correo electrónico de prueba. Si no lo has recibido, modifica la configuración con la información correcta.

![](../../../.gitbook/assets/54265546.png)

