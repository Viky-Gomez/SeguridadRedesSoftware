# Bandit Level 14 → Level 15

## Objetivo
La contraseña para el siguiente nivel se puede recuperar enviando la contraseña del nivel actual para el **puerto 30000 en localhost**.

## Datos de acceso al nivel
* Servidor: ssh bandit14@bandit.labs.overthewire.org
* Usuario: bandit14
* Contraseña: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## Solución
``` bash
bandit14@bandit:~$ nc localhost 30000 
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq 
Correct! 
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt 
^C 
bandit14@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| nc | (Netcat) Permite que dos equipos se conecten y compartan recursos. |

## Referencias
* [nc]([nc Command en Linux: 5 ejemplos prácticos (linuxhandbook.com)](https://linuxhandbook.com/nc-command/))

Fecha: 21/02/2023.