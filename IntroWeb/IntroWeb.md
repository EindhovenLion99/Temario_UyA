# Introduccion a la Web

# Internet

Internet es un conjunto descentralizado de redes de comunicación interconectadas que funcionan como una red única. La conexión se realiza mediante una familia de protocolos.

* Capa de aplicación: HTTP, FTP, SMTP, Telnet, SSH, VoIP, IPTV...
* Capa de transporte: TCP
* Capa de Internet: IP.
* Capa de red

# IP. DNS

* Dirección IP: El protocolo IP requiere la identificación de los elementos que están conectados por la misma mediante una etiqueta numérica separado por 4 partes.
* * IPV4 utiliza 32 bits
* * IPV6 utiliza 128 bits.

* DNS: Sistema de nomenclatura estándar que asigna un nombre lógico al número IP
```
193.145.118.38 --- www.ull.es
``` 
# Worl Wide Web

* World Wide Web (WWW) constituye un sistema de distribución de información enlazada por hipertextos o hipermedios a través de internet.
* URL: Secuencia de caracteres definida de acuerdo a un estándar que constituye un identificador único para cada recurso en la web.

```
esquema://máquina/directorio/archivo
```
*********************************************
```
http://193.145.118.38   ->  http://www.ull.es
```

# Esquema Cliente - Servidor Web

* El servidor recibe la petición por el puerto solicitado, envía al cliente la respuesta.
```
http://host[:puerto][path][?consulta]
```
* El cliente recibe la respuesta, el navegador la muestra.

# Peticion HTTP

* El cliente HTTP inicia una conexión TCP al servidor HTTP por el puerto 80.

* * El servidor HTTP, que se encuentra escuchando en el puerto 80, acepta la conexión, notificándoselo al cliente

* El cliente HTTP manda un mensaje de petición GET a la página index.html dentro de la conexión TCP abierta

* * El servidor HTTP recibe el mensaje de petición, crea un mensaje de respuesta incluyendo el texto HTML de la página solicitada
* * El servidor HTTP cierra la conexión TCPs

* El cliente recibe el mensaje, y presenta la página web. Analizando el documento, encuentra 2 referencias a otros documentos.
* Se repiten los pasos anteriores para cada referencia encontrada.
*****************************************************************************
* Una transacción HTTP está formada por un encabezado seguido, opcionalmente, por una línea en blanco y algún dato.
*****************************************************************************
* GET Petición de recurso
* POST Petición de recurso pasando parámetros. Se usa:
* * ? -> para separar la url de los parámetros
* * nombre del parámetro = valor + para los espacios en blanco
* Otros tipos de petición son: HEAD, PUT, DELETE, TRACE, OPTIONS, CONNECT

*****************************************************************************

*Ejemplo de Peticion*
```
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: nombre-cliente
[Línea en blanco]
```

*Respuesta*
* Respuesta: Similar a la petición. Se especifica:
* Protocolo, código de retorno, información, fecha, servidor, ...
* Código de retorno:
* * 1xx: Petición recibida
* * 2xx: Correcta
* * 3xx: Redireccionado
* * 4xx: Error de cliente
* * 5xx: Error de servidor.

| 1xx: Mensaje Informativo                                                                                  | 4xx: Error del Cliente      400 Bad Request      401 Unauthorized      402 Forbidden      404 Not Found                           |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 2xx: Éxito      200 OK      201 Created      202 Accepted      204 No Content                             | 5xx: Error del Servidor      500 Internal ServerError      501 Not Implemented      502 Bad Gateaway      504 Service Unavailable |
| 3xx: Redireccion      300 Multiple Choice      301 Moved Permanently      302 Found      304 Not Modified |                                                                                                                                   |

*Respuesta*

```
HTTP/1.1 200 OK
Date: Fri, 31 Dec 2003 23:59:59 GMT
Content-Type: text/html
Content-Length: 1221
``` 
```
<html>
<body>
<h1>Página principal de tu Host</h1>
Contenido...
</body>
</html>
```

# Cookies.

* HTTP es un protocolo sin estado.
* Las cookies las utiliza el servidor en el sistema cliente para guardar información relativa al estado.
* Son ficheros de texto que almacena el navegador en memoria o en el disco duro a petición del servidor con información de la petición.