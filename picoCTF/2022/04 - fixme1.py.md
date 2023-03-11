## fixme1.py

## Descripción
Corrija el error de sintaxis en este script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/39/fixme1.py)

## Pistas
* La sangría es muy significativa en Python.
* Para ver el archivo en el webshell, haga: `$ nano fixme1.py`
* Para salir presione Ctrl y x y siga las instrucciones en pantalla.`nano`
* La función no necesita ingeniería inversa para esto. desafiar.`str_xor`

## Solución
``` bash
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/39/fixme1.py
--2023-03-11 20:08:50--  https://artifacts.picoctf.net/c/39/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.42, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

2023-03-11 20:08:50 (287 MB/s) - 'fixme1.py' saved [837/837]

vikyga-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  codebook.txt  file       flag      runme.py    static    static.ltdis.strings.txt  strings
Addadshashanammu.zip  code.py     convertme.py  fixme1.py  ltdis.sh  runme.py.1  static.1  static.ltdis.x86_64.txt   warm
vikyga-picoctf@webshell:~$ python fixme1.py 
  File "/home/vikyga-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
vikyga-picoctf@webshell:~$ nano fixme1.py 
vikyga-picoctf@webshell:~$ python fixme1.py 
That is correct! Heres your flag: 'picoCTF{1nd3nt1ty_cr1515_182342f7}'
vikyga-picoctf@webshell:~$

```

## Bandera
**picoCTF{1nd3nt1ty_cr1515_182342f7}**

## Notas adicionales
* Al ejecutar el archivo "fixme1.py", nos indica un error de identación, por lo que se hizo uso del comando "nano" para poder editar el archivo y poder obtener la bandera.

## Referencias
* [Ninguna]