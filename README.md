# OSTicket_APIUsuarios
Servidor Web: Compatible con PHP (Apache/Nginx).
PHP: Versión 7.2 o superior. Verifica con:
bash
Copiar código
php -v
Extensiones PHP:
mysqli
curl
mbstring
xml
json
Base de Datos MySQL: Configura MySQL o MariaDB, crea una base de datos para osTicket.
osTicket: Descarga la última versión desde osTicket.
Configuración de osTicket: Ajusta el archivo config.php con los datos de tu base de datos.
Acceso a Internet: Asegúrate de que tu servidor pueda descargar dependencias.
Instalación 🔧
Archivos a modificar:

Edita upload/api/http.php.
Crea upload/include/api.users.php.
Configura osTicket:

Inicia sesión como agente.
Ve a Admin Panel > Manage > API.
Crea una API key:
Añade la IP de tu aplicación.
Marca las casillas para permitir JSON, XML y EMAIL.
Guarda la API key para usarla en los headers o como parámetro.
Llamadas a la API
Haz un POST a la URL:

JSON: http://tu-dominio/osticket/upload/api/users.json
XML: http://tu-dominio/osticket/upload/api/users.xml
EMAIL: http://tu-dominio/osticket/upload/api/users.email
Ejemplo de datos (JSON):

json
Copiar código
{
  "email": "usuario@ejemplo.com",
  "full_name": "Nombre Usuario",
  "phone": "123456789",
  "timezone": "America/Los_Angeles",
  "password": "contraseña123",
  "confirm_password": "contraseña123"
}
Pruebas
Usa una aplicación como Postman o un entorno de desarrollo configurado para realizar pruebas.
