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

Este es solo un resumen de algunos de los estilos y conceptos presentes en el código CSS. Cabe mencionar que para comprender completamente el funcionamiento de una página web, también se necesitaría revisar el código HTML y cualquier JavaScript que esté presente en el sitio. Si necesitas ayuda con alguna parte específica o tienes alguna pregunta en particular, no dudes en preguntar.
