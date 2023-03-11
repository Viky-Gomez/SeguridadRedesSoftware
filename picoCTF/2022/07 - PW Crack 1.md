## PW Crack 1

## Descripción
¿Puedes descifrar la contraseña para obtener la bandera?Descarga el comprobador de contraseñas [aquí](https://artifacts.picoctf.net/c/52/level1.py) y necesita el [indicador](https://artifacts.picoctf.net/c/52/level1.flag.txt.enc) cifrado en el mismo directorio también.

## Pistas
* Para ver el archivo en el webshell, haga:  `$ nano level1.py`
* Para salir presione Ctrl y x y siga las instrucciones en pantalla.`nano`
* La función no necesita ingeniería inversa para esto, desafiar: `str_xor`

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/52/level1.py
--2023-03-11 20:43:16--  https://artifacts.picoctf.net/c/52/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.6, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

2023-03-11 20:43:16 (45.4 MB/s) - 'level1.py' saved [876/876]

vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/52/level1.flag.txt.enc
--2023-03-11 20:43:30--  https://artifacts.picoctf.net/c/52/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.6, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

2023-03-11 20:43:30 (10.7 MB/s) - 'level1.flag.txt.enc' saved [30/30]

vikyga-picoctf@webshell:~$ ls -la
total 912
drwxr-xr-x 5 vikyga-picoctf vikyga-picoctf   4096 Mar 11 20:43 .
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
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    270 Jan  4  2022 runme.py
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1668 Mar 11 19:14 static.ltdis.strings.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   6499 Mar 11 19:14 static.ltdis.x86_64.txt
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm
vikyga-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: ^C
Traceback (most recent call last):
  File "/home/vikyga-picoctf/level1.py", line 28, in <module>
    level_1_pw_check()
  File "/home/vikyga-picoctf/level1.py", line 18, in level_1_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

vikyga-picoctf@webshell:~$ nano level1.py          
vikyga-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a 
Welcome back... your flag, user:
'picoCTF{545h_r1ng1ng_fa343060}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{545h_r1ng1ng_fa343060}**

## Notas adicionales
* Al ejecutar el archivo "level1.py" el programa solicita una contraseña la cual no tenemos, con el comando "nano" se logró ver su contenido y dentro de un ciclo de validación se encontraba la contraseña correcta que se solicita, al ingresarla obtuvimos la bandera correspondiente. 

## Referencias
* [Ninguna]