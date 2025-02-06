# Apache HTTP sever and PHP

## Actividad 7.1

**Whilst /etc/httpd/httpd.conf is still open, answer the following questions.**
**1. Lines that start with a # are comments: what are the purpose of these?**

 Su propósito es permitir que los administradores incluyan notas explicativas o desactiven temporalmente ciertas líneas de configuración sin que afecten el funcionamiento del servidor web

**2. Find the default values of ServerName and DocumentRoot and note them down. (Uncomment the line containing ServerName.) What do they do/mean?**

ServerName: Es el nombre del servidor (generalmente un dominio o dirección IP) que el servidor Apache utiliza para identificarse. Si no está configurado explícitamente, Apache podría emitir una advertencia y usar la dirección IP del servidor. En algunos sistemas, el valor predeterminado es localhost.

DocumentRoot: Es el directorio principal donde se almacenan los archivos que Apache sirve a los usuarios. El valor predeterminado suele ser /var/www/html. Esto significa que los archivos en este directorio son los que se mostrarán cuando los usuarios accedan al sitio web.

**3. Uncomment the line Include /etc/httpd/mod_php.conf. What does this do?**

Al descomentar esta línea, se está indicando a Apache que incluya el archivo mod_php.conf en su configuración principal.

## Actividad 7.2

**1. Why do you need to restart httpd if you make changes to the configuration?**

Para que Apache lea y aplique las nuevas configuraciones.

**2. This question is about the command ps aux | grep httpd.**

**a) What does the command ps aux do? What about the command grep httpd? What does “|” mean? Hence, explain what the command ps aux | grep httpd does.**

El comando ps aux es un comando que muestra una lista de todos los procesos que se están ejecutando en el sistema.

El comando grep httpd busca todas las líneas que contiene el texto "httpd".

"|" se utiliza para canalizar la salida de un comando como entrada de otro.

El comando ps aux | grep httpd lista todos los procesos que estan relacionados con el servidor Apache(httpd).

**b) What would you expect to see as the output of the command ps aux | grep httpd if httpd is running? How about if it is not running? Try both cases and note down the results.**

Ver una lista de varias líneas con los procesos asociados con el servidor Apache.

Si no está en ejecución solo mostraría una línea mostrando el propio comando grep httpd, ya que no encontrará ningún proceso relacionado con httpd en la lista de procesos activos.

**3. By executing ps axl | egrep "httpd|PPID" (make sure you copy this command exactly: note the spacing and capitalletters),find the processIDofthe parenthttpdprocess(the PPID).**

Al ejecutar el comando ps axl | egrep "httpd|PPID", estás realizando una búsqueda avanazada para identificar procesos relacionados con httpd mostrando las columnas que incluyen "PPID".

Para encontrar el ID del proceso padre hay que buscar la columna que indica PPID y verás qué el valor corresponde al proceso de Apache (httpd).

## Actividad 7.3

**1. What is special about index.htm and index.htmlfiles?**

Estos archivos suelen ser utilizados como la página predeterminada que se carga cuando un usuario accede a un directorio en un servidor web sin especificar un archivo particular.

**2. Find out the permissions and file and group ownership of index.html.**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_7.3.2.png?raw=true)

**3. Create a new file called test.html with the following source code:**

<html>
<head><title>NSE Apache Lab</title></head>
<body>
<h1>This is the NSE Apache Lab test page</h1>
<p>Under construction!</p>
</body>
</html>

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_7.3.3.png?raw=true)

## Actividad 7.4

**1. Explain the difference between CLI andGUI.**

Mientras que CLI es una interfaz donde los usuarios interactuan con el sistema operativo o aplicaciones escribiendo comandos en una consola o terminal, GUI es una interfaz que utiliza elementos
gráficos como ventanas, botones y menús para permitir la interacción con el sistema o aplicaciones. 

**2. What is special about the IP address 127.0.0.1?**

La dirección IP 127.0.0.1 apunta de vuelta a la misma máquina en la que se está ejecutando.

**3. View the HTML file in lynx by executing.**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_7.4.3.png?raw=true)