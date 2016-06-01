Breyta ***(variable)*** er nafn sem vísar í tiltekið gildi. Breytur eru skilgreindar með `var` og fylgt eftir með nafni breytunnar.

Hér er dæmi: 

```js 
var example;
```

Ofangreind breyta er **skilgreind** ***(defined)*** en vísar ekki enn í tiltekið gildi ***(not declared)***.

Hér er dæmi skilgreinda breytu sem vísar í tiltekið gildi: 

```js
var example = 'some string';
```

# Athugið

Breyta er **skilgreind** ***(declared)*** með því að nota `var` en notar samasemmerkið til að gefa breytunni gildi ***(define)*** sem hún vísar síðan í. Almennt er talað um að "gefa breytu gildi".

## Verkefni: 

Búðu til skrá sem heitir `variables.js`.

Í þeirri skrá skaltu skilgreina breytu sem heitir `example`. 

**Gefðu breytunni `example` gildið `'some string'`.**

Notaðu síðan `console.log()` til þess að prenta `example` breytuna í stjórnborð ***(console)***. 

Til þess að sjá hvort forritið er rétt geturðu keyrt þessa skipun: 

`javascripting verify variables.js`