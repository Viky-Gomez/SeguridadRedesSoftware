## Nice netcat...

## Descripción
Hay un buen programa con el que puedes hablar usando este comando en un shell: , pero no habla inglés ...`$ nc mercury.picoctf.net 35652`

## Pistas
* Puedes practicar el uso de netcat con este problema de picoGym: [¿qué es un netcat?](https://play.picoctf.org/practice/challenge/34)
* Puedes practicar ASCII de lectura y escritura con este problema de picoGym: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

## Solución
``` bash 
vikyga-picoctf@webshell:~$ nc mercury.picoctf.net 35652
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
57 
98 
51 
98 
55 
51 
57 
50 
125 
10 
'picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}'
```

## Bandera
**picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}**

## Notas adicionales
1. Los valores obtenidos en la terminal son una representación decimal de los caracteres ASCII.
2. Con ayuda de "Cyberchef" y la función "FromCharCode" se logró "decodificar" y obtener la bandera correspondiente.

## Referencias
* [Cyberchef](https://gchq.github.io/CyberChef/)
