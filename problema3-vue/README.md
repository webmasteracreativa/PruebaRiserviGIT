Ejercio 3 - Proyecto Vue

Este proyecto es una prueba de Vue.js que utiliza Vite como herramienta de construcción. El código encapsula un Single File Component (SFC), donde se combinan la plantilla HTML, la lógica en JavaScript y los estilos CSS.

## Requisitos

Antes de ejecutar el proyecto, asegúrate de cumplir con los siguientes requisitos:

Tener Node.js instalado en tu sistema.

Haber instalado Vite y Vue 3.

Instalación y Configuración

## Clonar el Repositorio 

Si el código está en un repositorio, clónalo con:

git clone https://github.com/usuario/proyecto.git

2. Navegar a la Carpeta del Proyecto

cd PruebaRiservi/problema3-vue

3️. Instalar Dependencias

Ejecuta el siguiente comando para instalar las dependencias necesarias:

npm install

4. Iniciar el Servidor de Desarrollo

Ejecuta:

npm run dev

Esto iniciará el servidor y podrás acceder a la aplicación en el navegador en la URL que se muestra en la terminal.


## Lógica en Vue.js

Se genera un listado de divs dentro del contenedor con la clase v-container, basado en un array myArray.

Se inicializa myArray con 5 objetos, cada uno con id, name y roles (array de enteros).

Se muestra la información en el formato:

Nombre: [nombre]
Roles: [roles separados por comas]

Los elementos con índice impar tienen un fondo gris (#e6e6e6).

Los elementos con índice par están ocultos.

Se agrega un botón "Generar" que, al hacer clic, muestra la cantidad total de elementos en la variable output.


## Autor
Este ejercicio fue realizado por Damian Arredondo https://www.linkedin.com/in/jhonatan-damian-4b408917a/
