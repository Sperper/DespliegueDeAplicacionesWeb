# Tarea 4

## Comandos usados
- docker run -d --name web -p 8181:80 php:7.3-apache

- <h1>HOLA SOY [Tu Nombre y Apellidos]</h1>

- <?php phpinfo(); ?>

- docker cp index.html web:/var/www/html/
- docker cp index.php web:/var/www/html/

- docker run -d --name bbdd -p 3336:3306 \
    -e MYSQL_ROOT_PASSWORD=root \
    -e MYSQL_DATABASE=prueba \
    -e MYSQL_USER=invitado \
    -e MYSQL_PASSWORD=invitado \
    mariadb

## Foto
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Docker/Ejercicio4/BaseDeDatos.png?raw=true)