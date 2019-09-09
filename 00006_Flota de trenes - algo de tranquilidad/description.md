Somos insistentes ... seguimos con la flota de trenes:

```wollok
object flotaFerroviaria {
  const trenes = [chucu1, chucu2, chucu3, chucu4]
  
  method tranquilidadTotal() { 
    return trenes.all({ tren => tren.vaTranca() })
  }
  method trenTranca() { 
    return trenes.find({ tren => tren.vaTranca() })
  }
  method cuantosTrancas() { 
    return trenes.count({ tren => tren.vaTranca() })
  }
  method hayAlgoDeTranquilidad() { 
    return trenes.any({ tren => tren.vaTranca() })
  }
  method trenesQueVanTranca() {
    return trenes.filter({ tren => tren.vaTranca() })
  }
}
```

> Toca indicar el **tipo** del objeto que devuelve `flotaFerroviaria.hayAlgoDeTranquilidad()`.
