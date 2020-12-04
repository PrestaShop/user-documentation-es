# La interfaz multitienda

## Gestionar tus tiendas <a id="Lainterfazmultitienda-Gestionartustiendas"></a>

La página "Multitienda" consta de tres secciones principales:

* **Árbol multitienda**. Te ofrece una visión general de tu grupo de tiendas, de tus tiendas, e incluso de las distintas URLs relacionadas con cada tienda.  De manera predeterminada, tan sólo hay una tienda disponible, en el grupo por defecto: la tienda principal.
* **Grupo de tiendas**. Enumera los grupos de tiendas disponibles. Puedes editarlos haciendo clic en el botón de acción 'Modificar' situado a la derecha.
* **Opciones multitienda**. Enumera las opciones disponibles para las tiendas existentes.  


  * **Tienda por defecto**. La tienda por defecto es la única que servirá como eje central para todas las demás, compartiendo sus detalles con otras tiendas \(productos, transportistas, etc.\), y es la única que aparece al iniciar sesión en el área de administración.

  ![](../../.gitbook/assets/54265610.png)

## Un único back-office para gobernarlas a todas <a id="Lainterfazmultitienda-Un&#xFA;nicoback-officeparagobernarlasatodas"></a>

Cuando la funcionalidad multitienda está activada en PrestaShop, muchos aspectos de PrestaShop pueden ser personalizados para cada tienda o grupo de tiendas.

Para ayudarte a establecer a cuál/es tiendas se aplican los cambios que realices, PrestaShop añade un selector desplegable en la parte superior de cada pantalla, donde puedes elegir el ámbito en los que quieres aplicar los cambios:

* Aplicar a todas tus tiendas en esta instalación de PrestaShop.
* Aplicar sólo a las tiendas del grupo de tiendas seleccionado.
* Aplicar sólo a la tienda seleccionada. 

![](../../.gitbook/assets/54265613.png)

Este selector de tiendas te ayuda a saber en qué tienda\(s\) está\(s\) trabajando actualmente.

Dicho esto, una vez que el modo multitienda está establecido correctamente, muchos de los ajustes más comunes sólo se pueden cambiar a nivel global \(todas las tiendas\), más concretamente los ajustes de configuración de las páginas: localización, preferencias, parámetros avanzados, administración, presentándose las opciones desactivadas en cualquier otra selección de tienda. Sin embargo, puedes optar por editar los ajustes de las configuraciones a un nivel más local \(por grupos de tienda o incluso por tienda individual\) si es necesario.

De hecho, las páginas de configuración presentan el look habitual cuando el selector de tienda está establecido en "Todas las tiendas", cosa que no ocurre en cualquier otra selección \(grupo de tiendas o tienda individual\) presentando estas opciones adicionales:

* Una opción "Sí/No" en la parte superior de cada sección de la página de configuración.
* Una casilla de verificación junto a cada opción.

![](../../.gitbook/assets/54265617.png)

Ambas tienen el mismo propósito: permitirre habilitar opciones que de otro modo estarían desactivadas en el contexto de la tienda actual. Puedes escoger las opciones que desees activar, o activar todas las opciones presentadas en una sección mediante el interruptor "Sí" de la opción Multitienda. Una vez activadas, te corresponde a ti establecer el valor de cada opción haciendo clic en su casilla de verificación o utilizando el interruptor "Sí/No" de cada una de ellas, lo que te permite cambiar el valor en ese contexto.  


No obstante, como podrás comprobar algunas de estas opciones no pueden editarse en un contexto local: se te indicará esta situación mediante un mensaje textual en pantalla: "No se puede cambiar el valor de este campo de configuración para esta tienda"

La siguiente tabla, indica si el elemento puede ser personalizado para una sola tienda individual, para un grupo de tiendas o para todas las tiendas al mismo tiempo.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Elemento</th>
      <th style="text-align:left">Para cada tienda</th>
      <th style="text-align:left">Para un grupo de tiendas</th>
      <th style="text-align:left">Para todas las tiendas</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Empleados</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Grupos de clientes</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Productos</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Precios</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Combinaciones y precios</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Idiomas</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; M&#xFA;ltiples im&#xE1;genes (<b>excepto para la imagen principal</b>)</td>
      <td
      style="text-align:left">X</td>
        <td style="text-align:left">X</td>
        <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>&#x2014; Cantidades disponibles para la venta, siempre que:</p>
        <ul>
          <li>La opci&#xF3;n &quot;Compartir cantidades disponibles para la venta&quot;
            se encuentre marcada para el grupo,</li>
          <li>El grupo no comparta sus cantidades disponibles para la venta con una
            tienda fuera del grupo.</li>
        </ul>
      </td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Toda otra informaci&#xF3;n (descripci&#xF3;n, etiquetas, URL
        amigable, etc.)</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Atributos y valores del cat&#xE1;logo</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Descuentos: reglas del carrito</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Descuentos: reglas de precios del cat&#xE1;logo</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Impuestos: Reglas de impuestos fiscales</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Categor&#xED;as (<b>excepto para la imagen principal</b>)</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Transportistas</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Almacenes</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Gesti&#xF3;n avanzada de stock</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Proveedores</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Marcas</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">P&#xE1;ginas con contenido est&#xE1;tico</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Contactos</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Pa&#xED;ses
        <br />El estado de un pa&#xED;s (activado o desactivado) es com&#xFA;n a todas
        las tiendas a los que est&#xE1; asociado</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Monedas</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Idiomas</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">M&#xF3;dulos</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Hooks (ganchos) y excepciones</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Activaci&#xF3;n/Desactivaci&#xF3;n</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Configuraci&#xF3;n (por ejemplo, credenciales de acceso a Paypal)</td>
      <td
      style="text-align:left">X</td>
        <td style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">M&#xF3;dulos de pago</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Restricciones por pa&#xED;s</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Restricciones por moneda</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x2014; Restricciones por grupo de clientes</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">URLs amigables</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Escenarios</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Cuenta de servicio web (webservice)</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left">X</td>
    </tr>
    <tr>
      <td style="text-align:left">Carrusel de im&#xE1;genes de la p&#xE1;gina principal</td>
      <td style="text-align:left">X</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

Notes

**Categorías**: Un producto sólo puede aparecer en una determinada categoría de una tienda si éste ha sido asociado a esta categoría en el contexto de la tienda. En otras palabras: si tienda A y tienda B tienen a la categoría C en común, nosotros podemos asociar el producto P a la categoría C para el contexto de la tienda A, y P no aparecerá en la categoría C de la tienda B.

**Transportistas**: Puedes gestionar la asociación de los transportistas para cada tienda, grupo de tiendas o para todas las tiendas; pero no personalizar un transportista para una tienda. Debes duplicar el transportista, si deseas utilizar el mismo transportista con diferentes rangos de precios en dos tiendas.

**Almacenes**: Aunque la gestión avanzada de existencias sólo puede ser utilizada por una sola tienda al mismo tiempo, los almacenes pueden ser utilizados por grupos de tiendas, por lo que sólo tienes que gestionar los almacenes para llevar un control avanzado de las existencias.

Para cada tienda, puedes fijar el precio específico para cada producto, compartir un parte o la totalidad del catálogo, cambiar las imágenes de los productos, etc.

Puedes optar por compartir las cuentas de los clientes entre tus tiendas, permitiendo a tus clientes utilizar sus credenciales para todas las tiendas, e incluso conectarse a cada una de tus tiendas de manera transparente.

A través del gestor avanzado de existencias, puedes gestionar con mayor precisión las asociaciones entre tus tiendas y tus almacenes.

