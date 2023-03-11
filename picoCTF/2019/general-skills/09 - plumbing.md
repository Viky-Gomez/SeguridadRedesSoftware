## plumbing

## Descripción
A veces es necesario manejar datos de proceso fuera de un archivo. ¿Puedes encontrar una manera de mantener la salida de este programa y buscar la bandera? Conéctese a: `jupiter.challenges.picoctf.org 14291`

## Pistas
* Recuerde que el formato de la bandera es picoCTF{XXXX}.
* ¿Qué es pipe? No, no ese tipo de pipa ... Este [tipo](http://www.linfo.org/pipes.html)

## Solución
``` bash 
vikyga-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep pico
'picoCTF{digital_plumb3r_ea8bfec7}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{digital_plumb3r_ea8bfec7}**

## Notas adicionales
* *Pipes ( | ):* es una forma de redirección que se utiliza en Linux y otros sistemas operativos similares a Unix para enviar la salida de un programa a otro programa para su posterior procesamiento.

## Referencias
* [Pipes](http://www.linfo.org/pipes.html)
