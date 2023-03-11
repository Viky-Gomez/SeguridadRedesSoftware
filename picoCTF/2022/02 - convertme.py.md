## convertme.py

## Descripción
Ejecute el script de Python y convierta el número dado de decimal a binario a Consigue la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/31/convertme.py)

## Pistas
* Busque una aplicación de conversión de números decimales a binarios en la web o use su ¡Calculadora de computadora!
* La función no necesita ingeniería inversa para esto: desafiar `str_xor`
* Si tiene Python en su computadora, puede descargar el script normalmente y Ejecútalo. De lo contrario, use el comando en el webshell: `wget`
* Para usar en el webshell, primero haga clic derecho en el enlace de descarga y seleccione 'Copiar enlace' o 'Copiar dirección de enlace: `wget`
* Escriba todo después del signo de dólar en el webshell: y, a continuación, Pegue el enlace después del espacio después y presione Entrar. Esto hará ¡Descargue el script en el Webshell para que pueda ejecutarlo! `$ wget` `wget`
* Finalmente, para ejecutar el script, escriba todo después del signo de dólar y luego Presione Entrar: `$ python3 convertme.py`

## Solución
``` bash
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/31/convertme.py
--2023-03-11 20:00:45--  https://artifacts.picoctf.net/c/31/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.42, 108.156.172.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                          100%[=========================================================================>]   1.16K  --.-KB/s    in 0s      

2023-03-11 20:00:45 (473 MB/s) - 'convertme.py' saved [1189/1189]

vikyga-picoctf@webshell:~$ ls
Addadshashanammu      README.txt    file  ltdis.sh  static.ltdis.x86_64.txt  warm
Addadshashanammu.zip  convertme.py  flag  runme.py  static  static.ltdis.strings.txt  strings
vikyga-picoctf@webshell:~$ python convertme.py 
If 45 is in decimal base, what is it in binary base?
Answer: 101101
That is correct! Heres your flag: 'picoCTF{4ll_y0ur_b4535_9c3b7d4d}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{4ll_y0ur_b4535_9c3b7d4d}**

## Notas adicionales
* Al ejecutar el archivo "convertme.py" nos pide que ingresemos el valor en binario de un número aleatorio en base decimal, al ingresarlo correctamente nos da la bandera.

## Referencias
* [Ninguna]