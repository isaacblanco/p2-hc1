# P2 - hc1

P2 for HTML &amp; CSS I

## Cambios

### La web debe contar con una cabecera (header) que incluya un título y un pequeño logotipo creado por ti

Se ha incluido un logo en la cabecera como un .svg, creado por mí. El fichero header.html ya existía, se requiere tener el fichero .posthtmlrc en el raiz con el contenido:

```json
{
  "plugins": {
    "posthtml-include": {
      "root": "./src"
    }
  },
  "removeComments": true,
  "minifySvg": false
}
```

Para que funcione correctemente.

**NOTA: el header no se muestra en la portada**

### La web debe contener un pie de página (footer) con enlaces a todas las páginas

Ya se contaba con el fichero **footer.html** que funciona de igual manera que el header.html.

Se ha incluido el mismo logotipo que en la cabecera. Es un .svg, con el peso minimo, y sin perdida de calidad en le escalado. Y enlaces a todas las páginas.

### Todas las imágenes de la web deben ser responsive y al menos debe haber una imagen por cada técnica de imágenes responsive.

Basandome en la referencia de: https://mdn.github.io/learning-area/html/multimedia-and-embedding/responsive-images/responsive.html

Veo que tiene dos opciones, el uso de picture con diferentes origenes o el uso de srcset y sizes.

```html
<picture>
  <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg" />
  <source media="(min-width: 800px)" srcset="elva-800w.jpg" />
  <img src="elva-800w.jpg" alt="Chris standing up holding his daughter Elva" />
</picture>

<img
  srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
  sizes="(max-width: 600px) 480px,800px"
  src="elva-fairy-800w.jpg"
  alt="Elva dressed as a fairy"
/>
```

### La web debe ser responsive

Se han aplicado las técnicas necesarias para que la página sea responsive.

### La web debe tener algunos elementos animados mediante transiciones y animaciones

Header: el mouse hover en los menús de la cabecera ya cuenta con efecto de animación:

```css
transition: all 0.2s ease-in-out;
```

Un listado de elementos animados incluidos en la web:

- Los enlaces de la home principales, tienen efecto de hover
- Los enlaces de los menús incorporan varias animaciones, dende color al redondeo del borde borde
- Los h1 se reducen de tamaño en un 4% en todas las páginas
- El clip-path de la home se mueve en el hover
- El svg incluye animaciones
- En el detalle la imagen del grupo muestra las camisetas al pasar sobre ellas
- En el footer los enlaces tienen un efecto de luminosidad

### La web debe cumplir las reglas básicas WCAG 2.1Links to an external site. A y AA de accesibilidad

https://validator.w3.org/ se ha revisado

## Portada

### Debe haber al menos un recurso gráfico editado con clip-path.

Se ha agregado una capa de opacidad con clip-path sobre la imagen principal, para mejorar el efecto del inicio, adicionalmente una imagen de fondo que con el hover hace que el clip-path se modifique en medio segundo.

## Página de detalle

### Hay que añadir una imagen destacada representativa del contenido que explica la página.

En este caso se ha optado por usar tres imágenes principales, para ajustar la resolución por estilos, que se sitúan justo debajo del título de la página.

### hay que añadir otras imágenes (como mínimo 2 más sin contar con el header y el footer)

Se han includo dos imagenes extras que se intercambian entre sí cuando el ratón se superpone sobre ellas.

### La imagen destacada debe incluir gestión de la dirección de arte

Si bien el album es el último publicado, la dirección de arte se puede enfocar a su promoción. Lo que justifica que este en esta y el resto de las pantallas.

## Página de la categoría

### La imagen destacada que hemos elegido para la página de detalle debe ser visible también en esta página.

Nota: si bien la he añadido, ya se considero en la pasada P1 la cabecera de forma general. No obstante, como se ha comentado, se añade la promoción del albúm en ella, como imagen destacada, se hara lo mismo en presentación.html

## Página de presentación

### En esta página debe haber al menos un recurso gráfico hecho con SVG. Este SVG debe tener una pequeña animación mediante CSS.

Se ha hecho un recuadro, con 4 lineas que se mueven, y el texto de DISTURBED sobre ello, que se puede intuir dependiendo de la combinación de tiempos de las líneas.

## Página de enlaces

### Derechos de autor

Se han incluido la ruta original de todas las imágenes de donde se han obtenido.

## Extras

### Inclusión del favicon

Se ha incluido el favicon, un fichero svg, creado por mí.
