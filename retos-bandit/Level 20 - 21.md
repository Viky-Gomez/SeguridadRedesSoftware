# Bandit Level 20 → Level 21

## Objetivo
Hay un binario setuid en el home directory que hace lo siguiente: Realiza una conexión a localhost en el puerto que especifique como argumento de línea de comandos. A continuación, lee una línea de texto de la conexión y la compara con la contraseña del nivel anterior (Bandit20). Si la contraseña es correcta, transmitirá la contraseña para el siguiente nivel (Bandit21).

## Datos de acceso al nivel
* Servidor: ssh bandit20@bandit.labs.overthewire.org
* Usuario: bandit20
* Contraseña: VxCazJaVykI6W36BkBU0mJTCM8rR95XT

## Solución
``` bash 
bandit20@bandit:~$ nc -lnvp 6666 <<<VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[2] 3122221
bandit20@bandit:~$ Listening on 0.0.0.0 6666

bandit20@bandit:~$ ./suconnect 6666
Connection received on 127.0.0.1 49362
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
'NvEJF7oVjkddltPSrdKEFOllh9V1IBcq'
bandit20@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| nc | Abre comunicación por medio de puertos. |
| & | Background. | 

## Referencias
* [nc](https://www.neoguias.com/comando-nc/)

Fecha: 23/02/2023.