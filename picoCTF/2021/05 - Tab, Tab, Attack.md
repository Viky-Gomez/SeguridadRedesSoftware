## Tab, Tab, Attack

## Descripción
El uso de tabcomplete en la Terminal agregará años a su vida, especialmente cuando se trata de largas estructuras de directorios y nombres de archivo: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)

## Pistas
* Después de 'descomprimir', este problema se puede resolver con 11 pulsaciones de botón... (principalmente Tab)...

## Solución
``` bash 
vikyga-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip
--2023-03-11 19:28:48--  https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                  100%[=========================================================================>]   4.41K  --.-KB/s    in 0s      

2023-03-11 19:28:48 (1.83 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]

vikyga-picoctf@webshell:~$ ls -la
total 876
drwxr-xr-x 2 vikyga-picoctf vikyga-picoctf   4096 Mar 11 19:28 .
drwxr-xr-x 3 root           root               28 Mar  2 18:36 ..
-rw------- 1 vikyga-picoctf vikyga-picoctf    708 Mar  9 19:27 .bash_history
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 vikyga-picoctf vikyga-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 vikyga-picoctf vikyga-picoctf     73 Mar  2 18:55 .python_history
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf    178 Mar 11 19:28 .wget-hsts
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root             4443 Mar 11 18:09 README.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf     34 Mar 16  2021 flag
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf    785 Mar 16  2021 ltdis.sh
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   8376 Mar 16  2021 static.1
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   1668 Mar 11 19:14 static.ltdis.strings.txt
-rw-rw-r-- 1 vikyga-picoctf vikyga-picoctf   6499 Mar 11 19:14 static.ltdis.x86_64.txt
-rwxrwxrwx 1 vikyga-picoctf vikyga-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 vikyga-picoctf vikyga-picoctf  10936 Mar 16  2021 warm
vikyga-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
vikyga-picoctf@webshell:~$ ls Addadshashanammu
Almurbalarammi
vikyga-picoctf@webshell:~$ ls -R Almurbalarammi
ls: cannot access 'Almurbalarammi': No such file or directory
vikyga-picoctf@webshell:~$ ls -R Addadshashanammu
Addadshashanammu:
Almurbalarammi

Addadshashanammu/Almurbalarammi:
Ashalmimilkala

Addadshashanammu/Almurbalarammi/Ashalmimilkala:
Assurnabitashpi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi:
Maelkashishi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi:
Onnissiralis

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis:
Ularradallaku

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku:
fang-of-haynekhtnamet
vikyga-picoctf@webshell:~$ strings Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico
*ZAP!* 'picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}'
vikyga-picoctf@webshell:~$ 
```

## Bandera
**picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| unzip | Descomprime y extrae el contenido de un archivo con extensión ".zip". |
| strings | Imprime las cadenas de caracteres imprimibles en archivos. | 

## Referencias
* [unzip](https://linuxhandbook.com/unzip-command/)
* [strings](https://www.howtoforge.com/linux-strings-command/#:~:text=Linux%20Strings%20command.%20The%20Strings%20command%20basically%20prints,file%20given%2C%20GNU%20strings%20prints%20the%20printable%20character.)