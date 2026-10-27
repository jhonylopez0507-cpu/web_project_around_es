# Around The U.S.

Proyecto web de TripleTen (Sprint 6) que muestra el perfil de un explorador y una galería de tarjetas con lugares naturales. El proyecto avanza por etapas: primero se organizaron los datos de las tarjetas en un array de JavaScript y después se agregó una ventana emergente para editar el perfil.

## Descripción del proyecto

Around The U.S. es una página responsiva construida con HTML, CSS y JavaScript puro. Presenta el perfil de Jacques Cousteau y una cuadrícula de tarjetas con fotografías de paisajes. El usuario puede abrir una ventana emergente para editar su nombre y su descripción, y los cambios se reflejan al instante en la página.

## ¿Qué encontrarás aquí?

- **Perfil de usuario:** avatar, nombre, descripción y botón de edición.
- **Edición de perfil:** ventana emergente con un formulario precargado con los datos actuales; se abre con el botón de editar y se cierra con la X o al guardar.
- **Galería de tarjetas:** seis lugares con imagen, título, botón de "me gusta" y botón de eliminar.
- **Ventanas emergentes adicionales:** estructura HTML para agregar una nueva tarjeta y para ampliar una imagen (su lógica llegará en las siguientes etapas).
- **Array `initialCards`:** seis objetos con los campos `name` y `link`, con los datos de cada tarjeta.

## Características técnicas

- HTML semántico (`header`, `main`, `section`, `footer`).
- Metodología **BEM** para nombrar clases y organizar los estilos por bloques.
- Estructura de archivos por bloques, con CSS modular dentro de `blocks/` y archivo principal en `pages/`.
- Diseño adaptable a distintos tamaños de pantalla.
- Fuente **Inter** cargada localmente desde `vendor/`.
- JavaScript puro (Vanilla JS), sin librerías ni frameworks.
- Manipulación del DOM con `querySelector`, `classList` y `addEventListener`.
- Formulario controlado con `preventDefault()` para evitar la recarga de la página.
- Nombres de variables y funciones en **camelCase**, con sustantivos descriptivos.

## ¿Cómo se hizo?

- Se partió de la plantilla de TripleTen con el HTML y los estilos de las tarjetas.
- **Etapa 1:** se creó `scripts/index.js`, se declaró el array `initialCards` y se recorrió con `forEach()` para mostrar el nombre de cada tarjeta en la consola.
- **Etapa 2:** se seleccionaron los elementos del perfil y de la ventana emergente `edit-popup`.
- Se programó la apertura del popup agregando la clase `popup_is-opened` y el relleno de los campos con los valores actuales del perfil.
- Se programó el cierre del popup con el botón de la X.
- Se manejó el evento `submit` del formulario para actualizar el nombre y la descripción en la página y cerrar la ventana.
- Se verificó que la consola no registrara errores al abrir la página.

## Estructura del proyecto

```
web_project_around_es/
├── blocks/        # Estilos CSS por bloque (BEM)
├── images/        # Imágenes y recursos gráficos
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
4. Pulsa el botón de editar junto al nombre, modifica los campos y pulsa **Guardar** para ver los cambios en el perfil.

## Tecnologías principales

- HTML5
- CSS3 (metodología BEM)
- JavaScript (Vanilla JS)
- Git y GitHub

## ¿Por qué este proyecto es diferente?

Los datos de las tarjetas viven en un array y no en el HTML, y la edición del perfil usa el DOM de forma directa, sin librerías. Esa base permite que en las siguientes etapas se generen tarjetas dinámicamente, se agreguen nuevas desde un formulario y se amplíen las imágenes, todo con el mismo patrón de ventanas emergentes.

## Autor

Jonathan Lopez
