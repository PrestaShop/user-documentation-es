# Tus clientes

La primera página bajo el menú "Clientes" te ofrece un listado de todos los usuarios registrados en tu tienda.

![](../../../.gitbook/assets/54265149.png)

Ésta te proporciona a vista de pájaro una visión general de todos tus clientes, con algunos detalles que puedes utilizar para ordenar y buscar cuentas:

* **ID.** La identificación única adjunta al cliente.
* **Tratamiento \(Título social\)**. Los clientes pueden declarar su título social, que se corresponden a un género y que puede servirte de ayuda para ofrecer una experiencia más personalizada a tus clientes. Hay dos títulos sociales predeterminados \(Sr., y Sra.\), pero puedes crear todos los que considere necesarios desde la pestaña "Tratamientos" bajo la página "Ajustes sobre clientes" del menú "Parámetros de la tienda".
* **Nombre** y **Apellido**. El nombre del cliente.
* **Dirección email**. La dirección de correo electrónico que el cliente utilizó para registrarse en tu tienda.
* **Ventas**. Cuánto ha gastado el cliente en tu tienda hasta ahora.
* **Activado**. Indica si el cliente está activado o no. Puedes desactivar una cuenta haciendo clic en la marca de verificación de color verde.
* **Boletín**. Indica si el cliente está suscrito al boletín de noticias de la tienda o no. Puedes darle de baja, haciendo clic en la marca de verificación de color verde.
* **Ofertas de asociados**. Indica si el cliente de esta cuenta ha aceptado recibir e-mails de tus socios o no. Puedes darle de baja, haciendo clic en la marca de verificación de color verde. **No suscribas a un usuario a recibir estos mensajes de correo electrónico sin su consentimiento, ya que esto se considera spam**.
* Las fechas de Registro y de Última visita siempre pueden serte útiles para ordenar las cuentas de usuario.
* **Acciones**. Puedes modificar la cuenta del usuario, simplemente ver estas con detalle \(sus mensajes, pedidos, direcciones, cupones, etc.\), o eliminar ésta para siempre.

Cuando se instala Prestashop con datos de ejemplo, observarás que tienes un usuario predeterminado, llamado John DOE.

Puedes utilizar este falso cliente para probar algunas de las características de tu tienda, y navegar a través de ella para ver la forma en la que un cliente real lo haría.

Para iniciar sesión en tu tienda con esta cuenta pública, utiliza estas credenciales:

* Dirección de correo electrónico: [pub@prestashop.com](mailto:pub@prestashop.com)
* Contraseña: 123456789

**¡Antes de abrir tu tienda al público, asegúrate de eliminar este usuario por defecto, o por lo menos modifica sus credenciales!**. Si no realizas esto, algún visitante con malas intenciones puede utilizarlo para realizar compras falsas y provocar otros tipos de daños.

Bajo la tabla de los clientes se encuentra el botón "Establece los campos obligatorios para esta sección". Esto abre un formulario en el que puedes especificar si un campo de la base de datos es obligatorio o no marcando las casillas correspondientes: de esta manera, puede hacer que el campo "Ofertas de asociados", sea obligatorios cumplimentarlo o no cuando un cliente nuevo esté registrándose para comprar en tu tienda.

Puedes exportar una lista de tus clientes haciendo clic en el botón "Exportar" situado en la parte superior.  
También puedes importar los clientes utilizando el botón "Importar". Necesitarás para ello un archivo CSV que siga este formato:

```text
ID;Title;Last name;First Name;Email address;Age;Enabled;News.;Opt.;Registration;Last visit;
2;1;Gorred;Francis;francis@example.com;-;1;0;0;2013-07-04 15:20:02;2013-07-04 15:18:50;
1;1;DOE;John;pub@prestashop.com;43;1;1;1;2013-07-02 17:36:07;2013-07-03 16:04:15;
```

Más opciones de importación están disponibles en la página "Importación" del menú "Parámetros Avanzados".

## Crear una nueva cuenta de cliente <a id="Tusclientes-Crearunanuevacuentadecliente"></a>

Para crear manualmente una cuenta de cliente, haz clic en el botón "Añadir cliente". Un formulario aparecerá en pantalla.

![](../../../.gitbook/assets/54265152.png)

Rellena la información del cliente:

* **Tratamiento \(Título social\)**. Selecciona uno de entre los disponibles, o crea otro nuevo en la pestaña "Títulos" en la página "Ajustes sobre clientes" del menú "Parámetros de la tienda".
* **Nombre, Apellidos, Dirección de correo electrónico**. Estos datos son esenciales: los nombres se utilizan en los mensajes de correo electrónico de confirmación que PrestaShop envía, y la dirección de correo electrónico se utiliza para acceder al sistema.
* **Contraseña**. Elige una contraseña, de al menos 5 caracteres de longitud.
* **Fecha de nacimiento**. Esta información puede ser utilizada para enviar felicitaciones de cumpleaños y realizar descuentos temporales.  
  


  Si no deseas solicitar la fecha de nacimiento cuando un cliente crea una cuenta, puedes desactivar el campo de fecha de nacimiento en la página "Ajustes sobre clientes". Simplemente selecciona "No" para la opción "Solicitar fecha de nacimiento".

* **Activado**. Es posible que desees crear una cuenta, pero no desees activarla todavía.
* **Ofertas de asociados**. Puede ser utilizado por los módulos para enviar e-mails promocionales de sus socios a aquellos clientes que lo solicitaron. **No suscribas a un usuario a recibir estos mensajes de correo electrónico sin su consentimiento, ya que esto se considera spam**.
* **Acceso de grupo**. Tener grupos de clientes te permite crear descuentos para grupos específicos. Muchas otras características de PrestaShop también pueden ser restringidas por grupo.
* **Grupo de clientes predeterminado**. Aunque no importa el número de grupos a los que pertenece el cliente, éste siempre debe pertenecer a un grupo principal.  

