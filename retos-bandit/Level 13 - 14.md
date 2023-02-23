# Bandit Level 13 → Level 14

## Objetivo
La contraseña para el siguiente nivel se almacena en /**etc/bandit_pass/bandit14 y sólo puede ser leída por el usuario bandido14**. Para este nivel, no obtienes la siguiente contraseña, pero obtener una clave SSH privada que se puede utilizar para iniciar sesión en el siguiente nivel.

## Datos de acceso al nivel
* Servidor: ssh bandit13@bandit.labs.overthewire.org
* Usuario: bandit13
* Contraseña: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

## Solución
``` bash 
bandit13@bandit:~$ ls sshkey.private 
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220 
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established. ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY. 
This key is not known by any other names Are you sure you want to continue connecting (yes/no/[fingerprint])? Yes
... 
...  
```
``` bash
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14 fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq 
bandit14@bandit:~$ exit 
logout 
Connection to localhost closed. 
bandit13@bandit:~$ exit 
logout 
Connection to bandit.labs.overthewire.org closed
```

## Notas Adicionales

|Comando | Descripcion |
|-----|-------|
| ssh | Proporciona una conexión cifrada segura entre dos hosts a través de una red insegura. |

## Referencias
* [ssh]([¿Qué Es El Comando Ssh En Linux? - FAQs De Tecnología (tecnofaq.com)](https://tecnofaq.com/que-es-el-comando-ssh-en-linux/#:~:text=Comando%20SSH%20en%20Linux%20El%20comando%20ssh%20proporciona,transferencias%20de%20archivos%20y%20para%20canalizar%20otras%20aplicaciones.))

Fecha: 21/02/2023.