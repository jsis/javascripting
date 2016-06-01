Það eru margar leiðir til að hagræða fylki.

Ein algeng leið er sía fylki í að aðeins innihalda ákveðin gildi.

Fyrir þetta getum við notað `.filter()` aðferðina.

Hér er dæmi:

```js
var pets = ['cat', 'dog', 'elephant'];

var filtered = pets.filter(function (pet) {
  return (pet !== 'elephant');
});
```

Breytan `filtered` inniheldur núna bara  `cat` og` dog`.

## Áskorunin:

Búa til skrá sem heitir `array-filtering.js`.

Í þeirri skrá, skilgreina breytu sem heitir `numbers` og inniheldur eftifarandi:

```js
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```

Eins og að ofan, skilgreindu breytu sem heitir `filtered` og vísar í niðurstöðu `numbers.filter()`.

Fallið sem þú sendir inní `.filter()` aðferðina mun líta eitthvernveginn svona út.

```js
function evenNumbers (number) {
  return number % 2 === 0;
}
```

Notið `console.log()` til að prenta `filtered` fylkið í terminal.

Athugaðu að sjá hvort forritið sé rétt með því að keyra þessa skipun:

```bash
javascripting verify array-filtering.js
```
