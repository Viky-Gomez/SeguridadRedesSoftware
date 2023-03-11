## Glitch Cat

## Descripción
¡Nuestro servicio de impresión de banderas ha comenzado a brillar! `$ nc saturn.picoctf.net 51109`

## Pistas
* ASCII es una de las codificaciones más comunes utilizadas en programación.
* ¡Sabemos que la salida de glitch es válida Python, de alguna manera!
* Presione Ctrl y c en su teclado para cerrar su conexión y volver a la símbolo del sistema.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ nc saturn.picoctf.net 51109
picoCTF{gl17ch_m3_n07_ + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
^C
vikyga-picoctf@webshell:~$ python  
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(picoCTF{gl17ch_m3_n07_ + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')
'picoCTF{gl17ch_m3_n07_bda68f75}'
>>> 
```

## Bandera
**picoCTF{gl17ch_m3_n07_bda68f75}**

## Notas adicionales
* Al ingresar el "netcat" se realizó una conexión al servidor indicado y con ello se obtuvieron unas líneas que nos podrían dar la bandera. Dentro de python se pegaron dichas líneas dentro de una función "print()" y con ello se obtuvo la bandera correspondiente.

## Referencias
* [Ninguna]