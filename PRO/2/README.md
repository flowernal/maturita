# Zadanie

Základná štruktúra hlavného programu, charakteristika jeho jednotlivých častí, základné procesy prebiehajúce pri preklade súboru typu .cpp, význam a tvorba komentárov.
Príklad: napíšte program, ktorý vypíše na obrazovku nasledovný text:

```
************************************

           SPS Stara Tura

************************************
```

# Vypracovanie

## Zdrojové a hlavičkové súbory

- meno.cpp je zdrojový súbor, v ktorom je uložený náš program. Pre jeho správnu funkciu je väčšinou potrebné doplniť ho vložením ďalších súborov. Najčastejšie vkladáme (include) tzv. hlavičkové (header-ové) súbory s príponou .h .

- meno.h je hlavičkový (header-ový) súbor, ktorý obsahuje potrebné knižničné funkcie. Pr.: #include <stdio.h>

## Funkcia main

- Funkcia je skupina príkazov, ktoré plnia určitú úlohu.

- main je názov hlavnej funkcie

- Každý program v C++ má práve 1 funkciu main, ktorá je vstupnou funkciou programu

- Ak by program nemal funkciu main, počítač by nevedel, kde má začať vykonávať program

- Ak by program mal viac ako 1 funkciu main, počítač by nevedel, ktorú z nich si má vybrať

- Telo funkcie začína { a končí }

### Základný tvar funkcie main:

```cpp
int main () {
  [telo funkcie]
  return 0; // ukončuje program
}
```

**Štandardná knižnica C++ std** - obsahuje rad súborov, z ktorých každý definuje niektoré bežne používané objekty

**#include** - Inštrukcia pre preprocesor, Za #include nasleduje názov knižného súboru v zátvorkách <>

**Menný priestor** - Príkaz using namespace std; hovorí počítaču, že pred každé meno bez menného priestoru si má pridať std::

**Funkcie** – okrem hlavnej funkcie main môže program obsahovať ďalšie, vedľajšie, funkcie, ktoré sú umiestnené buď pred main, alebo za mainom, kedy je potrebné pridať hlavičku funkcie pred main. Tieto funkcie pomáhajú rozdeliť program na viacero menších podprogramov pre jednoduchšie čítanie programu a zároveň dokážu zmenšiť celkovú veľkosť programu pri opakovanom volaní funkcie.

### Preklad zdrojového kódu do binárneho súboru zabezpečujú 3 programy:

- **Preprocessor** – stará sa o predspracovanie zdrojového kódu (napr.: namiesto odkazu na súbor iostream vloží jeho obsah, vynechá komentáre..)
- **Prekladač** – preprocesorom spracovaný zdrojový kód preloží do relatívneho (obektového) kódu počítača. Výsledok uloží do samostatného objektového súboru s príponou .obj (.o), v prípade syntaktickej chyby program nepreloží
- **Linker** – pridá do .obj súboru kódy z knižníc, relatívne adresy nahradí skutočnými adresami. Výsledkom je spustiteľný program (.exe).

### Chyby pri preklade

- Syntaktické (syntax errors) sú gramatické chyby. Vznikajú ak sa nedodržia pravidlá (syntax) pri písaní príkazov (napr. vynechanie bodkočiarky, chybne napísaný príkaz, …)
- Sémantické, rozoznávame 2 typy:
  - run-time errors sú chyby vznikajúce počas behu programu, kedy nastal stav, v ktorom počítač nevie ďalej pokračovať (napr. delenie nulou, otvorenie neexistujúceho súboru)
  - logical-errors sú logické chyby. Sú zapríčinené nesprávnosťou samotného algoritmu (napr. x = a – 1 a správne malo byť x = a + 1)

### Tvorba komentárov

- **Dokumentácia**: Komentáre umožňujú dokumentovať kód. Vysvetľujú, prečo boli urobené určité rozhodnutia, ako fungujú konkrétne časti kódu alebo akékoľvek dôležité skutočnosti, ktoré by budúci vývojári (vrátane vás) mohli potrebovať vedieť. Vďaka dobrým komentárom je kód zrozumiteľnejší a lepšie sa udržiava.

- **Jasnosť a zrozumiteľnosť**: Komentáre môžu objasniť zložité časti kódu. Fungujú ako sprievodca, ktorý pomáha ostatným (a v budúcnosti aj vám) pochopiť účel a funkčnosť rôznych zložiek kódu. Je to užitočné najmä vtedy, keď logika nie je okamžite zrejmá zo samotného kódu.

- V jazyku C++ sa označujú buď // pre jednoriadkový komentár, alebo /_ , _/ pre viacriadkový komentár.

# Príklad

napíšte program, ktorý vypíše na obrazovku nasledovný text:

```
************************************

           SPS Stara Tura

************************************
```

```cpp
#include <iostream>
using namespace std;

int main() {
  cout<<"************************************";
  cout<<"           SPS Stara Tura           ";
  cout<<"************************************";
}
```
