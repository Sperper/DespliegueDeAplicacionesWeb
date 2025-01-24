# Laboratorio 4 - Daemons and processes

## Actividad 4.1

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_4.1.png?raw=true)

- kworker/0:0-events: Hilo del kernel que se encarga de gestionar tareas diferidas y eventos de hardware. Estos procesos se activan según la carga de trabajo del sistema.
- systemd: El proceso principal de inicialización y gestión del sistema. Es el primero que se ejecuta al iniciar el sistema y se encarga de lanzar y gestionar todos los demás procesos.
- kthreadd: Un proceso del kernel que actúa como hilo padre para todos los demás procesos del kernel, gestionando la creación de otros hilos del sistema.
- rcu_gp: Responsable de la sincronización de la actualización de lectura-copia (RCU), que es un mecanismo para actualizar estructuras de datos en sistemas multiprocesador sin bloqueos.
- rcu_par_gp: Otro proceso relacionado con la sincronización de RCU, dedicado a gestionar el paralelismo en el procesamiento de tareas.
- slub_flushwq: Es un proceso del kernel relacionado con la gestión de la memoria en el sistema, en particular con la liberación de páginas de memoria inactivas.
- netns: Proceso encargado de la administración de los espacios de nombres de red (network namespaces) en el kernel de Linux, permitiendo el aislamiento de recursos de red.
- mm_percpu_wq: Administrador de memoria per-CPU, que asigna y libera memoria para cada CPU del sistema de manera eficiente.
- rcu_tasks_kthre: Parte de la infraestructura de RCU para gestionar tareas relacionadas con la actualización y sincronización de estructuras de datos en el kernel.
- rcu_tasks_rude_kthread: Otro proceso relacionado con la sincronización de tareas RCU, con un enfoque en las tareas que requieren una intervención más directa o agresiva.

## Actividad 4.2

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_4.2.png?raw=true)

## Actividad 4.3

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_4.3.png?raw=true)

## Actividad 4.4

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_4.4.png?raw=true)

![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Imagenes/Ejercicio_4.4_b.png?raw=true)

- SFTP: Es un protocolo seguro para transferir archivos a través de SSH, que cifra tanto los datos como las credenciales, protegiendo la información durante la transferencia.
- SSH: Es un protocolo que permite acceso remoto seguro a servidores cifrando los datos, utilizado para administrar sistemas de manera segura y ejecutar comandos de forma remota.
- Telnet no cifra los datos, lo que permite que credenciales y comandos sean interceptados fácilmente, haciendo su uso inseguro. SSH es la alternativa segura.

## Actividad 4.5

1. How could you combine pidof with kill -HUP in order to restart inetd in one command? Hint: try
using quotation marks (such as: 1,", `).

kill -HUP `pidof inetd`

2. Can you ftp as root? Is it a good idea to be able to ftp as root and why? If so, in what context?
Sí, pero está deshabilitado por seguridad en muchos sistemas.
No, porque FTP transmite datos en texto plano y root tiene acceso total al sistema, lo que supone mucho riesgo.
Solo en entornos muy controlados, pero es mejor usar SFTP con privilegios limitados.
