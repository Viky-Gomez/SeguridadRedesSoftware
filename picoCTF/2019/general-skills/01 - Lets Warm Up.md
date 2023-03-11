# Lets Warm Up

## Descripción
Si te dijera que una palabra comienza con 0x70 en hexadecimal, ¿con qué comenzaría en ASCII?

## Pistas
* Envíe su respuesta en nuestro formato de bandera. Por ejemplo, si su respuesta fue 'hola', enviaría 'picoCTF{hello}' como bandera.

## Solución
``` bash 
vikyga-picoctf@webshell:~$ python 
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x70)
112
>>> chr(112)
'p'
>>> 
```

## Bandera
**picoCTF{p}**

## Notas adicionales
* *int(string, base):* devuelve un número entero de un objeto dado o convierte un número en una base dada a decimal. 
* *chr(number):* devuelve el carácter que representa el unicode especificado.

## Referencias
* [Función int](https://barcelonageeks.com/funcion-int-en-python/)
* [Función chr](https://www.w3schools.com/python/ref_func_chr.asp)

