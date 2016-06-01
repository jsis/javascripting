`Gildissvið` ***(Scope)*** er samansafn af breytum ***(variables)***, hlutum ***(objects)***, og föllum ***(functions)*** sem þú hefur aðgang að. 

Javascript hefur tvö gilissvið: `víðvært` ***(global)*** og `staðvært` ***(local)***. Breyta sem er skilgreind ***(declared)*** utan falls er `víðvær` breyta, og gildi þess er aðgengilegt og breytanlegt í öllu forritinu þínu. Breyta sem er skilgreind inni í falli er `staðvær`. Hún er búin til og henni eytt í hvert skipti sem fall er keyrt og ekki hægt að nálgast hana úr kóða utan fallsins. 

Föll skilgreind inni í öðrum föllum eru þekkt sem földuð föll ***(nested functions)*** og hafa aðgang að gildisviði ytra fallsins ***(parent function's scope)***. 

Skoðaðu vel athugasemdirnar í kóðanum hér fyrir neðan:

```js
var a = 4;  // a er víðvær breyta. Hún er aðgengileg úr föllunum hér fyrir neðan

function foo() {
    var b = a * 3;  // b er ekki hægt að nálgast fyrir utan foo fallið en hægt er að nálgast b úr 
                    // föllum skilgreindum innan foo
    function bar(c) {
    var b = 2;  // Hér er önnur `b` breyta er skilgreind innan gildissviðs bar fallsins
                // Breytingarnar á þessari nýju breytu `b` hafa ekki áhrif á gömlu `b` breytuna
    console.log( a, b, c );
    }

    bar(b * 4);
}

foo(); // 4, 2, 48
```
IIFE, Immediately Invoked Function Expression, er algengt mynstur þegar skapaðar eru staðbundin gildissvið, dæmi:
```js
    (function(){ // Function segðin (expression) er umvafin hornklofum.
        // Breytur sem eru skilgreindar hér
        // er ekki hægt að nálgast utan frá.
    })(); // () gerir að verkum að fallið er keyrt samstundis
```

## Verkefnið: 

Búðu til skrá sem heitir `scope.js`.

Í þeirri skrá skaltu afrita eftirfarandi kóða: 

```js
var a = 1, b = 2, c = 3;

(function firstFunction(){
    var b = 5, c = 6;

    (function secondFunction(){
        var b = 8;

        (function thirdFunction(){
            var a = 7, c = 9;

            (function fourthFunction(){
                var a = 1, c = 8;

            })();
        })();
    })();
})();
```

Notaðu þekkingu þína á breytum `gildissviðsins` og settu eftirfarandi kóða inn í eitt af föllunum í `scope.js` þannig að úttakið verði `a: 1, b: 8, c: 6` 

```js
console.log("a: "+a+", b: "+b+", c: "+c);
```

Athugaðu hvort forritið sé rétt með því að keyra eftirfarandi skipun:

```bash
javascripting verify scope.js
```

