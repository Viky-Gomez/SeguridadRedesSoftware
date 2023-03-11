## Bases

## Descripción
¿Qué significa esto? Creo que tiene algo que ver con las bases: `bDNhcm5fdGgzX3IwcDM1`

## Pistas
* Envíe su respuesta en nuestro formato de bandera. Por ejemplo, si su respuesta fue 'hola', enviaría 'picoCTF{hello}' como bandera.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ echo "bDNhcm5fdGgzX3IwcDM1" | base64
YkROaGNtNWZkR2d6WDNJd2NETTEK
# Decodificamos 
vikyga-picoctf@webshell:~$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
l3arn_th3_r0p35
vikyga-picoctf@webshell:~$ 
'picoCTF{l3arn_th3_r0p35}'
```

## Bandera
**picoCTF{l3arn_th3_r0p35}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| echo | Muestra la línea de texto/cadena que se pasa como un argumento. |
| base64 | Esquema de codificación y decodificación que a menudo se usa para convertir datos binarios a un formato de texto ASCII y viceversa. |

## Referencias
* [echo](https://www.geeksforgeeks.org/echo-command-in-linux-with-examples/)
* [base64](https://lindevs.com/base64-encode-and-decode-in-linux/#:~:text=Base64%20Encode%20and%20Decode%20in%20Linux%201%20Encoding,encoded%20data%3A%201%20echo%20%27SGVsbG8gd29ybGQK%27%20%3E%20encoded_data.txt%20)
