Introducción a la Web y Protocolo HTTP

Arquitectura Cliente-Servidor

En la arquitectura cliente-servidor, un cliente solicita un servicio a un servidor, que responde a la solicitud. En desarrollo web, los clientes (navegadores) solicitan páginas web a un servidor, y este responde con el contenido solicitado. Esta arquitectura permite que un servidor multitarea atienda a varios clientes simultáneamente.

Protocolos en la Web

HTTP/HTTPS: Protocolo de transferencia de hipertexto. HTTPS es la versión segura usando SSL/TLS.

Telnet/SSH: Protocolos de acceso remoto, SSH reemplaza a Telnet con cifrado.

FTP/SFTP: Protocolos para transferencia de archivos; SFTP asegura la transferencia mediante SSH.


Protocolo HTTP

HTTP es un protocolo sin estado que permite transferir páginas web. Cada solicitud HTTP es independiente, lo que significa que el servidor no mantiene la información de cada cliente a menos que se implementen cookies o sesiones.

Ejemplo de Petición y Respuesta HTTP

Petición HTTP:

GET /index.html HTTP/1.1
Host: www.misitio.com
User-Agent: Mozilla/5.0

Respuesta HTTP:

HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8

<html>...</html>

HTTPS y Seguridad SSL/TLS

SSL/TLS añade una capa de seguridad al protocolo HTTP, creando HTTPS. HTTPS asegura la autenticación y privacidad en la web y evita ataques como "Man in the Middle".

Componentes de la Web

La web es una estructura interconectada de páginas HTML, CSS, imágenes, etc., obtenidas mediante HTTP. Los recursos son servidos por un servidor web, y pueden incluir:

Código de visualización: HTML, CSS, imágenes.

Código en el cliente: JavaScript ejecutado en el navegador.

Código en el servidor: Lógica de la aplicación en el servidor.


Herramientas de Desarrollo en el Navegador

Los navegadores incluyen herramientas de desarrollo, como Chrome DevTools, que permite analizar las peticiones y respuestas HTTP.

Características y Ventajas de HTTP

Simplicidad: Es texto plano, fácil de usar y entender.

Sin estado: Las peticiones son independientes, facilitando la escalabilidad.

Ventajas: Soporte para caché, autenticación, proxys, sesiones y manejo de formatos de contenido.


Formato de una Petición y Respuesta HTTP

Las cabeceras en las peticiones y respuestas HTTP ayudan a gestionar el contenido y la comunicación.

Cabeceras de petición: Accept, Accept-Language, Host, Content-Type.

Cabeceras de respuesta: Content-Type, Content-Language, Content-Length, Cache-Control.


Códigos de Estado HTTP

200-299: Éxito.

300-399: Redirección.

400-499: Error del cliente.

500-599: Error del servidor.


Métodos HTTP

GET: Obtiene datos.

POST: Crea datos.

PUT: Actualiza datos.

DELETE: Elimina datos.


REST y JSON en HTTP

REST (Representational State Transfer) usa las características de HTTP, especialmente en servicios web. En REST, las operaciones CRUD (Create, Read, Update, Delete) se asignan a métodos HTTP (POST, GET, PUT, DELETE) y normalmente usan JSON para la transferencia de datos.

Ejemplos de Comandos curl

1. GET: curl -X GET https://jsonplaceholder.typicode.com/posts/1


2. POST: curl -X POST https://jsonplaceholder.typicode.com/posts -d '{"title": "foo", "body": "bar"}'


3. PUT: curl -X PUT https://jsonplaceholder.typicode.com/posts/1 -d '{"title": "updated title"}'


4. DELETE: curl -X DELETE https://jsonplaceholder.typicode.com/posts/1


5. Autenticación: curl -u usuario:contraseña https://ejemplo.com/protegido


