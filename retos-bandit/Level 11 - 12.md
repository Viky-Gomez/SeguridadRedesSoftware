# Bandit Level 11 → Level 12

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo **.txt**, donde todas las letras minúsculas (a-z) y mayúsculas (A-Z) han sido rotado por 13 posiciones.

## Datos de acceso al nivel
* Servidor: ssh bandit11@bandit.labs.overthewire.org
* Usuario: bandit11
* Contraseña: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solución
*- Forma 1*
``` bash 
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-zA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```
*- Forma 2: Python*
``` bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ python3
Python 3.10.6 (main, Nov 14 2022, 16:10:14) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> codecs.decode('Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi','rot13')
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv'
>>>
```
## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
|ROT13 | Cifrado de sustitución de letras simple que reemplaza una letra con la letra 13 después de ella en el alfabeto.|
| tr | Traduce, elimina y comprime caracteres de la entrada estándar y escribe el resultado en la salida estándar. |

## Referencias
* [ROT13]([ROT13 - Wikipedia, la enciclopedia libre](https://en.wikipedia.org/wiki/ROT13))
* [tr]([Comando Tr en Linux con ejemplos | Linuxizar (linuxize.com)](https://linuxize.com/post/linux-tr-command/))

Fecha: 21/02/2023.