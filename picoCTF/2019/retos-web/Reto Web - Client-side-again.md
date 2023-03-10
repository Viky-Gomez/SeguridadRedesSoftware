## Client-side-again

## Descripción
¿Puedes entrar en este portal súper seguro? ([enlace](https://jupiter.challenges.picoctf.org/problem/6353/)) o https://jupiter.challenges.picoctf.org/problem/6353/

## Pistas
* ¿Qué es la ofuscación?

## Solución
1. Inspeccionar la página.
2. Ubicarse en el apartado "Debugger" y ver el código html.
3. Copiar el código javascript que se ubica dentro del código.
4. Ir a la página [jsnice](http://jsnice.org/) y pegar el código copiado anteriormente.
5. Analizar la versión "limpia y mejorada" del código y obtener la bandera:
``` bash 
'use strict';
/** @type {!Array} */
var _0x5a46 = ["0a029}", "_again_5", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];
(function(data, i) {
  /**
   * @param {number} isLE
   * @return {undefined}
   */
  var write = function(isLE) {
    for (; --isLE;) {
      data["push"](data["shift"]());
    }
  };
... continue
'picoCTF{not_this_again_50a029}'
```

## Bandera
**picoCTF{not_this_again_50a029}**

## Notas adicionales
* *Ofuscación:* Es el proceso de reemplazar información sensible existente en entornos de prueba o de desarrollo con la información que parece información real de producción, pero no sirve para nadie que desee darle mal uso.

## Referencias
* [Ofuscación](https://www.computerweekly.com/es/consejo/Como-las-tecnicas-de-ofuscacion-de-datos-pueden-ayudar-a-proteger-a-las-empresas)

Fecha: 09/03/2023.