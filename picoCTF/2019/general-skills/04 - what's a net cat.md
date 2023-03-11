# what's a net cat?

## Descripción
El uso de netcat (nc) va a ser muy importante. ¿Se puede conectar a puerto para obtener la bandera?`jupiter.challenges.picoctf.org``25103`

## Pistas
* nc [tutorial](https://linux.die.net/man/1/nc)

## Solución
``` bash 
vikyga-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 25103
Youre on your way to becoming the net cat master
'picoCTF{nEtCat_Mast3ry_d0c64587}'
```

## Bandera
**picoCTF{nEtCat_Mast3ry_d0c64587}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| nc | *Netcat*. Permite que dos equipos se conecten y compartan recursos. |

## Referencias
* [Netcat](https://linuxhandbook.com/nc-command/)
