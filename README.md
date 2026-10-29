# Around The U.S.

Proyecto web de TripleTen (Sprint 6) con un perfil de usuario y una galería de tarjetas totalmente interactiva: se pueden crear, dar "me gusta", eliminar y ampliar. Es la parte front-end de una aplicación web.

**Demo en GitHub Pages:** https://jhonylopez0507-cpu.github.io/web_project_around_es/

## Descripción del proyecto

Around The U.S. es una página responsiva construida con HTML, CSS y JavaScript puro. Presenta el perfil de Jacques Cousteau y una cuadrícula de tarjetas con fotografías de paisajes. Las tarjetas se generan con JavaScript a partir de un array de datos y una plantilla HTML, y el usuario puede editar su perfil y administrar las tarjetas desde ventanas emergentes.

## ¿Qué encontrarás aquí?

- **Perfil de usuario:** avatar, nombre, descripción y botón de edición.
- **Edición de perfil:** ventana emergente con un formulario precargado con los datos actuales; los cambios se reflejan al guardar.
- **Galería de tarjetas:** seis tarjetas iniciales generadas desde el array `initialCards`.
- **Agregar tarjetas:** ventana emergente con título y enlace de imagen; la nueva tarjeta aparece como la primera de la galería.
- **Botón "Me gusta":** el corazón cambia de color al pulsarlo.
- **Eliminar tarjetas:** el botón de papelera quita la tarjeta del DOM.
- **Imagen ampliada:** al hacer clic en una imagen se abre una ventana emergente con la foto grande y su título.

## Características técnicas

- HTML semántico (`header`, `main`, `section`, `footer`) y un elemento `<template>` para las tarjetas.
- Metodología **BEM** para nombrar clases y organizar los estilos por bloques.
- Diseño adaptable a distintos tamaños de pantalla y fuente **Inter** cargada localmente.
- JavaScript puro (Vanilla JS), sin librerías ni frameworks.
- Funciones reutilizables `openModal()` y `closeModal()` para todas las ventanas emergentes.
- Función `getCardElement()` con **parámetros predeterminados**: si falta el nombre se muestra "Sin título" y si falta el enlace se usa `placeholder.jpg`.
- Función `renderCard()` que antepone cada tarjeta al contenedor.
- Manejo de eventos con `addEventListener()` y `preventDefault()` en los formularios.
- Nombres de variables y funciones en **camelCase**; las funciones empiezan con un verbo.
- Los datos del usuario nunca se insertan con `innerHTML`.

## ¿Cómo se hizo?

- **Etapa 1:** se creó `scripts/index.js` con el array `initialCards`.
- **Etapa 2:** se programó la ventana "Editar perfil" con `openModal()`, `closeModal()` y el manejo del envío del formulario.
- **Etapa final:**
  - Se reemplazaron las tarjetas escritas a mano por un `<template>` y se clonan con `getCardElement()`.
  - Se agregó la ventana "Agregar una tarjeta" con su controlador `handleCardFormSubmit()`.
  - Se configuraron los detectores de eventos dentro de `getCardElement()` para "me gusta", eliminar y ampliar la imagen.
  - Se reutilizaron las mismas funciones del modal para la ventana de imagen.

## Estructura del proyecto

```
web_project_around_es/
├── blocks/        # Estilos CSS por bloque (BEM)
├── images/        # Imágenes y recursos gráficos (incluye placeholder.jpg)
├── pages/         # Archivo principal de estilos (index.css)
├── scripts/       # Lógica en JavaScript (index.js)
├── vendor/        # Fuentes y estilos normalizados
├── index.html
└── README.md
```

## Instalación y uso

1. Clona este repositorio:
   ```
   git clone https://github.com/jhonylopez0507-cpu/web_project_around_es.git
   ```
2. Abre la carpeta del proyecto en tu editor de código.
3. Abre `index.html` en el navegador (o usa la extensión **Live Server**).
4. Prueba la galería: pulsa **+** para crear una tarjeta, el corazón para dar "me gusta", la papelera para eliminarla o la imagen para verla ampliada.

Los cambios no se guardan al recargar la página: eso requerirá un back-end, que es la siguiente parte de la aplicación.

## Tecnologías principales

- HTML5
- CSS3 (metodología BEM)
- JavaScript (Vanilla JS)
- Git y GitHub Pages

## ¿Por qué este proyecto es diferente?

Las tarjetas ya no dependen del HTML: se generan desde datos con una plantilla y una sola función que las construye y les conecta sus eventos. Un mismo par de funciones (`openModal()` y `closeModal()`) controla las tres ventanas emergentes, y los parámetros predeterminados evitan que una tarjeta con datos incompletos rompa la página.

## Autor

Jonathan Lopez
