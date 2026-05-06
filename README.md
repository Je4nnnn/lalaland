# Foro de moda de Kim Taehyung

Sitio web informativo con formato de foro sobre los momentos de moda de Kim Taehyung, V de BTS, durante 2025. El contenido se basa en el PDF entregado, que resume looks de Celine, Bode, Song For the Mute y otras referencias de moda masculina moderna.

El proyecto esta construido como una pagina estatica con HTML y CSS. No requiere instalacion de dependencias ni proceso de compilacion.

## Estructura del proyecto

```text
lalaland/
|- index.html
`- assets/
   |- css/
   |  `- styles.css
   `- img/
      |- featured.jpg
      |- news1.jpg
      |- news2.jpg
      |- news3.jpg
      `- news4.jpg
```

## Contenido del sitio

La pagina presenta:

- Un encabezado con el tema del foro y el titulo principal.
- Una franja superior con 4 imagenes fijas, reemplazando la idea inicial de una ruleta.
- Una publicacion fijada que introduce el tema con tono de foro.
- Un bloque visual tipo collage con imagenes superpuestas y tarjetas de conversacion.
- Una frase destacada en un cuadro azul para separar la introduccion de las entradas principales.
- Ocho entradas principales, cada una con foto, fuente pequena bajo la imagen y descripcion en un cuadro lateral.
- Informacion sobre 8 momentos de moda de Taehyung en 2025: alta costura, craftcore, nostalgia vintage, cuero, tejido arquitectonico, lujo discreto y estilo retro.

## Tecnologias usadas

- HTML5 semantico.
- CSS3 organizado con variables.
- Diseno responsive con `grid`, elementos `inline-block` y media queries.
- Imagenes locales en `assets/img/`.
- Posicionamiento CSS `relative` y `absolute`.
- Uso de etiquetas `div`, `p`, `h1`, `h2`, `header`, `main`, `section`, `article`, `aside` y `footer`.

## Uso de posicionamiento CSS

El proyecto usa `position: relative` para crear contextos de posicionamiento y `position: absolute` para ubicar elementos dentro de esos contextos, tal como se pidio para la evaluacion.

### Relative

- `.forum-header`: bloque principal del titulo del foro.
- `.top-thread`: contexto para la etiqueta `4 imagenes fijas`.
- `.fixed-image`: contexto para las etiquetas de cada imagen superior.
- `.thread-intro`: contexto para la etiqueta `Publicacion fijada`.
- `.collage-card` y `.collage-stage`: contexto para el bloque de imagenes superpuestas.
- `.quote-thread`: contexto para la etiqueta `frase`.
- `.look-media`: contexto para la etiqueta `imagen`.
- `.look-text`: contexto para el numero de cada entrada.

### Absolute

- `.roulette-note`: etiqueta ubicada sobre la franja de cuatro imagenes.
- `.fixed-image span`: etiquetas sobre cada imagen fija.
- `.intro-label`: etiqueta ubicada sobre la publicacion fijada.
- `.vertical-note`: rotulo lateral del collage.
- `.collage-img-one`, `.collage-img-two`, `.collage-img-three`: imagenes superpuestas dentro del collage.
- `.mini-label-one` y `.mini-label-two`: etiquetas pequenas dentro del collage.
- `.quote-thread::after`: etiqueta del cuadro azul de frase.
- `.look-media::before`: etiqueta ubicada sobre cada foto.
- `.look-number`: numero ubicado dentro del cuadro de texto de cada entrada.

## Imagenes

Las imagenes actuales se mantienen en `assets/img/` con la nomenclatura disponible:

- `featured.png`
- `news1.jfif`
- `news2.jfif`
- `news4.jfif`

Como todavia no estan las 8 fotos definitivas, algunas imagenes se reutilizan temporalmente en varias entradas. Cuando se agreguen las fotos finales, se pueden reemplazar manteniendo las mismas rutas usadas en `index.html` o cambiando solo el valor de `src` en cada entrada.

## Como verlo localmente

Opcion simple:

1. Abre la carpeta del proyecto.
2. Abre `index.html` en el navegador.

Opcion con servidor local:

```powershell
python -m http.server
```

Luego abre:

```text
http://localhost:8000
```

## Publicacion en Netlify

El proyecto esta preparado para desplegarse desde GitHub en Netlify.

Configuracion recomendada:

- Repository: repositorio del proyecto
- Branch: `main`
- Base directory: vacio
- Build command: vacio
- Publish directory: `.`

Como es un sitio estatico puro, Netlify solo necesita publicar la raiz del repositorio, donde se encuentra `index.html`.

## Actualizar el sitio

Despues de hacer cambios:

```powershell
git add .
git commit -m "Actualizar foro de moda de Taehyung"
git push
```

Netlify detectara el `push` y publicara automaticamente una nueva version del sitio.
