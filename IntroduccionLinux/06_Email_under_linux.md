## Laboratorio 06: Email under linux 

### Actividad 1
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.1.png?raw=true)

- **Explain what the following command does:**
**echo "Welcome to Network Computer Systems" | mail -s "Hello world" bob@anglia.bryant -c smith@anglia.bryant -b root@anglia.bryant**

El comando envía un correo con el asunto "Hello World" y el cuerpo "Welcome to Network Computer Systems" a la dirección principal bob@anglia.bryant, con copia a smith@anglia.bryant y con copia oculta a root@anglia.

### Actividad 6.2
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.2.png?raw=true)

### Actividad 6.3

#### - Leer mails
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.3_Leer.png?raw=true)

#### - Responder mails
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.3_Leer.png?raw=true)

#### - Enviar mails
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.3_Enviar.png?raw=true)

#### - Eliminar mails
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.3_Eliminar.png?raw=true)

**What is contained in /var/spool/mail/? What are the security implications of this?**
Se almacenan los buzones de correo de los usarios locales de un sistema linux. Cada usuario del sistema tiene un archivo en este directorio que lleva su nombre de usuario.

Las implicaciones son que al no ser que se configuren bien los permisos otros usuarios pueden leer el correo, eliminarlos o usarlos para escalar privilegios.

**From your Windows host machine, telnet to your virtual machine on port 25 (telnet ip_address 25) and send a message to bob@localhost from your_name @localhost by talking to the serve The message body text and subject can be anything you like.**

**Enable POP3. Hint: look in /etc/inetd.conf. Also, you should remember that you need to do something after saving changes to a configuration file to make those changes take effect... (refer to Lab 4 on page 23)**

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_6.3_POP3.png?raw=true)

**What ports are used by SMTP and POP3?**
**STMP**
- Purto 25
- Puerto 465
- Puerto 587

**POP3**
- Puerto 110
- Puerto 995

