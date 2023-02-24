# Bandit Level 7 → Level 8

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo **.txt**  junto a la palabra **millonésima**.

## Datos de acceso al nivel
* Servidor: ssh bandit7@bandit.labs.overthewire.org
* Usuario: bandit7
* Contraseña: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Solución
``` bash
C:\Users\vikyg>ssh bandit7@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit7@bandit.labs.overthewire.org's password:
```
``` bash 
bandit7@bandit:~$ ls data.txt 
bandit7@bandit:~$ wc data.txt 
	98567 197133 4184396 data.txt 
bandit7@bandit:~$ grep millionth data.txt 
	millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP 
bandit7@bandit:~$ cat data.txt | grep millionth millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP 
bandit7@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| grep | Busca un patrón que definimos en un archivo de texto. |
| wc | Averigua el número de líneas en un archivo específico. |


## Referencias
* [grep](https://www.hostinger.es/tutoriales/comando-grep-linux#:~:text=El%20comando%20grep%20perteneciente%20a%20la%20familia%20Unix,imprimir%C3%A1%20la%20l%C3%ADnea%20o%20l%C3%ADneas%20que%20la%20contengan.)
* [wc](https://www.geeksforgeeks.org/wc-command-linux-examples/)

Fecha: 16/02/2023.