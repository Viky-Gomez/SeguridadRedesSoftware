# 2Warm

## Descripción
¿Se puede convertir el número 42 (base 10) a binario (base 2)?

## Pistas
* Envíe su respuesta en el formato de bandera de nuestra competencia. Por ejemplo, si su respuesta fue '11111', enviaría 'picoCTF{11111}' como bandera.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ python 
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(42)
'0b101010'
>>> 
```

## Bandera
**picoCTF{101010}**

## Notas adicionales
* *bin(x):* devuelve la cadea binaria de un número entero dado.

## Referencias
* [Función bin](https://www.geeksforgeeks.org/bin-in-python/)
