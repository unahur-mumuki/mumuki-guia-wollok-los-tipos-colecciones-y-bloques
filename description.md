Los objetos no tienen todos las mismas características, para cada objeto hay algunas cosas que puedo hacer y otras no.

Por ejemplo un número lo puedo multiplicar por otro número, pero un ave (como Pepita) no. De ahí la diferencia entre las dos pruebas que siguen.

```wollok
>>> 4 * 8
32
>>> pepita * 8
wollok.lang.MessageNotUnderstoodException: pepita[energia=0] does not understand *(param1)
```

Si pienso en qué puedo hacer con cada objeto, entonces todos los números, o mejor dicho, tienen mucho en común: los puedo sumar, multiplicar, obtener el mínimo de dos números (p.ej. `4.min(2)`), etc..

De su lado, las distintas aves que definimos en la "serie de Pepita", como `pepita`, `pepon`, `pipa`, etc., también comparten varios de los mensajes que entienden, que son "las cosas" que se puede hacer con ellas: puedo pedirles que coman, que vuelen, y que hagan lo que quieran. El entrenador `roque` aprovecha esto para poder tomar a cualquiera de ellas como pupilo.  
Decimos que estos objetos **comparten un tipo** que es el de "objeto que `roque` puede entrenar".  
Todos los números comparten el **tipo** número.

Los objetos que "vienen con Wollok" corresponden a los que llamamos los _tipos básicos_: números, booleanos, Strings y algún otro.  
Los objetos que programamos nosotros van compartiendo tipos de acuerdo a los mensajes que entiende cada uno, y a qué otros objetos pueden usarlos (como `roque` puede usar a cualquier objeto que pueda entrenar).

Pensar qué tipos tiene un objeto puede ser muy útil a la hora de programar, para entender qué métodos tengo que ponerle a un objeto, o si puedo o no usar un objeto en un determinado lugar (p.ej. pasárselo como pupilo a `roque`).

