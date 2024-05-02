# Zadanie

Ukazovateľ a jeho využitie, deklarácia ukazovateľa a priradenie adresy premennej do ukazovateľa, dereferenčný operátor, aritmetika s ukazovateľmi a jej využitie pri práci s poľom.

# Vypracovanie

## Ukazovateľ

- Ukazovateľ (pointer) je premenná, ktorá ukazuje na inú premennú alebo konštantu. Ak ukazovateľ ukazuje na nejakú premennú, jeho hodnotou je adresa tejto premennej v pamäti.
- Ukazovateľ teda obsahuje adresu v pamäti počítača – a až na tejto adrese sa nachádza hodnota, na ktorú sme boli doteraz zvyknutí. Táto adresa je vždy celé číslo, ktoré zapisujeme v hexadecimálnom tvare (napr. 0x7fff513dab00).
- Príklad ukazovateľov: ikona na pracovnej ploche PC

### Deklarácia ukazovateľov

- Ako ktorákoľvek iná premenná, aj ukazovateľ sa musí deklarovať. Dátový typ ukazovateľa popisuje dátový typ premennej, ktorej adresu môže ukazovateľ obsahovať. Pre deklaráciu ukazovateľa sa požíva symbol \* .
- Pr. `int *ukazovatel;`

### Hodnota vs. adresa

- Hodnotou ukazovateľa na int môže byť iba adresa premennej typu int, hodnotou ukazovateľa na float môže byť iba adresa premennej typu float, atď. Jediný rozdiel medzi ukazovateľmi rôzneho typu je dátový typ premennej, na ktorú ukazujú. (Ukazovateľ je vždy zviazaný s nejakým typom).

## Ukazovateľ ako premenná a referenčný (adresovací) operátor „&“

- Keďže je ukazovateľ premenná, môžeme do neho priradiť hodnotu – tj. nejakú adresu. Najčastejšie s ukazovateľom pracujeme tak, že ako jeho hodnotu použijeme adresu niektorej premennej, ktorú máme zadeklarovanú. Pre tento účel použijeme tzv. referenčný operátor (adresovací) `&`, ktorý po aplikovaní na premennú vráti jej adresu.
- `int premenna = 17;` deklarácia a inicializácia premennej
- `int *ukazovatel;` deklarácia ukazovateľa na typ int
- `ukazovatel = &premenna;` získanie adresy, priradenie do premennej

### Veľkosť ukazovateľa

- Všetky ukazovatele majú rovnakú veľkosť, ktorá nezávisí na ich type, ale na type prekladača a operačného systému. Pre 64 bitové prekladače ukazovateľ má veľkosť 8 bajtov.

## Dereferenčný operátor „\*“

- Vieme získať adresu premennej a uložiť ju do ukazovateľa. Ukazovatele sa predovšetkým používajú pre čítanie a zmenu hodnôt uložených v premenných, na ktoré ukazuje.
- Na tento účel sa používa tzv. dereferenčný operátor `*`, ktorým sa sprístupní premenná na adrese, kam ukazovateľ ukazuje.
- `int premenna = 17;` deklarácia a inicializácia premennej
- `int *ukazovatel;` dekláracia ukazovateľa na typ `int`
- `ukazovatel = &premenna;` získanie adresy a jej priradenie
- `*ukazovatel = 19;` na adresu v premennej `ukazovatel` dá hodnotu 19

## Aritmetika s ukazovateľmi

- V tabuľke sú príklady použitia aritmetických a relačných (porovnávacích) operátorov medzi ukazovateľmi a celými číslami. Sú použité ukazovatele `p, p1, p2` vždy rovnakého typu (je jedno, aký je to typ, ale musí byť pre všetky ukazovatele rovnaký) a `x` je celé číslo.

| Operácia | Typ výsledku  | Význam                                                  |
| -------- | ------------- | ------------------------------------------------------- |
| p+x      | rovnaký ako p | Vypočíta novú adresu zvýšenú o x položiek               |
| p-x      | rovnaký ako p | Vypočíta novú adresu zníženú o x položiek               |
| p++      | rovnaký ako p | Zvýši ukazovateľ o 1, ukazuje na nasledujúcu položku    |
| p--      | rovnaký ako p | Zníži ukazovateľ o 1, ukazuje na predchádzajúcu položku |
| p1-p2    | int           | Relatívna vzdialenosť p1 od p2 v položkách              |
| p1==p2   | bool          | Ukazujú obidva ukazovatele na rovnakú premennú?         |
| p1!=p2   | bool          | Ukazujú obidva ukazovatele na rôznu premennú?           |
| p1>p2    | bool          | Ukazuje p1 na vyššiu adresu ako p2?                     |
| p1>=p2   | bool          | Ukazuje p1 na rovnakú alebo vyššiu adresu ako p2?       |
| p1<p2    | bool          | Ukazuje p1 na nižšiu adresu ako p2?                     |
| p1<=p2   | bool          | Ukazuje p1 na rovnakú alebo nižšiu adresu ako p2?       |

Pomocou aritmetiky dokážeme indexovať v poli pomocou vypočítanej adresy.
