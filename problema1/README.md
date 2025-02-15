# Ejercio 1 PHP - FOOBAR

Este ejercicio implementa la función examen() en PHP, que valida los parámetros ingresados y genera un array basado en las siguientes reglas:

Si un número es múltiplo de 3, se asigna "FOO".

Si un número es múltiplo de 5, se asigna "BAR".

Si un número es múltiplo de ambos (3 y 5), se asigna "FOOBAR".

En caso contrario, se asigna una cadena vacía ("").

## Requisitos

Para que la función se ejecute correctamente, se deben cumplir las siguientes condiciones:

iMin e iMax deben ser enteros de 1 a 3 dígitos.

iMax debe ser mayor que iMin.

aDatos debe ser un array vacío cuando se pasa como argumento.

La función devuelve TRUE si los parámetros son válidos y el array se genera correctamente; en caso contrario, devuelve FALSE.

## Estructura del Código

El código consta de lo siguiente:

Definición de la función examen() con validaciones y generación de datos.

Casos de prueba para verificar su correcto funcionamiento.

Salida de datos esperada para cada caso de prueba.

## Instalación y Ejecución

### Ubicación del Proyecto
Este ejercicio esta en la carpeta PruebaRiservi/problema1/problema1.php

### Arrancar el Servidor
1. Descargar e instalar el siguiente servidor local MAMP en la siguiente URL: https://www.mamp.info/en/mac/
2. Una vez descargado e instalado inicia los servidores de Apache y MySql.
3. Verifica que el servidor este corriendo en el navegador con la siguiente url http://localhost:8888/

### Acceder al Ejercicio en el Navegador
1. Abrir navegador
2. Ingresa la siguiente URL: http://localhost:8888/PruebaRiservi/problema1/ejercicio1.php
3. Presiona Enter y revisa la salida.

### Ejecución desde la Terminal

También puedes ejecutar el script desde la terminal si tienes PHP instalado en tu sistema:
- Ejemplo: cd /Applications/MAMP/htdocs/PruebaRiservi/problema1/php ejercicio1.php

## Casos de prueba
El script incluye seis casos de prueba y cada uno tiene una combinacion diferente de valores

### Caso 1
Valores validos (iMin = 1, iMax = 30)

### Caso 2
aDatos es NULL

### Caso 3
iMin e iMax como strings

### Caso 4
iMin e iMax como floats

### Caso 5
iMax fuera del rango permitido

### Caso 6
Valores válidos

### El resultado final debe mostrar el caso 1 y el caso 6 para que de como resultado correcto.


## Autor
Este ejercicio fue realizado por Damian Arredondo https://www.linkedin.com/in/jhonatan-damian-4b408917a/