Versión en Español
# Instalación de Celery y RabbitMQ

Celery se instala localmente (en el entorno virtual del proyecto):

$(nombre_ambiente): `pip install celery`


El broker de mensajería RabbitMQ se instala globalmente (en el sistema):

$: `sudo apt-get install -y erlang rabbitmq-server`

Verificar que el servicio está corriendo:

Opción 1:

$: `sudo service rabbitmq-server status`

Opción 2:

$: `sudo systemctl status rabbitmq-server` o $: `sudo systemctl status rabbitmq-server.service`
