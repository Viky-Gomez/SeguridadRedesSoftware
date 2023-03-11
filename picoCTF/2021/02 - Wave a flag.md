## Wave a flag

## Descripción
¿Se pueden invocar indicadores de ayuda para una herramienta o binario? [Este programa](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) tiene información extraordinariamente útil...

## Pistas
* Este programa solo funcionará en el webshell u otra computadora Linux.
* Para obtener el archivo accesible en su shell, ingrese lo siguiente en el indicador de Terminal: `$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm`
* Ejecute este programa escribiendo lo siguiente en el indicador de Terminal: , pero primero tendrá que hacerlo ejecutable con `$ ./warm``$ chmod +x warm`
* -h y --help son los argumentos más comunes para dar a los programas para obtener más información de ellos!
* No todos los programas implementan funciones de ayuda como -h y --help.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
--2023-03-11 18:41:17--  https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                      100%[==================================>]  10.68K  --.-KB/s    in 0s      

2023-03-11 18:41:17 (383 MB/s) - 'warm' saved [10936/10936]

vikyga-picoctf@webshell:~$ ls -la
total 824
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf    188 Mar 11 18:41 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    178 Mar 11 18:41 .wget-hsts
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm
vikyga-picoctf@webshell:~$ ./warm 
-bash: ./warm: Permission denied
vikyga-picoctf@webshell:~$ chmod +x warm 
vikyga-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
vikyga-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don´t do much, but I do have this flag here: 'picoCTF{b1scu1ts_4nd_gr4vy_30e77291}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{b1scu1ts_4nd_gr4vy_30e77291}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| ./ | Ejecuta un archivo. |
| chmod | Cambia el modo de acceso a un archivo. | 
| +x | Agrega el permiso de ejecución a un archivo específico. |

## Referencias
* [chmod](https://www.geeksforgeeks.org/chmod-command-linux/)
