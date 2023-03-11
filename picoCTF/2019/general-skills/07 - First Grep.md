## First Grep

## Descripción
¿Puedes encontrar la bandera en el [archivo](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? Esto sería realmente tedioso de revisar manualmente, algo me dice que hay una mejor manera.

## Pistas
* grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)

## Solución
``` bash
vikyga-picoctf@webshell:~$ ls -la
total 792
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf    152 Mar  2 19:11 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    178 Mar  2 19:04 .wget-hsts
-rw-r--r-- 1 root           root             4443 Mar 11 00:41 README.txt
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
vikyga-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file 
--2023-03-11 00:54:06--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'
file                                                   100%[============================================================================================================================>]  14.21K  --.-KB/s    in 0s      

2023-03-11 00:54:06 (357 MB/s) - 'file' saved [14551/14551]

vikyga-picoctf@webshell:~$ cat file | grep pico 
'picoCTF{grep_is_good_to_find_things_f77e0797}'
vikyga-picoctf@webshell:~$ 
```

## Bandera
**picoCTF{grep_is_good_to_find_things_f77e0797}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| wget | Descargador de red no interactivo que se utiliza para descargar archivos del servidor.|
| cat | Lee los datos del archivo y da su contenido como salida. | 
| grep | Busca en un archivo un patrón particular de caracteres y muestra todas las líneas que contienen ese patrón. | 

## Referencias
* [wget](https://www.geeksforgeeks.org/wget-command-in-linux-unix/)
* [cat](https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/)
* [grep](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)