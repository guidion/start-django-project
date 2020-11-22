Versión en Español
# Configuración del servidor Ubuntu 18.04 LTS

## 1. CAMBIAR ZONA HORARIA DEL SERVIDOR

Puedes cambiar la zona horaria del servidor de esta manera:

$: `sudo timedatectl set-timezone America/Bogota`

Si tu zona horaria es diferente puedes buscarla con este comando:

$: `timedatectl list-timezones`

## 2. INSTALACIÓN DE PAQUETES PRINCIPALES

Actualizamos información de repositorios:

$: `sudo apt-get update`

Instalamos paquetes necesarios para el desarrollo con Python:

$: `sudo apt-get install -y build-essential python3-pip python3-dev python3-virtualenv virtualenvwrapper`

Instalamos Git (Gestor de Versiones):

$: `sudo apt-get install -y git`

Instalamos Servidor Web Nginx (Engine X, se pronuncia *enyáinex*):

$: `sudo apt-get install -y nginx`

Ahora se deben actualizar las fuentes desde las que se leen los paquetes, aplicaciones y comandos de la terminal. Si no actualizas las fuentes no podrás ejecutar algunas cosas que acabas de instalar. La ruta al directorio del usuario actual se puede representar por *~/*. Ejecuta este comando:

$: `source ~/.bashrc`

## 3. CREACIÓN DE UN AMBIENTE VIRTUAL

Para la versión Python 3 de tu sistema (usualmente es Python 3.6.9):

$: `mkvirtualenv nombre_ambiente --python=$(which python3)`

Para Python 3.8:

$: `mkvirtualenv nombre_ambiente --python=$(which python3.8)`

Para acceder al ambiente virtual creado:

$: `cdvirtualenv`

El resultado será:

$: `~\.virtualenvs\nombre_ambiente\`

Dentro de este ambiente deberás instalar los paquetes del proyecto que vas a trabajar. Se trata de una instalación local dentro del ambiente virtual.

## 4. INSTALACIÓN DE DJANGO

Comienza por instalar una versión LTS de Django. Para este caso usaré Django 2.2.17. Si quieres saber cuál es la versión actual LTS visita su página de descargas [https://www.djangoproject.com/download/] y consulta en la sección Supported Versions.

$: `pip install django==2.2.17`

### 4.1. CREACIÓN DE UN PROYECTO

$: `django-admin startproject nombre_proyecto`




