# Instalar PrestaShop en su ordenador

Quizá quieras instalar PrestaShop en tu ordenador local, tanto si es para probarlo antes de invertir dinero en un servidor y un nombre de dominio como para personalizar tu tienda localmente antes de vertir tus modificaciones a la instalación de PrestaShop que ya tienes online.

Para instalar cualquier aplicación web localmente, primero tienes que instalar el entorno adecuado, como el servidor web Apache, el intérprete de lenguaje PHP, el servidor de base de datos MySQL e, idealmente, la herramienta phpMyAdmin. Esto se conoce como AMP: Apache + MySQL + PHP. Existe para muchos sistemas operativos; de ahí que se añada otra letra al acrónimo: WAMP \(Windows + Apache + MySQL + PHP\), MAMP \(Mac OS X + ...\) y LAMP \(Linux + ...\).

## Cómo elegir un paquete AMP <a id="InstalarPrestaShopensuordenador-C&#xF3;moelegirunpaqueteAMP"></a>

Esto requeriría un alto nivel técnico, pero por suerte, existen muchos paquetes ya preparados que puedes instalar fácilmente. Esto no quita que tengas que ser técnico aquí y allá, pero desde luego son de lo más útil. Puesto que todos los paquetes son de código abierto, estos instaladores suelen ser gratuitos la mayoría de las veces. Aquí tienes una selección de instaladores AMP gratuitos:

* EasyPHP: [http://www.easyphp.org/](http://www.easyphp.org/) \(Windows\)
* MAMP: [http://www.mamp.info/](http://www.mamp.info/) \(Mac OS X\)
* WampServer: [http://www.wampserver.com/en/](http://www.wampserver.com/en/) \(Windows\)
* XAMPP: [http://www.apachefriends.org/en/xampp.html](http://www.apachefriends.org/en/xampp.html) \(Windows, Mac OS X, Linux, Solaris\)

Elige el paquete que te resulte más cómodo y ejecútalo.

## Cómo comprobar que todo funciona <a id="InstalarPrestaShopensuordenador-C&#xF3;mocomprobarquetodofunciona"></a>

Antes de continuar con este tutorial de instalación de PrestaShop, asegúrate de que todos los componentes de tu paquete AMP funcionan correctamente:

* **El servidor web tiene que estar en marcha**. Deberías poder acceder a él a través de tu navegador escribiendo “127.0.0.1” en la barra de direcciones.

[http://127.0.0.1](http://127.0.0.1/) es el “servidor local”, es decir, “tu ordenador”: es una dirección de bucle invertido que dirige el navegador a tu servidor web local.  
En efecto, [http://127.0.0.1](http://127.0.0.1/) y [http://localhost](http://localhost/) son sinónimos: puedes usarlos indistintamente, ya que ambos te dirigen a la carpeta raíz de tu servidor web local.

Algunos servidores web podrían no arrancar debido a que hay otra aplicación que ya está usando sus puertos de conexión \(normalmente, el puerto 80\).

Esto suele ocurrir cuando se utiliza Skype. Para evitar que Skype bloquee el funcionamiento de tu servidor web, visita la configuración avanzada de Skype \(Herramientas &gt; Opciones &gt; Avanzada &gt; Conexiones\) y desmarca la opción “Usar los puertos 80 y 443 para las conexiones entrantes adicionales”. Reinicia Skype y vuelve a iniciar tu servidor web local.

* **El servidor de la base de datos tiene que estar en marcha**. Los datos de PrestaShop se almacenan en MySQL. El paquete AMP tiene que indicarte claramente si MySQL está funcionando o no.
* **Debes poder acceder a la herramienta phpMyAdmin**. Esta es la aplicación web que te permite gestionar los datos almacenados en MySQL. Su ubicación depende del paquete AMP que elijas: puedes encontrarla en [http://127.0.0.1/phpmyadmin](http://127.0.0.1/phpmyadmin) \(XAMPP, WampServer, MAMP\), en [http://127.0.0.1/mysql](http://127.0.0.1/mysql) \(EasyPHP\) o en otra ubicación. Consulta la documentación de tu paquete, ya que podría proporcionarte incluso un botón phpMyAdmin que abriría la URL correcta en tu navegador.

## Cómo encontrar la carpeta raíz en el servidor web local <a id="InstalarPrestaShopensuordenador-C&#xF3;moencontrarlacarpetara&#xED;zenelservidorweblocal"></a>

Cuando hayas comprobado que el paquete está instalado correctamente y que todos sus componentes están funcionando, tienes que encontrar la carpeta raíz de tu servidor web local.

Esta es la carpeta local donde colocarás los archivos de tu aplicación. Puede compararse con la carpeta raíz de tu servidor web online, solo que accedes a su contenido con [http://127.0.0.1](http://127.0.0.1/).

La ubicación local real de la carpeta depende enormemente del paquete AMP, y puede personalizarse:

* EasyPHP: `C:\easyphp\www`
* MAMP: `/Applications/MAMP/htdocs/`
* WampServer: `C:\easyphp\www`
* XAMPP: `C:\xampp\htdocs` o `/Applications/xampp/htdocs`

## Cómo encontrar la información del usuario MySQL <a id="InstalarPrestaShopensuordenador-C&#xF3;moencontrarlainformaci&#xF3;ndelusuarioMySQL"></a>

Por último, tienes que conocer el nombre de usuario raíz y la contraseña de MySQL para poder instalar PrestaShop.

**La mayoría de los paquetes utilizan el nombre de usuario “root” con una contraseña vacía**, entre ellos EasyPHP, MAMP, WampServer y XAMPP.

Lee la documentación de tu paquete.

## Nota final antes del tutorial de instalación <a id="InstalarPrestaShopensuordenador-Notafinalantesdeltutorialdeinstalaci&#xF3;n"></a>

Con todo eso claro y hecho, ya puedes continuar con el resto de esta guía de iniciación y empezar a instalar PrestaShop.

Ten en cuenta lo siguiente cuando instales PrestaShop en local:

* los archivos no se cargarán mediante un software FTP \(como FileZilla\) a un servidor web: solo tienes que moverlos a la carpeta local correspondiente, tal como hemos indicado anteriormente.
* No tienes que crear un nombre de dominio local: tal como comentábamos, PrestaShop está disponible mediante la dirección de bucle inverso que hemos comentado anteriormente, que puede ser [http://localhost](http://localhost/) o [http://127.0.0.1](http://127.0.0.1/). Para acceder a PrestaShop como tal en esta dirección, solo tienes que añadir el nombre de su carpeta, por ejemplo [http://localhost/prestashop](http://localhost/prestashop) o [http://127.0.0.1/prestashop](http://127.0.0.1/prestashop), suponiendo que PrestaShop esté en la subcarpeta `/prestashop/` de la carpeta raíz local. Cuando accedas a esta dirección por primera vez, se te debería redirigir automáticamente a la instalación de PrestaShop en [http://localhost/prestashop/install](http://localhost/prestashop/install) o [http://127.0.0.1/prestashop/install](http://127.0.0.1/prestashop/install).

¿Lo has leído todo? Ahora sigue la guía de instalación, empezando por la sección “Creación de una base de datos para tu tienda”: [Instalación de PrestaShop](instalar-prestashop.md).

