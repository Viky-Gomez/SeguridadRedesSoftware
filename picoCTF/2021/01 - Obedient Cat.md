## Obedient Cat

## Descripción
Este archivo tiene una bandera a la vista (también conocida como "in-the-clear"). [Descargar bandera](https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag).

## Pistas
* Cualquier sugerencia sobre cómo ingresar un comando en la Terminal (como el siguiente), comenzará con un '$'... todo después del signo de dólar se escribirá (o copiará y pegará) en su Terminal.
* Para obtener el archivo accesible en su shell, ingrese lo siguiente en el indicador de Terminal: `$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag`
* $ man cat

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
--2023-03-11 18:36:24--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                      100%[==================================>]      34  --.-KB/s    in 0s      

2023-03-11 18:36:24 (14.5 MB/s) - 'flag' saved [34/34]

vikyga-picoctf@webshell:~$ ls -la
total 812
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf    176 Mar 11 18:36 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    215 Mar 11 18:36 .wget-hsts
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
vikyga-picoctf@webshell:~$ cat flag
'picoCTF{s4n1ty_v3r1f13d_2aa22101}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{s4n1ty_v3r1f13d_2aa22101}**

## Notas adicionales
* Ninguna.

## Referencias
* [Ninguna]