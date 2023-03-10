## dont-use-client-side

## Descripción
¿Puedes entrar en este portal súper seguro? ([enlace](https://jupiter.challenges.picoctf.org/problem/29835/)) o https://jupiter.challenges.picoctf.org/problem/29835/

## Pistas
* Nunca confíes en el cliente.

## Solución
1. Ver el código fuente de la página.
2. Cifrar la forma de la llave del reto en base al código que viene dentro de la sección "script": 
``` bash 
<script type="text/javascript">
	function verify() {
		checkpass = document.getElementById("pass").value;
		split = 4;
		if (checkpass.substring(0, split) == 'pico') {
			if (checkpass.substring(split*6, split*7) == '723c') {
				if (checkpass.substring(split, split*2) == 'CTF{') {
					if (checkpass.substring(split*4, split*5) == 'ts_p') {
						if (checkpass.substring(split*3, split*4) == 'lien') {
							if (checkpass.substring(split*5, split*6) == 'lz_7') {
								if (checkpass.substring(split*2, split*3) == 'no_c') {
									if (checkpass.substring(split*7, split*8) == 'e}') {
										alert("Password Verified")
										}
									}
								}
							}
						}
					}
				}
			}
		else {
			alert("Incorrect password");
		}
	}
</script> 'picoCTF{no_clients_plz_7723ce}'
```

## Bandera
**picoCTF{no_clients_plz_7723ce}**

## Notas adicionales
*- Client-side:* se refiere a todo en una aplicación web que se muestra o tiene lugar en el dispositivo del usuario final: texto, imágenes y el resto de la interfaz de usuario.
*- Server-side:* todos los procesos que tienen lugar dentro de un servidor: interacción con bases de datos, autenticación de identidad notificaciones push, etc.

## Referencias
* [Client side vs Server side](https://www.cloudflare.com/learning/serverless/glossary/client-side-vs-server-side/)

Fecha: 09/03/2023.