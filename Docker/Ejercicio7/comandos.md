# Tarea 7

- docker volume create volumen_datos
- docker volume create volumen_web

- docker run -d --name c1 -p 8080:80 -v volumen_web:/var/www/html php:7.4-apache

- docker run -d --name c2 -p 3307:3306 \
    -e MYSQL_ROOT_PASSWORD=admin \
    -v volumen_datos:/var/lib/mysql \
    mariadb

- docker stop c2

- docker rm c2

- docker volume rm volumen_datos

## Imagen
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Docker/Ejercicio7/Tarea7.png?raw=true)