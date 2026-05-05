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
- Un bloque central con collage de imagenes y textos tipo publicacion/respuesta.
- Una frase destacada y una seccion inferior con tres columnas.
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
- `.collage-panel` y `.collage-stage`: contexto para el collage central.
- `.quote-thread`: contexto para la etiqueta `frase`.
- `.feature-photo`: contexto para la etiqueta sobre la imagen inferior.

### Absolute

- `.roulette-note`: etiqueta ubicada sobre la franja de cuatro imagenes.
- `.fixed-image span`: etiquetas sobre cada imagen fija.
- `.side-label`: rotulo lateral del bloque de collage.
- `.collage-img-one`, `.collage-img-two`, `.collage-img-three`: imagenes superpuestas del collage.
- `.mini-card-one` y `.mini-card-two`: etiquetas pequenas dentro del collage.
- `.quote-thread::after`: etiqueta de frase destacada.
- `.photo-pin`: etiqueta ubicada sobre la imagen inferior.

## Imagenes

Las imagenes actuales se mantienen en `assets/img/` con la misma nomenclatura:

- `featured.jpg`
- `news1.jpg`
- `news2.jpg`
- `news3.jpg`
- `news4.jpg`

Cuando se reemplacen las imagenes definitivas, conviene conservar los mismos nombres para que el HTML no necesite cambios.

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