Si tus clientes son mayoritariamente empresas, debes activar el modo B2B con el fin de obtener opciones adicionales: dirígete a la página "Ajustes sobre clientes" del menú "Parámetros de la tienda", y selecciona "Sí" para la opción "Activar modo B2B".

![](../../../.gitbook/assets/54265154.png)

El modo B2B añade algunos campos específicos para empresas:

* **Empresa**. l nombre de la empresa.
* **SIRET**. Su número SIRET \(solamente para Francia\).
* **APE**. Su código principal de actividad _Actividad principal ejercida_ -  solamente para Francia\).
* **Sitio Web**. Su sitio web.
* **Cantidad máxima pendiente permitida**. La cantidad de dinero en circulación que se permite a la empresa.
* **Número máximo de días para pagar**. El número de días que se le permite a la empresa pagar el préstamo de productos.
* **índice \(Calificación\) de riesgo**. Su calificación de riesgo para esta empresa: Ninguna, Baja, Media o Alta.

## Visualizar la información de un cliente <a id="Tusclientes-Visualizarlainformaci&#xF3;ndeuncliente"></a>

En caso de que desees obtener más información sobre un cliente determinado, puedes hacer clic en el botón "Ver", situado en el extremo de cada fila en la lista de clientes. Una nueva página aparecerá en pantalla.

![](../../../.gitbook/assets/54265156.png)

Las diversas secciones te proporcionan datos importantes sobre el cliente:

* **Información del cliente**: nombre y apellidos, dirección de correo electrónico, tratamiento \(título social\), fecha de registro, fecha de la última visita, índice de riesgo.
* Información relativa a la suscripción al boletín de noticias de la tienda y la suscripción a recibir información sobre empresas asociadas, la edad, la fecha de la última actualización, y si la cuenta está activa.
* **Notas privadas** de los empleados de la tienda \(es decir, tuyas o de su equipo\).
* **Mensajes** enviados por el cliente al equipo de la tienda \(a través del servicio de atención al cliente\).
* **Cupones** de descuento / reglas del carrito disponibles.
* **Últimas conexiones** a la tienda.
* Los **grupos** a los que pertenece el cliente.
* Resumen de los **pedidos** anteriores del cliente. Cantidad gastada, el método de pago utilizado, estado del pedido. Para obtener más información sobre cada pedido, haz clic en la fecha del pedido.
* **Carritos** que los clientes han creado \(pero no necesariamente han sido validados\) desde que se registraron en nuestra tienda. Cuando un cliente se encuentra visitando su cuenta, puedes visualizar lo que está añadiendo al carrito en tiempo real.
* Resumen de los productos que fueron pedidos por el cliente. Entre otras cosas, esto te permite saber cuándo al cliente le gusta un determinado producto, y tal vez crear un descuento especial para su décima compra. Al hacer clic sobre un producto serás redirigido al pedido al que ese producto está ligado.
* Una lista de los **productos más vistos** por el cliente. De la misma forma, puedes ver las páginas de productos que el cliente visitó en tu sitio web. Si el cliente no realiza el pedido después de haber visitado varias veces la página del producto, tal vez puedas ayudar al cliente a decidirse por la compra del producto, ofreciéndole un descuento dirigido.
* **Direcciones** registradas.  

## Búsqueda de clientes <a id="Tusclientes-B&#xFA;squedadeclientes"></a>

La búsqueda de un cliente en tu tienda PrestaShop puede hacerse de dos maneras diferentes.

**El primer método** consiste en introducir la información que tiene de él en la barra de búsqueda de PrestaShop, que se encuentra en la parte superior central de tu back-office. Selecciona "todo", "por nombre" o "por dirección IP", para realizar una búsqueda en base a:

* ID. Los números que se han asignado a los clientes en la base de datos.
* Nombre o apellido. Ten en cuenta que no puedes buscar por ambos: selecciona entre buscar "john" o "doe", ya que buscando por "john doe" no vas a encontrar resultados.
* Dirección de correo electrónico.
* Dirección IP. Puedes buscar utilizando la IP de la última conexión a tu tienda.

![](../../../.gitbook/assets/54265158.png)

Los resultados, si los hay, serán presentados: el listado que se le presenta contiene la ID del cliente, el tratamiento \(título social\), dirección de correo electrónico, fecha de nacimiento, fecha de registro en la tienda, la cantidad de pedidos realizados y si la cuenta del usuario está activa. Desde aquí, puedes acceder a la información completa de los clientes, o editar sus datos.

![](../../../.gitbook/assets/54265160.png)

**El segundo método** consiste en ir a la página "Clientes", y utilizar la lista de clientes.

![](../../../.gitbook/assets/54265164.png)  
En esta página, puedes completar los campos situados en la parte superior de la lista, con el fin de realizar un filtrado de acuerdo a los siguientes criterios: ID, título social, nombre, apellido, dirección de correo electrónico, edad, estado de la cuenta \(activado o desactivado\), suscripción al boletín de noticias, suscripción a recibir publicidad de sus asociados, fecha de registro en la tienda, y fecha de la última conexión realizada. Introduce sus criterios y haz clic en el botón "Filtrar" en la esquina superior derecha de la tabla. A continuación, puedes ordenar la lista en función de cada columna.

Haz clic en el botón "Reinicializar" para regresar al listado completo de clientes.

