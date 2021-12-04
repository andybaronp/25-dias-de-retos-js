# ¡Ayuda al elfo a listar los regalos!🧝‍♂️

Te ha llegado una carta ✉️ con todos los regalos que debes preparar. El tema es que es una cadena de texto y es muy difícil de leer 😱. ¡Menos mal que han puesto cada regalo separado por espacio! (aunque **ten cuidado**, porque al ser niños, igual han colado más espacios de la cuenta)

Encima nos hemos dado cuenta que algunas palabras vienen con un `_` delante de la palabra, por ejemplo `_playstation`, que significa que **está tachado y no se tiene que contar.**

Transforma el texto a un objeto que contenga el nombre de cada regalo y las veces que aparece. Por ejemplo, si tenemos el texto:

```javascript
const carta = "bici coche balón _playstation bici coche peluche";
```

Al ejecutar el método debería devolver lo siguiente:

```javascript
const regalos = listGifts(carta);

console.log(regalos);
/*
{
  bici: 2,
  coche: 2,
  balón: 1,
  peluche: 1
}
*/
```

Ten en cuenta que los tests pueden ser más exhaustivos... 😝 **¡Cuidado con contar espacios vacíos!**

## Solución propuesta 🤓

```javascript
const res = letter
  .trim()
  .split(" ")
  .filter((e) => !e.includes("_"))
  .reduce((ac, cu) => ((ac[cu] = (ac[cu] || 0) + 1), ac), {});

return res;
```

- Se declara una variable `res` que será el resultado de la función sin modificar el array original.
- Uso el método `trim()` para quitar los espacios en blanco al principio y al final del texto.
- Uso el método `split()` para separar el texto por espacios.
- Uso el método `filter()` para filtrar los elementos que no contengan el caracter `_`.
- Uso el método `reduce()` para recorrer el array y añadir los elementos al objeto `res`.

Resultado:

```javascript

{
bici:2,
coche:2,
balón:1,
peluche:1
}

```
