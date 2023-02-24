# Bandit Level 12→ Level 13

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo **.txt**, que es un hexdump de un archivo que se ha comprimido repetidamente. Para este nivel puede ser útil crear un directorio bajo /tmp en que puede trabajar usando mkdir. Por ejemplo: mkdir /tmp/myname123. A continuación, copie el archivo de datos mediante cp y cámbiele el nombre mediante mv (lea el manpages!).

## Datos de acceso al nivel
* Servidor: ssh bandit12@bandit.labs.overthewire.org
* Usuario: bandit12
* Contraseña: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Solución
``` bash
bandit12@bandit:~$ xxd -r data.txt | file - 
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat |file - 
/dev/stdin: bzip2 compressed data, block size = 900k 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat |file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat |file - 
/dev/stdin: POSIX tar archive (GNU) 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file - 
/dev/stdin: POSIX tar archive (GNU) 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file - 
/dev/stdin: bzip2 compressed data, block size = 900k 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file - 
/dev/stdin: POSIX tar archive (GNU) 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file - 
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file - 
/dev/stdin: ASCII text 
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat 
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

## Notas Adicionales
* *Volcado Hexadecimal:* es una vista hexadecimal (en pantalla o papel) de datos informáticos, desde la memoria o desde un archivo  o dispositivo de almacenamiento.

|Comando | Descripcion |
|-----|-------|
| xxd | Permite crear un volcado hexadecimal o incluso hacer lo contrario.|
| gzip | Permite reducir el tamaño de un archivo y mantener el modo de archivo original, la propiedad y la marca de tiempo. |
| zcat | Permite ver el contenido de un archivo comprimido. |
| tar | Empaqueta archivos. | 

## Referencias
* [Volcado Hexadecimal](https://en.wikipedia.org/wiki/Hex_dump)
* [xxd](linux-console.nethttps://es.linux-console.net/?p=3429#gsc.tab=0)
* [gzip](https://linuxize.com/post/gzip-command-in-linux/)
* [zcat](https://linuxpasion.com/tutorial-de-comando-linux-zcat-para-principiantes-5-ejemplos)
* [tar](https://es.ccm.net/ordenadores/linux/2988-el-comando-tar/)

Fecha: 21/02/2023.