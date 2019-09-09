El siguiente objeto es un modelo muuuuy parcial de una agencia de turismo. 

```wollok
object agencia {
  var destinos = [encarnacion, salvadorDeBahia, potosi]
  
  method destinosSoleados() { 
    return destinos.filter({ destino => destino.haySol() })
  }
  
  method unDestinoSoleado() {
    return destinos.find({ destino => destino.haySol() })
  }
  
  method tieneDestinosCopados() {
    return destinos.any({ destino => destino.haySol() and destino.cantidadMuseos() > 10 })
  }
  
  method muchoSol() { 
    return destinos.count({destino => destino.haySol()}) > 1
  }
  
  method totalMuseos() {
    return destinos.sum({destino => destino.cantidadMuseos()})
  }
}
```

Cada destino es un objeto al que se le puede preguntar `haySol()` y `cantidadMuseos()`, como las ciudades del ejercicio "Ema en ciudades" de la guía de objetos y mensajes.

A partir de esta definición, se arman varias expresiones, que se podrían p.ej. evaluar en un REPL. Algunas son correctas, otras dan error al evaluarlas.

> ¿Cuáles de las expresiones son correctas, o sea, se pueden evaluar sin que dé error?