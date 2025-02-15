# Ejercio 2 - Consulta MySQL para Listar Ciudades y Países

Este ejercicio consiste en escribir una única sentencia MySQL que liste todas las ciudades y sus respectivos países, ordenadas de manera ascendente por país y luego por ciudad. Además, se aplicará un LIMIT 1 para devolver solo el primer resultado de la consulta.

## Requisitos

Para ejecutar correctamente esta consulta, se necesitan las siguientes condiciones:

Dos tablas en la base de datos:

ciudades con las columnas: id, id_pais, nombre.

paises con las columnas: id, nombre.

Los valores en id_pais de ciudades deben coincidir con id en paises para que la relación funcione correctamente.

## Instalación y Ejecución

### Ubicación del Proyecto
Este ejercicio esta en la carpeta PruebaRiservi/problema2/problema2.xlsx

### Arrancar el Servidor
1. Descargar e instalar el siguiente servidor local MAMP en la siguiente URL: https://www.mamp.info/en/mac/
2. Una vez descargado e instalado inicia los servidores de Apache y MySql.
3. Verifica que el servidor este corriendo en el navegador con la siguiente url http://localhost:8888/

### Acceder al Ejercicio en el Navegador
1. Abrir navegador
2. Ingresa la siguiente URL: http://localhost:8888/phpMyAdmin5/index.php

### Ejecución

1. Crea una base de datos con el nombre que desees.
2. Crea 1 tabla ciudades y la llenas con la informacion del excel, y creas otra tabla con el nombre paises y la llenas con la informacion de paises que hay en el excel.
3. En el sql ejecuta el siguiente query para listar los resultados esperados sin limit 1: 
SELECT ciudades.nombre AS Ciudad, 
paises.nombre AS Pais
FROM ciudades
LEFT JOIN paises ON ciudades.id_pais = paises.id
ORDER BY Pais ASC, Ciudad ASC;

o ejecuar esta consultar para resultados con limit 1: 
"SELECT ciudades.nombre AS Ciudad, 
paises.nombre AS Pais
FROM ciudades
LEFT JOIN paises ON ciudades.id_pais = paises.id
ORDER BY Pais ASC, Ciudad ASC LIMIT 1;"

## Autor
Este ejercicio fue realizado por Damian Arredondo https://www.linkedin.com/in/jhonatan-damian-4b408917a/