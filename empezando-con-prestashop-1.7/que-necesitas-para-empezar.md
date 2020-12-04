# ¿Qué necesitas para empezar?

## Instrucciones rápidas de configuración

Aquí tienes una lista rápida de lo que necesitas para empezar a instalar PrestaShop 1.7. Si te resulta incómodo que nos saltemos algunos detalles, encontrarás instrucciones detalladas en la sección siguiente.

* Requisitos del sistema:
  * PHP 5.4 o posterior.
    * Configuración útil \(en el archivo `php.ini`\): 
      * `allow_url_fopen` en On \(Activado\), 
      * `register_globals` en Off \(Desactivado\)`,`
      * `upload_max_filesize` en “16M” \(o más\).
    * Extensiones PHP obligatorias \(en el archivo `php.ini`\): PDO\_MySQL, cURL, SimpleXML, mcrypt, GD, OpenSSL, DOM, SOAP, Zip, fileinfo.
    * Herramientas de servidor útiles: cron/crontab, Memcached.
  * MySQL 5.0 o posterior.
  * Es mejor si utilizas: 
    * Alojamiento Unix/Linux.
    * Apache Web Server 2.0 o posterior, o nginx Web Server.
      * Configuración del módulo Apache: 
        * `mod_rewrite` activado, 
        * `mod_security` desactivado,
        * `mod_auth_basic` desactivado.
    * Mínimo 128 Mb de RAM exclusiva para PHP. Cuanto más, mejor.
* Códigos de acceso a tu servidor FTP y tu base de datos MySQL
  * Si no vas a hacer una instalación local, será el proveedor web quien deba proporcionarte los datos.
* Un editor de texto cualquiera.
* Un cliente FTP cualquiera.
* Un navegador web moderno cualquiera \(si usas Internet Explorer: mínimo IE9\).

También tienes que saber la URL de tu dominio mediante la que quieres que se acceda a tu tienda \(o tus tiendas\).

