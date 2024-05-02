# Zadanie

Úplná, neúplná a vnorená podmienka, vývojový diagram a zápis podmienok v Jave, príklad použitia ternárneho operátora, príkaz switch, význam hodnoty default vo switchi.

# Vypracovanie

## Úplná, neúplná a vnorená podmienka:
- **Úplná podmienka**: Je to podmienka, ktorá má definované spracovanie pre všetky možné vstupy. Teda obsahuje vetvy pre všetky prípady.
- **Neúplná podmienka**: Je to podmienka, ktorá nemá definované spracovanie pre všetky možné vstupy. Môže chýbať vetva pre niektoré prípady.
- **Vnorená podmienka**: Je to podmienka, ktorá je vnorená v inú podmienku. Teda sa vyhodnocuje len v prípade, že je splnená predchádzajúca podmienka.

## Vývojový diagram a zápis podmienok v Jave:
Vývojový diagram môže reprezentovať logické vetvenie programu pomocou symbolov ako sú rôzne tvary blokov, šípky a textové označenia (referuj na [tému 1](https://github.com/flowernal/maturita/tree/main/PRO/01#prvky-v%C3%BDvojov%C3%BDch-diagramov)). V Jave sa podmienky zapisujú pomocou klávesových slov ako `if`, `else if` a `else`.

## Príklad použitia ternárneho operátora:
Ternárny operátor v Jave má tvar `podmienka ? vyraz1 : vyraz2`. Jeho použitie je často zredukované, napríklad:
```java
int x = (a > b) ? a : b;
```
V tomto prípade sa premenná `x` nastaví na hodnotu `a`, ak je podmienka `(a > b)` pravdivá, inak sa nastaví na hodnotu `b`.

## Príkaz switch:
`switch` je kontrolná štruktúra v Jave, ktorá umožňuje vykonávať rôzne časti kódu na základe hodnoty jednej premennej alebo výrazu. Napríklad:
```java
switch (den) {
    case 1:
        System.out.println("Pondelok");
        break;
    case 2:
        System.out.println("Utorok");
        break;
    default:
        System.out.println("Neplatný deň");
        break;
}
```

## Význam hodnoty default vo switchi:
Hodnota `default` vo switchi definuje blok kódu, ktorý sa vykoná, ak žiadna z hodnôt nezodpovedá hodnote vyjadrenej vo výraze switchu. Je to ako "posledná možnosť" alebo "inak" vetva, ktorá sa vykoná, ak žiadna iná vetva nie je splnená.
