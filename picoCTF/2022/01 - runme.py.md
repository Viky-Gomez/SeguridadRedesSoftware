## runme.py

## Descripción
Ejecute el script para obtener la marca. Descarga el script con tu navegador o con en el webshell. `runme.py``wget` 
[Descargar runme.py script de Python](https://artifacts.picoctf.net/c/86/runme.py)

## Pistas
* Si tiene Python en su computadora, puede descargar el script normalmente y ejecútalo. De lo contrario, use el comando en el webshell: `wget`
* Para usar en el webshell, primero haga clic derecho en el enlace de descarga y seleccione 'Copiar enlace' o 'Copiar dirección de enlace'. `wget`
* Escriba todo después del signo de dólar en el webshell: y, a continuación, pegue el enlace después del espacio después y presione Entrar. Esto hará ¡Descargue el script en el Webshell para que pueda ejecutarlo! `$ wget` `wget`
* Finalmente, para ejecutar el script, escriba todo después del signo de dólar y luego presione enter: ¡Debería tener la bandera ahora! `$ python3 runme.py`

## Solución
``` bash
vikyga-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/86/runme.py
--2023-03-11 19:58:22--  https://artifacts.picoctf.net/c/86/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.74, 108.156.172.6, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py.1'

runme.py.1                            100%[=========================================================================>]     270  --.-KB/s    in 0s      

2023-03-11 19:58:22 (11.0 MB/s) - 'runme.py' saved [270/270]

vikyga-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  flag      runme.py    static    static.ltdis.strings.txt  strings
Addadshashanammu.zip  file        ltdis.sh  static.1  static.ltdis.x86_64.txt   warm
vikyga-picoctf@webshell:~$ python runme.py 
'picoCTF{run_s4n1ty_run}'
vikyga-picoctf@webshell:~$
```

## Bandera
**picoCTF{run_s4n1ty_run}**

## Notas adicionales
|Comando | Descripcion |
|-----|-------|
| python | Invoca y ejecuta el contenido de un archivo ".py". |

## Referencias
* [python](https://docs.python.org/3/using/cmdline.html)