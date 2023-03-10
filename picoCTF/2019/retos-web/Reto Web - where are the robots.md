# where are the robots

## Descripción
¿Puedes encontrar los robots? ([enlace](https://jupiter.challenges.picoctf.org/problem/60915/)) o https://jupiter.challenges.picoctf.org/problem/60915/

## Pistas
* ¿Qué parte del sitio web podría decirte dónde el creador no quiere que mires?

## Solución
1.  Inspeccionar el código fuente de la página.
2. Ingresar a la url el sufijo "/robots.txt":  
	User-agent: *  
	Disallow: /8028f.html
3. Copiar el valor de Disallow y agregarlo como un nuevo sufijo a la url:
		Guess you found the robots  
	**picoCTF{ca1cu1at1ng_Mach1n3s_8028f}**

## Bandera
**picoCTF{ca1cu1at1ng_Mach1n3s_8028f}**

## Notas adicionales
* *robots.txt:* indica a los rastreadores de motores de búsqueda a qué URL pueden acceder en tu sitio. Su principal propósito es evitar la sobrecarga de solicitudes para tu sitio.

## Referencias
* [robots.txt](https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es-419)

Fecha: 09/03/2023.