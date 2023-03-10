## picobrowser

## Descripción
Este sitio web solo puede ser renderizado por **picobrowser**, ¡ve y atrapa la bandera! ([enlace](https://jupiter.challenges.picoctf.org/problem/50522/)) o https://jupiter.challenges.picoctf.org/problem/50522/

## Pistas
* No necesita descargar un nuevo navegador web.

## Solución
*- Forma 1:*
1. Inspeccionar la página. 
2. Analizar cómo se envía el header en "Red".
3. Dar clic en "Flag".
4. Identificar la petición que pide la bandera y dar clic.
5. Identificar el valor de User-Agent dentro del apartado de "Headers".
6. Modificar el User-Agent por: *picobrowser* y enviar la solicitud.
7.  Seleccionar la petición creada y ver la respuesta con la bandera correspondiente: **picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}**

*- Forma 2:*
``` bash
vikyga-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/50522/flag -H "User-Agent:picobrowser" | grep pico
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}</code></p>
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}**

## Notas adicionales
* *User-Agent:* es una cadena característica que le permite a los servidores y servicios de red identificar la aplicación, sistema operativo, compañía, y/o la versión del user agent que hace la petición.

## Referencias
* [User-Agent](https://developer.mozilla.org/es/docs/Web/HTTP/Headers/User-Agent)

Fecha: 09/03/2023.