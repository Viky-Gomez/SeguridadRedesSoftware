## Codebook

## Descripción
Ejecute la secuencia de comandos de Python en el mismo directorio que: `code.py``codebook.txt`
-   [Descargar code.py](https://artifacts.picoctf.net/c/102/code.py)
-   [Descargar codebook.txt](https://artifacts.picoctf.net/c/102/codebook.txt)

## Pistas
* En el webshell, utilícelo para ver si ambos archivos están en el directorio en el que se encuentra en `ls`
* La función no necesita ingeniería inversa para esto, desafiar: `str_xor`

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/102/code.py
--2023-03-11 20:05:28--  https://artifacts.picoctf.net/c/102/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.6, 108.156.172.120, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.6|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

2023-03-11 20:05:29 (426 MB/s) - 'code.py' saved [1278/1278]

vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/102/codebook.txt
--2023-03-11 20:05:46--  https://artifacts.picoctf.net/c/102/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.42, 108.156.172.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'
 
2023-03-11 20:05:46 (11.7 MB/s) - 'codebook.txt' saved [27/27]

vikyga-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  codebook.txt  file  ltdis.sh  static.ltdis.x86_64.txt  warm
Addadshashanammu.zip  code.py     convertme.py  flag  runme.py  static      static.ltdis.strings.txt  strings
vikyga-picoctf@webshell:~$ cat codebook.txt 
azbycxdwevfugthsirjqkplomn
vikyga-picoctf@webshell:~$ python code.py 
'picoCTF{c0d3b00k_455157_197a982c}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{c0d3b00k_455157_197a982c}**

## Notas adicionales
* Ninguna.

## Referencias
* [Ninguna]