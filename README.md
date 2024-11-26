Resumen de Teoría sobre Introducción a la Web y Protocolo HTTP


---

Arquitectura Cliente-Servidor

Cliente-Servidor: Arquitectura donde el cliente solicita recursos al servidor, que responde. Permite que varios clientes usen un mismo servidor.

Modelo en 3 capas: Extiende el modelo cliente-servidor para detallar las tecnologías involucradas en cada capa (cliente, servidor, y bases de datos o almacenamiento).


Protocolos Importantes para la Web

HTTP: Protocolo básico de transferencia de hipertexto para cargar páginas web. Es sin estado.

HTTPS: HTTP con seguridad (cifrado TLS o SSL).

Otros Protocolos:

Telnet: Conexión remota de texto, sustituido por SSH (seguro).

SCP: Transferencia de archivos segura, usando SSH.

FTP: Transferencia de archivos no segura. SFTP añade cifrado.



Protocolo HTTP

Funcionamiento: El navegador envía una petición HTTP y el servidor responde con el recurso solicitado.

Sin Estado: No guarda información de sesiones, cada petición es independiente.

Sesiones y Cookies: Son técnicas para que el servidor "recuerde" al cliente usando almacenamiento en cookies.


Ejemplo de Petición y Respuesta HTTP

1. Petición (Request): Incluye un método (ej., GET), ruta, versión del protocolo, y encabezados.


2. Respuesta (Response): Incluye estado (200 OK, 404 Not Found, etc.), encabezados (como Content-Type) y el contenido solicitado.



Características de HTTP

Sencillo y Extensible: Usa texto plano y puede incluir metadatos personalizados.

Ventajas:

Cache: Mejora la velocidad.

Autenticación y Sesiones: Mediante cookies para mantener el estado.

Proxys: Intermediarios que facilitan la conexión entre cliente y servidor.



Métodos HTTP

GET: Solicita datos.

POST: Envía nuevos datos.

PUT: Actualiza datos existentes.

DELETE: Elimina datos.


Ejemplos de Peticiones cURL

1. GET: curl -X GET https://jsonplaceholder.typicode.com/posts/1


2. POST: curl -X POST https://jsonplaceholder.typicode.com/posts -d '{"title": "foo"}'


3. PUT: curl -X PUT https://jsonplaceholder.typicode.com/posts/1 -d '{"title": "updated"}'


4. DELETE: curl -X DELETE https://jsonplaceholder.typicode.com/posts/1



REST (REpresentational State Transfer)

REST: Aprovecha HTTP para desarrollar aplicaciones web usando JSON como formato de datos común.

Operaciones CRUD: Mapear operaciones HTTP a funciones de base de datos (ej., GET para leer, POST para crear).


Cabeceras HTTP

Cabeceras de Petición:

Accept: Formato deseado de respuesta (JSON, XML).

Host: Dominio de la petición.

Content-Type: Formato de los datos enviados.


Cabeceras de Respuesta:

Content-Type: Tipo de datos devueltos.

Cache-Control: Indica el tiempo de cacheo.



Estados HTTP

200-299: Éxito (ej., 200 OK).

400-499: Error del cliente (ej., 404 Not Found).

500-599: Error del servidor.


HTTPS y Seguridad

HTTPS: Añade SSL/TLS a HTTP para la encriptación y autenticación del servidor.

Seguridad: Protege la integridad de los datos y previene ataques como "Man in the Middle".


Herramientas de Depuración

Chrome DevTools: Herramienta para inspeccionar peticiones y respuestas HTTP en el navegador (F12 -> Network).



---

Este resumen cubre los conceptos básicos de HTTP y sus aplicaciones en la web, resaltando protocolos, métodos, encabezados y principios clave de seguridad en HTTPS.
