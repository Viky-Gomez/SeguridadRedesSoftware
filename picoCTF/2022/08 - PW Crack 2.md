## PW Crack 2

## Descripción
¿Puedes descifrar la contraseña para obtener la bandera?Descarga el comprobador de contraseñas [aquí](https://artifacts.picoctf.net/c/18/level2.py) y Necesita el [indicador](https://artifacts.picoctf.net/c/18/level2.flag.txt.enc) cifrado en el mismo directorio también.

## Pistas
* ¿Le resulta familiar esa codificación?
* La función no necesita ingeniería inversa para esto,  desafiar.`str_xor`

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level2.py
--2023-03-11 20:50:01--  https://artifacts.picoctf.net/c/18/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.6, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'
  
2023-03-11 20:50:01 (267 MB/s) - 'level2.py' saved [914/914]

vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level2.flag.txt.enc
--2023-03-11 20:50:14--  https://artifacts.picoctf.net/c/18/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.6, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

2023-03-11 20:50:14 (10.4 MB/s) - 'level2.flag.txt.enc' saved [31/31]

vikyga-picoctf@webshell:~$ ls -la
total 920
drwxr-xr-x 5 vikyga-picoctf vikyga-picoctf   4096 Mar 11 20:50 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
drwxrwxr-x 3 vikyga-picoctf vikyga-picoctf     19 Mar 11 20:09 .local
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf    212 Mar 11 20:41 .python_history
drwx------ 2 vikyga-picoctf vikyga-picoctf     48 Mar 11 19:39 .ssh
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    178 Mar 11 19:28 .wget-hsts
drwxr-xr-x 3 vikyga-picoctf vikyga-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1278 Mar 12  2022 code.py
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     27 Mar 12  2022 codebook.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1189 Mar 12  2022 convertme.py
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    835 Mar 11 20:31 fixme1.py
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1030 Mar 11 20:34 fixme2.py
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     30 Jan  4  2022 level1.flag.txt.enc
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    876 Jan  4  2022 level1.py
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     31 Jan  4  2022 level2.flag.txt.enc
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    914 Jan  4  2022 level2.py
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    270 Jan  4  2022 runme.py
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1668 Mar 11 19:14 static.ltdis.strings.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   6499 Mar 11 19:14 static.ltdis.x86_64.txt
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm

vikyga-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: ^Z
[1]+  Stopped                 python level2.py
vikyga-picoctf@webshell:~$ nano level2.py 
vikyga-picoctf@webshell:~$ python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
39ce
>>> 
vikyga-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
'picoCTF{tr45h_51ng1ng_502ec42e}'
```

## Bandera
**picoCTF{tr45h_51ng1ng_502ec42e}**

## Notas adicionales
* Dentro del archivo "level2.py" se encuentra una función que contiene una validación para obtener la contraseña que se solicita al ejecutar dicho archivo. Con ayuda de la función "print()" se logró decodificar e imprimir la contraseña del programa y así obtener la bandera.

## Referencias
* [Ninguna]