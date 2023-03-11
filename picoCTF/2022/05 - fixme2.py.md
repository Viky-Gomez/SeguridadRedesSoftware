## fixme2.py

## Descripción
Corrija el error de sintaxis en el script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/65/fixme2.py)

## Pistas
* ¿Son la igualdad y la asignación el mismo símbolo?
* Para ver el archivo en el webshell, haga: `$ nano fixme2.py`
* Para salir presione Ctrl y x y siga las instrucciones en pantalla.`nano`
* La función no necesita ingeniería inversa para esto, desafiar: `str_xor`

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/65/fixme2.py
--2023-03-11 20:33:03--  https://artifacts.picoctf.net/c/65/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.6, 108.156.172.120, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.6|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'  

2023-03-11 20:33:03 (248 MB/s) - 'fixme2.py' saved [1029/1029]

vikyga-picoctf@webshell:~$ python fixme2.py 
  File "/home/vikyga-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
vikyga-picoctf@webshell:~$ nano fixme2.py 
vikyga-picoctf@webshell:~$ python fixme2.py 
That is correct! Heres your flag: 'picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}**

## Notas adicionales
* Al ejecutar el archivo "fixme.py" nos indica que existe un error de intaxis dentro de un ciclo if, esto se debe a que se requería agregar un signo "=" ya que estaba haciendo una comparación. Con el comando "nano" se logró cambiar ese error y así se obtuvo la bandera.

## Referencias
* [Ninguna]