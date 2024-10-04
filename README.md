# API para Creación de Usuarios en osTicket

Este proyecto implementa una API para la creación de usuarios en osTicket sin la necesidad de confirmación por correo electrónico.

## Pre-requisitos 📋

Asegúrate de contar con los siguientes requisitos antes de comenzar:

- **Servidor Web**: Apache o Nginx compatible con PHP.
- **PHP**: Versión 7.2 o superior. Verifica tu versión ejecutando:
  ```bash
  php -v

## Extensiones de PHP:
mysqli
curl
mbstring
xml
json

Base de Datos MySQL: Configura una instancia de MySQL o MariaDB y crea una base de datos para osTicket.
osTicket: Descarga la última versión desde osTicket y configúralo.
Acceso a Internet: Asegúrate de que el servidor pueda descargar dependencias.
Instalación 🔧
Sigue los pasos para configurar la API de creación de usuarios:

## Modifica los archivos necesarios:

Edita upload/api/http.php.
Crea el archivo upload/include/api.users.php.
Configura la API en osTicket:

Inicia sesión como agente en osTicket.
Ve al panel de administración (Admin Panel).
Navega a Manage > API.
Crea una nueva API Key:
Añade la IP donde está alojada tu aplicación.
Marca las opciones para permitir JSON, XML y EMAIL.
Guarda la API Key, ya que la necesitarás en los headers o como parámetro de la API.
Uso de la API
Realiza un POST a las siguientes URLs según el formato que necesites:

JSON: http://tu-dominio/osticket/upload/api/users.json
XML: http://tu-dominio/osticket/upload/api/users.xml
EMAIL: http://tu-dominio/osticket/upload/api/users.email

## Ejemplo de solicitud JSON:
{
    "email": "lalo@mendez.com",
    "full_name": "Eduardo Mendez",
    "phone": "123456789X686",
    "timezone": "America/Los_Angeles",
    "password": "1234",
    "confirm_password": "1234"
}
