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

Se han aplicado

### La web debe tener algunos elementos animados mediante transiciones y animaciones

Header: el mouse hover en los menús de la cabecera ya cuenta con efecto de animación:

```css
transition: all 0.2s ease-in-out;
```

### La web debe cumplir las reglas básicas WCAG 2.1Links to an external site. A y AA de accesibilidad

https://achecker.ca/checker

## Portada

### Debe haber al menos un recurso gráfico editado con clip-path.

Se ha agregado una capa de opacidad con clip-path sobre la imagen principal, para mejorar el efecto del inicio, adicionalmente una imagen

## Página de detalle

### Hay que añadir una imagen destacada representativa del contenido que explica la página.

En este caso se ha optado por usar tres imágenes principales, para ajustar la resolución por estilos.

### hay que añadir otras imágenes (como mínimo 2 más sin contar con el header y el footer)

### La imagen destacada debe incluir gestión de la dirección de arte

## Página de la categoría

### La imagen destacada que hemos elegido para la página de detalle debe ser visible también en esta página.

## Página de presentación

### En esta página debe haber al menos un recurso gráfico hecho con SVG. Este SVG debe tener una pequeña animación mediante CSS.

## Página de enlaces

### Derechos de autor

## Extras

### Inclusión del favicon

Se ha incluido el favicon, un fichero svg, creado por mí.
