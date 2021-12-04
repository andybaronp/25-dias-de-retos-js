# Contando ovejas para dormir 🐑😴💤

Considera una lista/array de ovejas. Cada oveja tiene un nombre y un color. Haz una función que devuelva una lista con todas las ovejas que sean de color `rojo` **y que además** su nombre contenga tanto las letras `n` Y `a`, sin importar el orden, las mayúsculas o espacios.

Por ejemplo, si tenemos las ovejas:

```javascript
const ovejas = [
  { name: "Noa", color: "azul" },
  { name: "Euge", color: "rojo" },
  { name: "Navidad", color: "rojo" },
  { name: "Ki Na Ma", color: "rojo" },
];
```

Al ejecutar el método debería devolver lo siguiente:

```javascript
const ovejasFiltradas = contarOvejas(ovejas);

console.log(ovejasFiltradas);

// [{ name: 'Navidad', color: 'rojo' },
//  { name: 'Ki Na Ma', color: 'rojo' }]
```

## Solución propuesta

```javascript
function contarOvejas(ovejas) {

 const ovejasRojo = ovejas.
  .filter(oveja => oveja.color === "rojo")
  .filter(oveja => oveja.name.match(/(a)/i))
  .filter(oveja => oveja.name.match(/(n)/i))

  return ovejasRojo
}

```

- Se declara una variable **ovejasRojo** que contiene las ovejas que cumplen con los requisitos y retornarlo sin modificar el array original.
- Filtrar el array de ovejas por color rojo.
- Filtrar el array de ovejas por nombre que contenga las letras **n** y **a**.

## Resultado

![ resultado](https://imgur.com/gMHsoNr.png)

---

Eso es todo, ¡Muchas gracias! 😎
