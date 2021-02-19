# Ejemplo de usos y especificaciones del modo multitienda

Ejemplo de usos y especificaciones del modo multitienda:

* [Gestionar un catálogo en modo multitienda](ejemplo-de-usos-y-especificaciones.md#gestionar-un-catalogo-en-modo-multitienda)
* [Intercambio de datos entre las tiendas](ejemplo-de-usos-y-especificaciones.md#intercambio-de-datos-entre-las-tiendas)
  * [Duplicar datos entre tiendas](ejemplo-de-usos-y-especificaciones.md#duplicar-datos-entre-tiendas)
  * [Compartir datos entre las tiendas y los grupos de tiendas](ejemplo-de-usos-y-especificaciones.md#compartir-datos-entre-las-tiendas-y-los-grupos-de-tiendas)
  * [Compartir productos y categorías](ejemplo-de-usos-y-especificaciones.md#compartir-productos-y-categorias)
  * [Compartir clientes y grupos de clientes](ejemplo-de-usos-y-especificaciones.md#compartir-clientes-y-grupos-de-clientes)
  * [Compartir pedidos](ejemplo-de-usos-y-especificaciones.md#compartir-pedidos)
  * [Utilizar un tema diferente para cada tienda o grupo de tiendas](ejemplo-de-usos-y-especificaciones.md#utilizar-un-tema-diferente-para-cada-tienda-o-grupo-de-tiendas)
  * [Utilizar configuraciones específicas para cada tienda o grupo de tiendas](ejemplo-de-usos-y-especificaciones.md#utilizar-configuraciones-especificas-para-cada-tienda-o-grupo-de-tiendas)
* [Gestionar páginas en modo multitienda](ejemplo-de-usos-y-especificaciones.md#gestionar-paginas-en-modo-multitienda)
* [Gestionar descuentos en modo multitienda](ejemplo-de-usos-y-especificaciones.md#gestionar-descuentos-en-modo-multitienda)
* [Multitienda y Servicio Web \(webservice\)](ejemplo-de-usos-y-especificaciones.md#multitienda-y-servicio-web-webservice)

## Gestionar un catálogo en modo multitienda

En modo multitienda, algunas páginas de administración de PrestaShop presentan un menú desplegable, titulado "Configuración para multitienda". Este menú te permite seleccionar el contexto para lo que está haciendo: lo que te permite establecer la tienda o grupo de tiendas a las que se aplicará el cambio que estás realizando.

Por ejemplo, al crear un nuevo producto, la selección que realices en este menú determinará si el producto estará disponible para todas las tiendas, sólo para un grupo de tiendas, o en una sola tienda.

Durante la edición de un producto, PrestaShop muestra notificaciones para ayudarte a entender el alcance de los cambios. Por ejemplo, al modificar un producto en el contexto "Tienda A", la notificación mostrará el siguiente mensaje: "¡Advertencia! Si cambias el valor de los campos con una viñeta naranja, el valor será cambiado en todas las tiendas en donde se encuentre este producto", mostrando dicha viñeta de color naranja en todos los campos implicados, tales como "Tipo de producto", "Referencia", tamaño del paquete, etc.

Del mismo modo, si cambias un producto en el contexto "Todas las tiendas" o en el contexto de un grupo de tiendas, algunos campos serán desactivados: dados que esto tienen un impacto global, no podrás editarlos. Si realmente necesitas editar este contenido, cada campo tiene una casilla que puedes marcar para editar esos campos en todas las tiendas que se encuentren bajo este contexto.

Si modificas un campo desactivado, el producto es creado en todas las tiendas del contexto que todavía no tengan a éste en su propio catálogo. Asegúrate de comprobar el contexto antes de realizar esta acción.

## Intercambio de datos entre las tiendas

### Duplicar datos entre tiendas

Los datos duplicados en PrestaShop son establecidos durante la instalación de cualquier tienda individual, importando todos o algunos de los contenidos de una tienda existente a otra nueva. El contenido que puede ser importado es variado: productos, categorías, empleados, módulos, reglas de carrito, proveedores, etc. La importación de datos se realiza de una vez por todas: una vez la tienda ha sido creada, no puedes volver a importar datos de otra tienda - al menos tan fácilmente.

### Compartir datos entre las tiendas y los grupos de tiendas

Las tiendas pueden compartir datos. Los datos compartidos se gestionan fundamentalmente entre las tiendas a nivel de grupo: uno de los aspectos más importantes a comprender en el modo multitienda de PrestaShop es que todas las tiendas dentro del mismo grupo de tiendas pueden compartir sus datos – o más concretamente, tres tipos de contenidos: clientes, cantidades disponibles, y pedidos. Una vez que el grupo de tiendas está configurado, el intercambio de datos entre las tiendas finaliza: aunque puedes cambiar la configuración para las cantidades de productos disponibles, no puedes cambiar la configuración de los clientes y los pedidos a partir del momento en que una de las tiendas de este grupo tenga un cliente o un pedido.

### Compartir productos y categorías

Al crear una nueva tienda dentro de un grupo, puedes hacer que todas o algunas de las categorías en la nueva tienda sean copias exactas de las categorías de otra tienda instalada en PrestaShop.

Al crear una categoría, para una tienda específica o para todas las tiendas instaladas, PrestaShop registra la categoría para todas las tiendas – simplemente se oculta en cualquier tienda en la que ésta no haya sido establecida.

Al asociar las nuevas tiendas, con una categoría determinada, cualquier cambio en esta categoría tendrá un impacto en todas las tiendas que están asociadas con ella, incluso si las tiendas pertenecen a grupos de tiendas diferentes. Puedes cambiar el contenido de la categoría de una sola vez para todas las tiendas, incluyendo sus productos.

### Compartir clientes y grupos de clientes

Como se indicó anteriormente, las tiendas dentro de un mismo grupo de tiendas pueden compartir clientes: todo lo que tienes que hacer es establecer la opción adecuada al momento de crear el grupo de tiendas.

Los grupos son menos detallados: si cambias uno de los grupos de clientes de forma predeterminada en una tienda, el cambio se aplicará a todas las tiendas, cualesquiera que sean tus grupos de tiendas.

Si quieres tener diferentes grupos de clientes para cada tienda, debes crear un nuevo grupo y utilizar el selector "Configuración multitienda para" con el fin de asociar el grupo a una tienda o a un grupo de tiendas.

Si la opción "Compartir clientes" ha sido desactivada, la lista de clientes tendrá que estar vacía antes de activarla.

Si prefieres mantener su listado de clientes, puedes hacer lo siguiente:

* Dirígete al software de gestión de bases de datos que utilices, como phpMyAdmin.
* Busca la tabla `ps_customer`. Puede tener un nombre diferente, dependiendo del prefijo que hayas establecido a la base de datos.
* Exporta esta tabla.
* Vacía la tabla. NO la elimines. Si deseas eliminarla, asegúrate de volver a crear la tabla después.
* Regresa a la configuración multitienda para el grupo de tiendas.
* Activa la opción "Compartir clientes".
* Importa la tabla.

En estos momentos, has activado compartir clientes entre el grupo de tiendas, sin tener pérdidas de información de clientes.

### Compartir pedidos

Es posible que las tiendas del mismo grupo de tiendas compartan pedidos: todo lo que tienes que hacer, es establecer la opción adecuada al crear el grupo de tiendas.

Si la opción "Compartir pedidos" ha sido desactivada, su listado de pedidos deberá estar vacío antes de poder activarla.

Si prefiere mantener su lista de pedidos, puede hacer lo siguiente:

* Dirígete al software de gestión de bases de datos que utilices, como phpMyAdmin.
* Busca la tabla `ps_order`. Puede tener un nombre diferente, dependiendo del prefijo que hayas establecido a la base de datos.
* Exporta esta tabla.
* Vacía la tabla. NO la elimines. Si deseas eliminarla, asegúrate de volver a crear la tabla después.
* Regresa a la configuración multitienda para el grupo de tiendas.
* Activa la opción "Compartir pedidos".
* Importa la tabla.

En estos momentos, has activado compartir pedidos entre el grupo de tiendas, sin tener pérdidas de información de pedidos.

### Utilizar un tema diferente para cada tienda o grupo de tiendas

Una vez que un tema está instalado en tu instalación de PrestaShop, puedes utilizar la página "Tema y Logotipo" en el menú "Diseño" para cambiar el tema de la tienda actual, o del grupo de tiendas actual, dependiendo de cómo esté establecido el selector "Configuración multitienda para".

### Utilizar configuraciones específicas para cada tienda o grupo de tiendas

El selector "Configuración multitienda para" es la opción a la que debes dirigirte cuando quieras que tus modificaciones tengan un impacto sobre una tienda determinada o un conjunto de tiendas. Incluso debería ser la primera opción que veas al cargar la pantalla de administración, ya que PrestaShop cambiará las opciones disponibles dependiendo del contexto en el que te encuentres: tienda, grupo de tiendas o todas las tiendas.

Esto hace posible:

* Utilizar un formato de imagen diferente para cada tienda / grupo de tiendas.
* Activar / configurar un módulo en base a una tienda.
* Posicionar / mostrar bloques en el front-office en base a una tienda.
* ...¡y mucho más!.

## Gestionar páginas en modo multitienda

Al visualizar el listado de páginas con contenido estático en el contexto "Todas las tiendas", se muestran todas las páginas de todas las tiendas. Del mismo modo, cuando se está en un contexto de grupo de tiendas, se muestran las páginas para todas las tiendas de ese grupo.

Cuando se crea una página en un contexto de grupo de tiendas, todas las tiendas existentes en ese grupo se muestran en esta página, aunque la página sea única: al modificar ésta para una tienda se modificará en todas las tiendas de ese grupo.  
En la página de creación, una sección aparece con una lista, indicando cuáles de ellas se verán afectadas.

## Gestionar descuentos en modo multitienda

Al crear reglas de compra o reglas del catálogo en un contexto multitienda, una condición adicional estará disponible, con la que puedes elegir las tiendas en las que este descuento estará disponible.

## Multitienda y Servicio Web \(webservice\)

El acceso al servicio web \(webservice\) también es altamente configurable, tanto a nivel de tienda como a nivel de grupo de tiendas. Al crear una clave de servicios web, puedes elegir asociar ésta a todas las tiendas, a algunos grupos de tiendas, o a tiendas individuales.