Consulta la página oficial de requisitos del sistema: [https://www.prestashop.com/es/requisitos-de-sistema](https://www.prestashop.com/es/requisitos-de-sistema).

Cuando lo tengas todo listo, puedes usar la [guía de instalación](instalar-prestashop.md).

## Instrucciones detalladas de configuración

PrestaShop es una aplicación web, lo que significa que hay que instalarla en un servidor web para que funcione. Además, necesita un nombre de dominio que tus visitantes usarán para acceder a tu tienda.

### Registro de un nombre de dominio

Antes de descargar o instalar nada, tienes que buscar un lugar donde alojar tu tienda online de PrestaShop. Para ello, necesitas un nombre de dominio y un servidor web. Un dominio es el identificador online de tu sitio web, como [ejemplo.com](http://example.com/) o [mitiendaonline.net](http://myonlineshop.net/). Es la cara pública de tu servidor web, y por tanto, también la de tu tienda.

Tienes que comprar un nombre de dominio para tu tienda. Muchos proveedores ofrecen un dominio gratuito con cada cuenta nueva, así que podrías adquirir uno cuando compres tu alojamiento web. Además, quizá sea gratis durante un año o mientras te mantengas como cliente de dicho proveedor. Esto facilita conseguir el paquete completo \(alojamiento + nombre de dominio\) de una vez.

Si hay un problema con los nombres de dominio que ofrece el proveedor y su servicio no te satisface, querrás cambiarte a uno mejor. Esto significa que tendrás que trasladar tus archivos, datos y nombre de dominio a ese otro proveedor.

Trasladar los archivos y los datos es sencillo, pero recuperar tu nombre de dominio puede resultar más complicado en según qué servidores. Técnicamente, el dominio les pertenece porque han sido ellos quienes han comprado el nombre de dominio para ti. Por tanto, pueden ocurrir dos cosas: que te prohíban que lo transfieras a otro proveedor, o que te pidan que lo pagues. Y dado que el nombre de dominio es tu marca y tu dirección en la web, no te queda otra que seguir las reglas del proveedor.

Por este motivo, solemos recomendar que adquieras tu nombre de dominio de un registrador independiente de nombres de dominio \(consulta: [https://es.wikipedia.org/wiki/Registrador\_de\_dominios](http://en.wikipedia.org/wiki/Domain_name_registrar)\). Desde un punto de vista técnico, nunca se puede comprar un nombre de dominio; solo puedes alquilarlo, la mayoría de las veces por una tarifa anual. Esto te da derecho a utilizar ese nombre de dominio, pero en cuanto dejes de pagarlo, deja de ser tuyo y cualquiera puede quedárselo para usarlo.

Además de pagar el registro del nombre de dominio, también tienes que pagar el alojamiento web. Pero, al menos, tienes libertad para trasladarte a un proveedor mejor cuando tú quieras y sin tener que pagar tarifas suplementarias: solo tienes que cambiar las direcciones DNS del nombre de dominio. El cambio se habrá extendido a todo el mundo en 24 horas.

Si quieres obtener tu nombre de dominio de un registrador independiente, estos son algunos de confianza:

* Gandi: [http://en.gandi.net/](http://en.gandi.net/)
* Namecheap: [http://www.namecheap.com/](http://www.namecheap.com/)
* GoDaddy: [https://www.godaddy.com/](https://www.godaddy.com/)
* 1&1 IONOS : [https://www.ionos.es](https://www.ionos.es/)

Hay muchos más. ¡Pregunta a tus amigos!

### Búsqueda de un proveedor

Ahora que tienes un nombre de dominio, tienes que hacer que señale a PrestaShop. Esto significa que los archivos de PrestaShop tienen que encontrarse en un servidor web. Puedes tener el tuyo propio, pero es más probable que hayas alojado o vayas a alojar tu tienda en un servicio de alojamiento de Internet \(consulta: [https://es.wikipedia.org/wiki/Servicio\_de\_alojamiento\_de\_Internet](https://es.wikipedia.org/wiki/Servicio_de_alojamiento_de_Internet)\), que te ofrece una espacio de almacenamiento online por una tarifa mensual o anual.

Lo primero que tienes que hacer antes de abrir una tienda online es seleccionar un proveedor de alojamiento. Prácticamente cualquier alojamiento web puede gestionar de forma eficaz la solución PrestaShop. Sin embargo, solo unos pocos proveedores de alojamiento ofrecen servidores optimizados para PrestaShop \(con instalación en 1 clic y versión actualizada\). Esta es nuestra[ lista de socios de alojamiento](https://www.prestashop.com/es/ecommerce-hosting).

A la hora de elegir tu alojamiento, recuerda un requisito fundamental: tiene que ser compatible con PHP 5.4 \(o más reciente\), el lenguaje de programación en el que está escrito PrestaShop, y MySQL 5 \(o más reciente\), el sistema de base de datos donde PrestaShop almacena todos sus datos. Pero hay más requisitos: consulta la sección “Requisitos técnicos” a continuación.

### Requisitos técnicos

PrestaShop es una aplicación escrita con lenguaje de programación PHP que se ejecuta en un servidor web y almacena sus datos en un servidor MySQL.

PHP es un lenguaje de programación de código abierto que se usa principalmente para aplicaciones web. Desde su creación en 1995, se ha convertido en el lenguaje de programación más utilizado por los desarrolladores web. Utiliza una sintaxis similar al lenguaje C, lo que facilita que los desarrolladores puedan aprenderlo.

MySQL es un sistema de gestión de bases de datos de código abierto. Desde su creación también en 1995, se ha convertido en el sistema de bases de datos más utilizado por los desarrolladores web. Se basa en SQL, el lenguaje de bases de datos más utilizado.

  
Elijas el servicio de alojamiento que elijas, tu servidor web debe tener instalados los siguientes componentes:

* **Sistema**: Unix, Linux o Windows. Recomendamos encarecidamente que sea Unix.
* **Servidor web**: Apache Web Server 2.0 o posterior.
* **PHP 5.4 o posterior**. Puede que tengas que activar PHP 5 \(consúltalo con tu proveedor de alojamiento\).
* **MySQL 5.0 o posterior**.
* Mínimo 128 Mb de RAM en tu servidor.

PrestaShop también puede funcionar con IIS Web Server 6.0 o posterior \(de Microsoft\) y nginx 1.0 o posterior.

Los administradores de sistemas pueden obtener más información en la [guía para administradores de sistemas](http://doc.prestashop.com/display/PS16/System+Administrator+Guide) \(en inglés\). ¡No olvides leerla!

### Herramientas

Necesitarás dos herramientas: un editor de texto \(para poder editar archivos de texto\) y un cliente FTP \(para transferir archivos de tu equipo a tu servidor y viceversa\).

#### Editor de texto

Estos son algunos de los editores de texto más famosos:

* Windows y OS X:
  * Sublime Text: [http://www.sublimetext.com/](http://www.sublimetext.com/)
  * Atom: [https://atom.io/](https://atom.io/)
* Unix/Linux:
  * Vim: [http://www.vim.org/](http://www.vim.org/)
  * Emacs: [http://www.gnu.org/software/emacs/](http://www.gnu.org/software/emacs/)

No utilices un procesador de textos cuando edites archivos de texto, como Microsoft Word o Write de [OpenOffice.org](http://openoffice.org/).

#### Cliente FTP

FTP es el acrónimo de “File Transfer Protocol”: la forma estándar que se usa para transferir archivos desde un ordenador a un proveedor web.

En esta guía usaremos FileZilla, un cliente fabuloso y gratuito para Windows, MacOS X y Linux. Descárgalo desde [http://filezilla-project.org/](http://filezilla-project.org/) y arranca su instalador. Nota: No descargues FileZilla Server, solo FileZilla Client.

Cuando hayas instalado FileZilla, tendrás que configurarlo con los parámetros de conexión de tu servidor web que debe haberte proporcionado tu proveedor. Si no tienes dichos datos, pídelos o consulta tu carpeta de spam.

Básicamente, los parámetros que necesitas son:

* **un nombre del servidor** o **una dirección IP**: la ubicación del servidor FTP del espacio de tu alojamiento.
* **un nombre de usuario**: el identificador de tu cuenta de alojamiento, exclusivo para tu persona.
* **una contraseña**: una medida de seguridad obligatoria.

Abre FileZilla y su herramienta Site Manager. Tienes tres formas de hacerlo:

* Pulsa Ctrl-S.
* En la esquina superior izquierda, haz clic en el icono “Open the Site Manager” \(Abrir Site Manager\).
* Abre el menú “File” \(Archivo\) y selecciona la opción “Site Manager...”.

Se abre una ventana.

Para añadir tu espacio de alojamiento en Site Manager:

1. Haz clic en el botón “New Site” \(Nuevo sitio\). Se crea una nueva entrada en la lista del sitio. Ponle un nombre reconocible.
2. En el lado derecho, en la pestaña “General”, introduce los parámetros que te ha proporcionado tu proveedor: alojamiento, usuario y contraseña. No cambies el resto de parámetros predeterminados a menos que te lo indique tu proveedor.
3. Cuando hayas rellenado todos los campos, haz clic en el botón “Connect” \(Conectar\). Esta acción guardará tu sitio en la lista y te permitirá acceder a tu cuenta para que compruebes que todo funciona correctamente.

Si FileZilla no termina de convencerte, aquí tienes otros clientes FTP conocidos:

* Windows:
  * CoreFTP: [http://www.coreftp.com/](http://www.coreftp.com/)
  * WinSCP: [http://winscp.net/](http://winscp.net/)
  * SmartFTP: [http://www.smartftp.com/](http://www.smartftp.com/)
* Mac OS X:
  * Cyberduck: [http://cyberduck.ch/](http://cyberduck.ch/)
  * Transmit: [http://www.panic.com/transmit/](http://www.panic.com/transmit/)
  * Fetch: [http://fetchsoftworks.com/fetch/](http://fetchsoftworks.com/fetch/)
* Unix/Linux:
  * gFTP: [http://gftp.seul.org/](http://gftp.seul.org/)
  * kasablanca: [http://kasablanca.berlios.de/](http://kasablanca.berlios.de/)
  * NcFTP: [http://www.ncftp.com/ncftp/](http://www.ncftp.com/ncftp/)

## Diseño de un plan

Ahora te toca decidir dónde quieres alojar PrestaShop. Puedes configurar tu nombre de dominio de cuatro formas:

* En la raíz del dominio: [http://www.ejemplo.com/](http://www.example.com/)
* En una carpeta: [http://www.ejemplo.com/tienda/](http://www.example.com/shop/)
* En un subdominio: [http://tienda.ejemplo.com/](http://store.example.com/)
* En una carpeta de un subdominio: [http://moda.ejemplo.com/boutique/](http://clothes.example.com/boutique/)

Ten en cuenta que, gracias a la función de multitienda, puedes tener tantas tiendas como sea necesario con una sola instalación de PrestaShop 1.7, cada una con su propio nombre de dominio específico, si fuera necesario. Tenlo en cuenta a la hora de decidir dónde va cada qué.  
 Sea cual sea tu plan, la tienda predeterminada siempre se encontrará donde se ubique PrestaShop.

## Instalación de PrestaShop

Por último, ahora que ya reunimos todos los requisitos, puedes pasar a la [guía de instalación](instalar-prestashop.md).

