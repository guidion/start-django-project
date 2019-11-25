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

Instalamos Git (Gestor de Versiones) y Servidor Web Nginx (Engine X, se pronuncia *enyáinex*):

$: `sudo apt-get install -y git nginx`

Ahora se deben actualizar las fuentes desde las que se leen los paquetes, aplicaciones y comandos de la terminal. Si no actualizas las fuentes no podrás ejecutar algunas cosas que acabas de instalar. La ruta al directorio del usuario actual se puede representar por *~/*. Ejecuta este comando:

$: `source ~/.bashrc`
