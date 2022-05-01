# media-server
Si no tenemos instalado Docker, preparamos el sistema y lo instalamos.

Actualización del sistema:

        $ apt update
        $ apt upgrade

Instalamos dependencias:

        $ sudo apt install apt-transport-https ca-certificates curl software-properties-common

Instalación de Docker:

        $ cd /

        $ mkdir docker

        $ curl -fsSL https://get.docker.com -o get-docker.sh

        $ sh get-docker.sh

        $ sudo usermod -aG docker $USER

Instalación de Docker Compose:

        $ sudo curl -L "https://github.com/docker/compose/releases/download/v2.4.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    
Confirmamos la versión más reciente disponible en su página de (versiones.)[https://github.com/docker/compose/releases]

Y si tenemos Docker y Docker-compose instalamos, clonamos el repositorio
    
        $ git clone https://github.com/davidpebe78/media-server.git

Cambiamos de directorio:

        $ cd media-server

Edita el archivo .env, con las variables que necesites para el funcionamiento de los contenedores:

        $ nano .env

Y ejecutamos:

        $ docker-compose up -d


