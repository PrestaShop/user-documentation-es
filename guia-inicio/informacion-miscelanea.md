# Información miscelánea

## ¡Ten a mano una versión de prueba! <a id="Informaci&#xF3;nmiscel&#xE1;nea-&#xA1;Tenamanounaversi&#xF3;ndeprueba!"></a>

Cuando hayas terminado de configurar tu tienda y dejarla a tu gusto, pero antes de abrirla oficialmente al público, te recomendamos **encarecidamente** que instales una versión de prueba local en tu ordenador personal \(con [WAMP](http://en.wikipedia.org/wiki/Comparison_of_WAMPs) para Windows, [MAMP](http://en.wikipedia.org/wiki/MAMP) para Mac o [LAMP](http://en.wikipedia.org/wiki/LAMP_%28software_bundle) para Linux, o [XAMPP](http://www.apachefriends.org/en/xampp.html) para cualquier otra plataforma\), o en cualquier otro lugar de tu servidor de alojamiento.

Esta segunda instancia será útil como entorno de preproducción. En ella puedes hacer todos los cambios futuros de tu tienda online PrestaShop sin que afecte a la versión activa. De este modo, si algo falla, la tienda activa seguirá estando intacta.

Una vez que confirmes que tu versión de prueba funciona como debe, cópiala para sobrescribir la versión activa. Es mejor que lo hagas cuando pasen las horas punta de uso; además, también es recomendable que desactives temporalmente la tienda desde el back‑office.

## Comprobación de la biblioteca GD <a id="Informaci&#xF3;nmiscel&#xE1;nea-Comprobaci&#xF3;ndelabibliotecaGD"></a>

La [biblioteca GD](http://www.boutell.com/gd/) permite que PrestaShop retoque las imágenes que cargas, sobre todo para cambiar su tamaño.

En una instalación predeterminada de PHP, se debería activar la biblioteca GD; pero, si no es el caso de tu instalación, las instrucciones estándar de Windows son:

1. En el directorio raíz de tu carpeta PHP, abre el archivo `php.ini`.
2. Elimina el comentario de la línea `extension=php_gd2.dll` \(hacia la mitad del archivo aproximadamente, en medio de una larga lista de extensiones\) quitando el “;” que hay al inicio de la línea.
3. Reinicia los servicios PHP.

Si no tienes acceso al archivo `php.ini` \(que suele ser el caso si se usa alojamiento compartido\), ponte en contacto con tu proveedor para ponerle al tanto de tus necesidades de alojamiento.

## Activación de PHP 5 <a id="Informaci&#xF3;nmiscel&#xE1;nea-Activaci&#xF3;ndePHP5"></a>

Con frecuencia, tanto los servidores exclusivos como los compartidos disponen de PHP 4 y PHP 5, pero solo PHP 4 está activado de forma predeterminada.

Para instalar PrestaShop, se debe activar PHP 5. Si intentas ejecutar PrestaShop con PHP 4, recibirás numerosos errores, incluyendo este habitual mensaje de error:

```text
Parse error: parse error, unexpected T_STATIC, expecting T_OLD_FUNCTION or T_FUNCTION or T_VAR or '}' in [php file] on line X.
```

No dudes en publicar un informe de errores sobre los consejos que necesites para que PrestaShop funcione en tu servicio de alojamiento en [Forge](http://forge.prestashop.com/) de PrestaShop \(necesitarás una cuenta\). Los añadiremos a esta guía conforme los recibamos.

A continuación incluimos una lista de procedimientos que ya conocemos:

### 1&1 IONOS <a id="Informaci&#xF3;nmiscel&#xE1;nea-1&amp;1IONOS"></a>

Añade esta línea a tu archivo `.htaccess`:

```text
AddType x-mapp-php5 .php
```

Para la reescritura de la URL, añade estas líneas:

```text
Options +FollowSymLinks
RewriteEngine On
```

### OVH <a id="Informaci&#xF3;nmiscel&#xE1;nea-OVH"></a>

Añade esta línea a tu archivo `.htaccess`:

```text
SetEnv PHP_VER 5
```

Para desactivar las variables globales:

```text
SetEnv REGISTER_GLOBALS 0
```

### GoDaddy <a id="Informaci&#xF3;nmiscel&#xE1;nea-GoDaddy"></a>

Para ver tu versión de PHP:

1. Inicia sesión en tu administrador de cuentas.
2. En la sección Products \(Productos\), haz clic en Web Hosting \(Alojamiento web\).
3. Junto a la cuenta de alojamiento que quieras usar, haz clic en Launch \(Ejecutar\).

En la sección Server \(Servidor\), se muestra tu versión de PHP.

Para cambiar tu versión PHP:

1. En el menú Content \(Contenido\), selecciona Programming Languages \(Lenguajes de programación\).
2. Selecciona la versión de PHP que quieras usar y haz clic en Continue \(Continuar\).
3. Haz clic en Update \(Actualizar\).

Los cambios pueden tardar hasta 24 horas en completarse.

### Alojamiento compartido de Lunarpages <a id="Informaci&#xF3;nmiscel&#xE1;nea-AlojamientocompartidodeLunarpages"></a>

1. Entra en cPanel. Debería estar ubicado en [http://www.\(su\_dominio\).\(com/net/org/etc\)/cpanel](http://www.%28su_dominio%29.%28com/net/org/etc%29/cpanel)
2. Introduce el nombre de usuario de tu cuenta y la contraseña en el cuadro que aparece.
3. Aparece una nueva página. Desplázate hasta la fila inferior de iconos de la página y haz clic en el icono titulado “Enable/Disable PHP 5” \(Activar/Desactivar PHP 5\).
4. Aparece una nueva página. Haz clic en “Add PHP 5 To Your Account!” \(Añadir PHP 5 a tu cuenta\).

Se ha enviado tu solicitud de cambio de lenguaje. Deja pasar 24 horas para que el servidor de alojamiento procese el cambio.

