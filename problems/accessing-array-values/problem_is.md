Array þættir er hægt að nálgast í gegnum index númer.

Index númer byrjar frá núlli til lengdar arraysins mínus einn.

Hér er dæmi:


```js
var pets = ['cat', 'dog', 'rat'];

console.log(pets[0]);
```

Forritakóðinn fyrir ofan mun prenta fyrsta stak `pets` arraysins - strenginn `cat`.

Array stök verður að nálgast með hornklofa tákni.

Punkta ritháttur er ógildur.

Gildir ritháttur:

```js
console.log(pets[0]);
```

Ógildur ritháttur:
```
console.log(pets.1);
```

## Áskorunin:

Búa til skrá sem heitir `accessing-array-values.js`.

Í þeirri skrá, skilgreinið fylkið `food`:
```js
var food = ['apple', 'pizza', 'pear'];
```

Notið `console.log()` til að prenta `annað` gildið í arrayinu í terminal.

Athugaðu hvort forritið sé rétt með því að keyra þessa skipun:

```bash
javascripting verify accessing-array-values.js
```
