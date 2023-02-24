# Bandit Level 10 → Level 11

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo **.txt**, que contiene datos codificados en base64.

## Datos de acceso al nivel
* Servidor: ssh bandit10@bandit.labs.overthewire.org
* Usuario: bandit10
* Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solución
``` bash 
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "hola mundo"
hola mundo
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

*- Solución Python*
``` bash 
bandit10@bandit:~$ python3
Python 3.10.6 (main, Nov 14 2022, 16:10:14) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> cadena=open('data.txt', 'r').read()
>>> base64.b64decode(cadena)
b'The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM\n'
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| echo | Mostrar una línea de texto / cadena en la salida estándar o un archivo.|
| base64 | Representación de datos binarios. |
| -n | Nueva línea. | 
| -d | Decodificar una cadena. |

## Referencias
* [base64](https://en.wikipedia.org/wiki/Base64)
* [echo](https://phoenixnap.com/kb/echo)

Fecha: 21/02/2023.