## Objetivo
El objetivo de este nivel es que inicies sesión en el juego usando SSH. El host al que necesita conectarse es **bandit.labs.overthewire.org**, en el puerto 2220. El nombre de usuario es bandit0 y la contraseña es **bandit0**. Una vez Inicie sesión, vaya a la página de Nivel 1 para averiguar cómo superar el Nivel 1.

## Datos de acceso al nivel
* Servidor:  ssh bandit0@bandit.labs.overthewire.org
* Usuario: bandit0
* Contraseña: bandit0

## Solución

``` bash 
C:\Users\vikyg>ssh bandit0@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames
``` 

## Notas Adicionales
* Al acceder por primera vez se pide agregar el servidor a la lista de hosts conocidos, al ingresar estamos en un servidor de Linux para pruebas.

## Referencias
*   [Secure Shell (SSH) en Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
-   [Cómo usar SSH en wikiHow](https://www.wikihow.com/Use-SSH)

Fecha: 14/02/2023