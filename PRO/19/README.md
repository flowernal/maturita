# Zadanie

Pojem premenná, pravidlá pre tvorbu názvu premennej, prečo nemôžeme ako názov premennej použiť tzv. kľúčové slovo, základné dátové typy, príklad deklarácie a inicializácie premennej, v akých číselných sústavách môžu byť zapísané celočíselné konštanty, pojem literál.

# Vypracovanie

## Pojem premenná:
Premenná v Jave je označenie pre umiestnenie v pamäti, do ktorého sa môže ukladať hodnota. Táto hodnota môže byť menená a používaná v programe.

## Pravidlá pre tvorbu názvu premennej:
- Názov premennej musí začínať písmenom, podčiarkovaním (_) alebo znakom dolár ($) - neodporúča sa však používať znak dolára.
- Názov môže obsahovať písmená, číslice a znak podčiarknutia.
- Veľkosť písmen sa rozlišuje (Java je case-sensitive), teda premenné "premenna" a "Premenna" sú rôzne.
- Názov premennej by mal byť výstižný a opisný, aby sa ľahšie rozumelo jej účelu.

## Prečo nemôžeme ako názov premennej použiť tzv. kľúčové slovo:
Kľúčové slová v Jave sú vyhradené pre určité účely a operácie v jazyku. Používanie kľúčových slov ako názvov premenných by spôsobilo zmätenie interpretátoru, pretože by nevedel, či ide o operáciu alebo názov premennej.

## Základné dátové typy:
V Jave existuje niekoľko základných dátových typov, ktoré určujú typ hodnoty, ktorú môže premenná uchovávať. Medzi ne patria:
- `int`: celé čísla
- `double`: desatinné čísla s plávajúcou desatinnou čiarkou
- `boolean`: logické hodnoty `true` alebo `false`
- `char`: znaky Unicode
- `String`: reťazce znakov

## Príklad deklarácie a inicializácie premennej:
```java
int pocetJablk = 10; // Deklarácia a inicializácia premennej 'pocetJablk' s hodnotou 10
```

## V akých číselných sústavách môžu byť zapísané celočíselné konštanty:
V Jave môžu byť celočíselné konštanty zápisné v nasledujúcich číselných sústavách:
- Desiatkovej (základ 10)
- Dvojkovej (binárnej, základ 2)
- Osmičkovej (oktálnej, základ 8)
- Šestnástkovej (hexadecimálnej, základ 16)

## Pojem literál:
Literál v Jave je konkrétna hodnota, ktorá je priamo zapísaná v zdrojovom kóde. Môže to byť číslo, reťazec, znak alebo iná hodnota. Napríklad:
- Celé číslo: `10`
- Desatinné číslo: `3.14`
- Znak: `'A'`
- Reťazec: `"Hello, world!"`
