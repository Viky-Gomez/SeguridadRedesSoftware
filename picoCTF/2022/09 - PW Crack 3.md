## PW Crack 3

## Descripción
¿Puedes descifrar la contraseña para obtener la bandera?Descarga el comprobador de contraseñas [aquí](https://artifacts.picoctf.net/c/23/level3.py) y Necesita la [bandera](https://artifacts.picoctf.net/c/23/level3.flag.txt.enc) cifrada y el [hash](https://artifacts.picoctf.net/c/23/level3.hash.bin) en el mismo directorio también.Hay 7 contraseñas potenciales con 1 siendo correcta. Puede encontrarlos por Examinar el script del comprobador de contraseñas.

## Pistas
* Para ver el archivo level3.hash.bin en el webshell, haga: `$ bvi level3.hash.bin`
* Para salir, escriba y presione Entrar: `bvi``:q`
* La función no necesita ingeniería inversa para esto, desafiar.: `str_xor`

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/level3.py 
--2023-03-11 20:56:49--  https://artifacts.picoctf.net/c/23/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.42, 108.156.172.6, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

2023-03-11 20:56:49 (482 MB/s) - 'level3.py' saved [1337/1337]

vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/level3.flag.txt.enc
--2023-03-11 20:57:00--  https://artifacts.picoctf.net/c/23/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.42, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

2023-03-11 20:57:00 (1.38 MB/s) - 'level3.flag.txt.enc' saved [31/31]

vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/level3.hash.bin
--2023-03-11 20:57:10--  https://artifacts.picoctf.net/c/23/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.42, 108.156.172.120, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

2023-03-11 20:57:10 (9.10 MB/s) - 'level3.hash.bin' saved [16/16]

vikyga-picoctf@webshell:~$ ls
Addadshashanammu      code.py       file       flag                 level2.flag.txt.enc  level3.hash.bin  runme.py    static.1                  strings
Addadshashanammu.zip  codebook.txt  fixme1.py  level1.flag.txt.enc  level2.py            level3.py        static.ltdis.strings.txt  warm
README.txt            convertme.py  fixme2.py  level1.py            level3.flag.txt.enc  ltdis.sh         static      static.ltdis.x86_64.txt
vikyga-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: ^Z
[2]+  Stopped                 python level3.py

vikyga-picoctf@webshell:~$ nano level3.py 
vikyga-picoctf@webshell:~$ bvi level3.hash.bin
bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
vikyga-picoctf@webshell:~$ nano level3.py 
vikyga-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 4b17
Welcome back... your flag, user:
'picoCTF{m45h_fl1ng1ng_2b072a90}'
```

## Bandera
**picoCTF{m45h_fl1ng1ng_2b072a90}**

## Notas adicionales
* Al correr el programa se solicita una contraseña para ingresar a la bandera, sin embargo no se contaba con ella. Con ayuda del comando "nano" logré encontrar una lista que contenía la posible contraseña, por lo que ingresé una por una hasta dar con la correcta.

## Referencias
* [Ninguna]