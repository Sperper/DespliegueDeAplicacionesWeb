# Comandos

## Actualizar los repositorios
sudo apt update

## Instalar los paquetes necesarios
sudo apt install ca-certificates curl gnupg lsb-release

## Agregar la clave GPG de Docker
sudo curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

## Agregar el repositorio de Docker
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

## Actualizar los repositorios nuevamente
sudo apt update

## Instalar Docker Engine
sudo apt install docker-ce docker-ce-cli containerd.io

## Verificar la instalacion
docker version

## Foto de Hello World con docker
![](https://github.com/Sperper/DespliegueDeAplicacionesWeb/blob/master/Docker/InstalacionDocker/Hola-Mundo.png?raw=true)