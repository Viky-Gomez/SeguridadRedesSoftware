## strings it

## Descripción
¿Puede encontrar la bandera en el [archivo](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) sin ejecutarla?

## Pistas
* [strings](https://linux.die.net/man/1/strings)

## Solución
*- Descarga del archivo file.*
``` bash 
vikyga-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings

vikyga-picoctf@webshell:~$ strings strings | grep pico 
'picoCTF{5tRIng5_1T_d66c7bb7}'
vikyga-picoctf@webshell:~$ 
```

## Bandera
**picoCTF{5tRIng5_1T_d66c7bb7}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| wget | Descarga archivos de la web utilizando protocolos HTTP, HTTPS, FTP. |
| strings | Imprime las cadenas de caracteres imprimibles en archivos. | 

## Referencias
* [wget](https://linuxize.com/post/wget-command-examples/)
* [strings](https://www.howtoforge.com/linux-strings-command/)
