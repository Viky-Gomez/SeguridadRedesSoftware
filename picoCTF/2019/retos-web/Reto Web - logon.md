## logon

## Descripción
La fábrica está ocultando cosas a todos sus usuarios. ¿Puedes iniciar sesión como Joe y encontrar lo que han estado viendo? ([enlace](https://jupiter.challenges.picoctf.org/problem/15796/)) o https://jupiter.challenges.picoctf.org/problem/15796/

## Pistas
* Hmm, no parece verificar la contraseña de nadie, excepto la de Joe?

## Solución
*- Forma 1:*
1. Abrir el inspector de la página.
2. Ir al apartado de "Red".
3. Ingresar con cualquier nombre y contraseña.
4. Observar las peticiones que se realizaron al ingresar los datos solicitados. 
5. Añadir una nueva extensión al navegador: Cookie Editor y examinar las cookies de la página.
6. Modificar la cookie "Admin" con un valor "True".
7. Guardar y refrescar la página.
8. Obtener la bandera: **picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}**

*- Forma 2:*
``` bash 
vikyga-picoctf@webshell:~$ curl -s  https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: admin=True" | grep pico 
            <p style=text-align:center; font-size:30px;><b>Flag</b>: <code>'picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}'</code></p>
vikyga-picoctf@webshell:~$ 
```

## Bandera
**picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}**

## Notas adicionales
* *Comunicación HTTP:* protocolo sin estado de la capa de aplicación que articula los intercambios de información entre los clientes Web y los servidores HTTP.
* *HTTP headers:* permiten al cliente y al servidor pasar información adicional con una solicitud o respuesta HTTP.
* *HTTP cookies:* es una pequeña pieza de datos que un servidor envía a el navegador web del usuario, el navegador los guarda y los envía de regreso junto con la nueva petición al mismo servidor.

|Comando | Descripcion |
|-----|-------|
| curl | Transfiere datos hacia o desde un servidor, utilizando cualquiera de los protocolos compatibles (HTTP, FTP, IMAP, POP3, FILE, etc).|


## Referencias
* [HTTP](https://neo.lcc.uma.es/evirtual/cdd/tutorial/aplicacion/http.html)
* [HTTP headers](https://developer.mozilla.org/en-US/docs/web/http/headers)
* [HTTP cookies](https://developer.mozilla.org/es/docs/Web/HTTP/Cookies)
* [curl](https://www.geeksforgeeks.org/curl-command-in-linux-with-examples/)

Fecha: 09/03/2023.