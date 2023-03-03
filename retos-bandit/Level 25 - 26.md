# Bandit Level 25 → Level 26

## Objetivo
Iniciar sesión en bandit26 desde bandit25 debería ser bastante fácil... El shell para el usuario bandit26 no es /**bin/bash**, sino algo más. Averigüe qué es, cómo funciona y cómo salir de él.

## Datos de acceso al nivel
* Servidor: ssh bandit25@bandit.labs.overthewire.org
* Usuario: bandit25
* Contraseña: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

## Solución
``` bash 
bandit25@bandit:~$ ls 
bandit26.sshkey 
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220 

Connection to localhost closed.
bandit25@bandit:~$ cat /etc/passwd | grep bandit26 bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext 
bandit25@bandit:~$ cat /usr/bin/showtext 
#!/bin/sh export TERM=linux 
exec more ~/text.txt 
exit 0 
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220
--More--(83%) 
v
"~/text.txt" [readonly] 6L, 258B 
:e /etc/bandit_pass/bandit26 
'c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1'
~ 
~ 
~ 
~ 
"/etc/bandit_pass/bandit26" [readonly] 1L, 33B 
:!q
Press ENTER or type command to continue 
q 
~ 
~ 
------------------------ 
Connection to localhost closed. 
bandit25@bandit:~ exit
```
## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| more | Nos sirve para ver los archivos de texto en el símbolo del sistema, mostrando una pantalla a la vez en caso de que sea grande.

## Referencias
* [more](https://www.geeksforgeeks.org/more-command-in-linux-with-examples/)

Fecha: 28/02/2023.