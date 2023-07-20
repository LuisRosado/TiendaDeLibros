# TiendaDeLibros
Un Arquetipo de sitio para una tienda de libros en linea

![image](https://github.com/LuisRosado/TiendaDeLibros/assets/140114139/5fad46ee-db30-4cfc-841f-56b6e1153bbe)

Explicare lo mejor posible cada parte de el proyecto.

-----> CSS <-----

Los códigos que proporcionaste son una hoja de estilos CSS que controla el aspecto y la presentación visual de una página web. A continuación, te explico algunas partes clave de este código:

1. **Fuentes de Google Fonts**:
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;400;500;600&display=swap');
```
Esta línea importa la fuente "Poppins" desde Google Fonts y la hace disponible para su uso en la página web.

2. **Variables CSS (var(--nombre-variable))**:
```css
:root {
  --green: #232f3e;
  --dark-color: #111111;
  --black: #444;
  --light-color: #666;
  --yellow: #e47911;
  --border: .1rem solid rgba(0, 0, 0, .1);
  --border-hover: .1rem solid var(--black);
  --box-shadow: 0 .5rem 1rem rgba(0, 0, 0, .1);
}
```
Aquí se definen variables CSS globales que contienen valores que se reutilizarán en diferentes partes de la hoja de estilos para mantener la coherencia y facilitar el ajuste del diseño.

3. **Estilos generales**:
```css
* {
  /* ... */
  box-sizing: border-box;
  outline: none;
  border: none;
  text-decoration: none;
  text-transform: capitalize;
  transition: all .2s linear;
  /* ... */
}
```
Estos estilos se aplican a todos los elementos en la página web y proporcionan ajustes generales como eliminar el borde y el resaltado de enfoque, eliminar el subrayado de enlaces y aplicar una transición suave a todos los cambios.

4. **Media Queries**:
```css
@media (max-width: 991px) {
  /* Estilos para pantallas más pequeñas que 992px de ancho */
  /* ... */
}

@media (max-width: 768px) {
  /* Estilos para pantallas más pequeñas que 769px de ancho */
  /* ... */
}

@media (max-width: 450px) {
  /* Estilos para pantallas más pequeñas que 451px de ancho */
  /* ... */
}
```
Estos bloques de código contienen estilos específicos para diferentes tamaños de pantalla. Se utilizan para asegurar que el diseño sea responsive y se adapte adecuadamente a dispositivos móviles y tabletas.

-----> JS <-----

El código que proporcionaste es código JavaScript que controla la funcionalidad y la interacción del sitio web. A continuación, te explico lo que hace cada parte del código:

1. **Mostrar/ocultar el formulario de búsqueda**:
```javascript
searchForm = document.querySelector('.search-form');

document.querySelector('#search-btn').onclick = () => {
  searchForm.classList.toggle('active');
}
```
Este código selecciona el elemento con la clase "search-form" y el botón con el id "search-btn". Cuando se hace clic en el botón, se añade o se quita la clase "active" al elemento con la clase "search-form", lo que muestra u oculta el formulario de búsqueda en función de si la clase "active" está presente o no.

2. **Mostrar/ocultar el formulario de inicio de sesión**:
```javascript
let loginForm = document.querySelector('.login-form-container');

document.querySelector('#login-btn').onclick = () => {
  loginForm.classList.toggle('active');
}

document.querySelector('#close-login-btn').onclick = () => {
  loginForm.classList.remove('active');
}
```
En este bloque de código, se selecciona el elemento con la clase "login-form-container" y los elementos con los id "login-btn" y "close-login-btn". Cuando se hace clic en el botón con el id "login-btn", se añade o se quita la clase "active" al elemento con la clase "login-form-container", lo que muestra u oculta el formulario de inicio de sesión. Cuando se hace clic en el botón con el id "close-login-btn", se quita la clase "active" al elemento con la clase "login-form-container", ocultando el formulario de inicio de sesión.

3. **Cambiar el aspecto de la barra de navegación al hacer scroll**:
```javascript
window.onscroll = () => {
  searchForm.classList.remove('active');

  if (window.scrollY > 80) {
    document.querySelector('.header .header-2').classList.add('active');
  } else {
    document.querySelector('.header .header-2').classList.remove('active');
  }
}
```
Este bloque de código se encarga de cambiar el aspecto de la barra de navegación al hacer scroll en la página. Cuando el usuario hace scroll hacia abajo, se quita la clase "active" del elemento con la clase "search-form" para ocultar el formulario de búsqueda si está abierto. Además, si el valor de desplazamiento vertical es mayor que 80, se agrega la clase "active" al elemento con la clase "header-2" en la sección con la clase "header", lo que modifica el aspecto de la barra de navegación. Si el valor de desplazamiento es menor o igual a 80, se quita la clase "active" para restaurar el aspecto original de la barra de navegación.

4. **Funciones para el cargador y la animación de carga**:
```javascript
window.onload = () => {
  if (window.scrollY > 80) {
    document.querySelector('.header .header-2').classList.add('active');
  } else {
    document.querySelector('.header .header-2').classList.remove('active');
  }

  fadeOut();
}

function loader() {
  document.querySelector('.loader-container').classList.add('active');
}

function fadeOut() {
  setTimeout(loader, 4000);
}
```
Cuando la página se ha cargado completamente (evento "onload"), se verifica si el valor de desplazamiento vertical es mayor que 80, y en función de esto, se agrega o se quita la clase "active" del elemento con la clase "header-2" en la sección con la clase "header" para cambiar el aspecto de la barra de navegación. La función "fadeOut()" se utiliza para mostrar un cargador durante un período de tiempo específico (en este caso, 4 segundos) antes de quitarlo y mostrar el contenido de la página.

5. **Configuración de los Swipers (deslizadores) para diferentes secciones**:
En este fragmento, se configuran varios deslizadores utilizando la librería Swiper para crear carousels interactivos para diferentes secciones (como libros, destacados, nuevos productos, reseñas y blogs).

Es importante tener en cuenta que para que estos códigos funcionen correctamente, la página debe incluir la librería Swiper y los elementos HTML asociados con las clases y los ids mencionados en el código. Además, es posible que haya más código JavaScript en el sitio web para proporcionar funcionalidades adicionales.
