## Static ain't always noise

## Descripción
¿Puedes ver los datos en este binario: [estático](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? ¡Este [script BASH](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) podría ayudar!

## Pistas
* Ninguna.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static
--2023-03-11 19:02:07--  https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                    100%[==================================>]   8.18K  --.-KB/s    in 0s      

2023-03-11 19:02:07 (258 MB/s) - 'static' saved [8376/8376]

vikyga-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh
--2023-03-11 19:08:18--  https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                               100%[============================================================================================================================>]     785  --.-KB/s    in 0s      

2023-03-11 19:08:18 (507 MB/s) - 'ltdis.sh' saved [785/785]

vikyga-picoctf@webshell:~$ ls -la
total 856
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf   4096 Mar 11 19:08 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    215 Mar 11 19:08 .wget-hsts
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm

vikyga-picoctf@webshell:~$ chmod +x ltdis.sh 
vikyga-picoctf@webshell:~$ chmod +x static   
vikyga-picoctf@webshell:~$ ./ltdis.sh ./static
Attempting disassembly of ./static ...
Disassembly successful! Available at: ./static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in ./static have been written to ./static.ltdis.strings.txt with file offset
vikyga-picoctf@webshell:~$ ls -la
total 868
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf   4096 Mar 11 19:14 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    215 Mar 11 19:08 .wget-hsts
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf    785 Mar 16  2021 ltdis.sh
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static.1
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1668 Mar 11 19:14 static.ltdis.strings.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   6499 Mar 11 19:14 static.ltdis.x86_64.txt
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm
vikyga-picoctf@webshell:~$  cat static.ltdis.strings.txt | grep pico
   1020 'picoCTF{d15a5m_t34s3r_f6c48608}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{d15a5m_t34s3r_f6c48608}**

## Notas adicionales
* Ninguna.

## Referencias
* [Ninguna]