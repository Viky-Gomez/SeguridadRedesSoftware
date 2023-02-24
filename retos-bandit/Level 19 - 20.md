# Bandit Level 19 → Level 20

## Objetivo
Para obtener acceso al siguiente nivel, debe usar el binario setuid en el directorio principal. Ejecútalo sin argumentos para averiguar cómo para usarlo. La contraseña para este nivel se puede encontrar en el habitual place (/etc/bandit_pass), después de haber utilizado el binario setuid.

## Datos de acceso al nivel
* Servidor: ssh bandit19@bandit.labs.overthewire.org
* Usuario: bandit19
* Contraseña: awhqfNnAbc1naukrpqDYcF95h7HoMTrC

## Solución
``` bash
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit20 bandit19 14876 Feb 21 22:03 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| s | Dar permisos de sudo a distintos archivos (nivel usuario o grupo). |
| setuid / setgid | Permiten a los usuarios ejecutar un ejecutable con los permisos del sistema de archivos del propietario o grupo del ejecutable respectivamente y cambiar el comportamiento en los directorios. |

## Referencias
* [setuid/setgid](https://en.wikipedia.org/wiki/Setuid)

Fecha: 23/02/2023.