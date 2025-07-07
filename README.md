# Control de Nodos IoT - Flask + MQTT + MySQL

Este proyecto es una aplicación web desarrollada con Flask para gestionar nodos IoT. Permite a cada usuario registrar sus propios nodos, asignarles un setpoint y enviar comandos como activar un destello. La comunicación con los dispositivos se realiza mediante MQTTs y toda la información se guarda en una base de datos MariaDB/MySQL.

## Funcionalidades

- Registro y login de usuarios
- Alta de nodos asociados a un usuario
- Visualización de los nodos propios
- Envío de comandos (setpoint y destello) a cada nodo vía MQTT
- Soporte para temas claro/oscuro

## Requisitos

- Python 3.11+
- MariaDB/MySQL
- Broker MQTT con soporte para conexión segura (MQTTs)

## Tecnologías utilizadas

- Flask
- Flask-MySQLdb
- Flask-MQTT
- Bootstrap (tema Lux)
- Jinja2

## Configuración

Antes de correr la app, se deben tener configuradas las siguientes variables de entorno:

- MARIADB_USER
- MARIADB_USER_PASS
- MARIADB_DB
- MARIADB_SERVER
- FLASK_SECRET_KEY
- MQTT_BROKER
- MQTT_PORT
- MQTT_USER
- MQTT_PASSWORD


##Observaciones
- Cada nodo se asocia a un usuario al momento de registrarlo
- Los comandos MQTT se publican en los tópicos:
    * sensor_id/setpoint
    * sensor_id/destello


