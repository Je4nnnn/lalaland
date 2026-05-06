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
      |- featured.png
      |- news1.png
      |- news2.png
      |- news3.png
      |- news4.png
      |- news5.png
      |- news6.png
      |- news7.png
      |- news8.png
      |- C1.png
      |- C2.png
      |- C3.png
      |- C4.png
      |- C5.png
      `- C6.png
```

## Contenido del sitio

La pagina presenta:

- Un encabezado con el tema del foro y el titulo principal.
- Una franja superior con 4 imagenes fijas, reemplazando la idea inicial de una ruleta.
- Un bloque `Sobre el articulo` que introduce el tema con tono de foro.
- Un bloque visual tipo collage con imagenes superpuestas y tarjetas de conversacion.
- Una frase destacada en un cuadro azul para separar la introduccion de las entradas principales.
- Ocho entradas principales, cada una con foto, fuente pequena bajo la imagen y descripcion en un cuadro lateral.
- Enlaces finales con usuarios de redes: `@thv`, `@bts.bighitofficial`, `@BTS_twt`, `@BTS`, `@voguemagazine` y `@bighit_music`.
- Informacion sobre 8 momentos de moda de Taehyung en 2025: alta costura, craftcore, nostalgia vintage, cuero, tejido arquitectonico, lujo discreto y estilo retro.

## Tecnologias usadas

- HTML5 semantico.
- CSS3 organizado con variables.
- Diseno responsive con `grid`, elementos `inline-block` y media queries.
- Imagenes locales en `assets/img/`.
- Posicionamiento CSS `relative` y `absolute`.
- Uso de etiquetas `div`, `p`, `h1`, `h2`, `header`, `main`, `section`, `article`, `aside` y `footer`.
- Tipografia configurada con Futura para textos y TT Chocolates para titulos secundarios, con fuentes de respaldo por si el navegador no las tiene instaladas.

## Uso de posicionamiento CSS

El proyecto usa `position: relative` para crear contextos de posicionamiento y `position: absolute` para ubicar elementos dentro de esos contextos, tal como se pidio para la evaluacion.

### Relative

- `.forum-header`: bloque principal del titulo del foro.
- `.top-thread`: contexto para la etiqueta del artista.
- `.fixed-image`: contexto para las etiquetas de cada imagen superior.
- `.thread-intro`: contexto para la etiqueta `Sobre el articulo`.
- `.collage-card` y `.collage-stage`: contexto para el bloque de imagenes superpuestas.
- `.quote-thread`: contexto para la etiqueta `frase`.
- `.look-media`: contexto para la etiqueta `BTS`.
- `.look-text`: contexto para el numero de cada entrada.

### Absolute

- `.roulette-note`: etiqueta con el nombre del artista ubicada sobre la franja de cuatro imagenes.
- `.fixed-image span`: etiquetas sobre cada imagen fija.
- `.intro-label`: etiqueta ubicada sobre el bloque `Sobre el articulo`.
- `.vertical-note`: rotulo lateral del collage con el nombre del artista.
- `.collage-img-one`, `.collage-img-two`, `.collage-img-three`: imagenes superpuestas dentro del collage.
- `.mini-label-one` y `.mini-label-two`: etiquetas pequenas dentro del collage.
- `.quote-thread::after`: etiqueta del cuadro azul de frase.
- `.look-media::before`: etiqueta `BTS` ubicada sobre cada foto.
- `.look-number`: numero ubicado dentro del cuadro de texto de cada entrada.

## Imagenes

Las imagenes actuales se mantienen en `assets/img/` con la nomenclatura disponible:

- `featured.png`
- `news1.png`
- `news2.png`
- `news3.png`
- `news4.png`
- `news5.png`
- `news6.png`
- `news7.png`
- `news8.png`
- `C1.png` a `C6.png` para el collage superior

Cada entrada usa su imagen correspondiente: `news1.png` para el primer look, `news2.png` para el segundo y asi sucesivamente hasta `news8.png`.

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
