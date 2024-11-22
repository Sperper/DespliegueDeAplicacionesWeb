# Ejercicio 8

- mkdir saludo

- echo "<h1>HOLA SOY [Tu Nombre]</h1>" > saludo/index.html

- docker run -d --name c1 -p 8181:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache

- docker run -d --name c2 -p 8282:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache

## Imagen

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Docker/Ejercicio8/Ejercicio%208.png?raw=true)