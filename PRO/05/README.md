# Zadanie

Základné funkcie pre vstup a výstup dát, rozdiel medzi výrazom a literálom, matematické operátory podľa počtu operandov a typu operácie, priorita a asociativita jednotlivých operátorov.

# Vypracovanie

**Výraz** - kus kódu, ktorý má určitú hodnotu, napr. 4+4, sizeof(int), ...

**Literál** - znamená, že sa má brať bez ďalšieho vyhodnocovania. Dáva sa do úvodzoviek. “Karol“

## Objekt cout (console output)

- Slúži na výpis informácií na štandardný výstup, väčšinou obrazovku počítača
- Je definovaný štandardným knižničným súborom iostream
- Používa sa s operátorom << (insertor)
- Spôsob zápisu:

```cpp
cout << vyraz;
cout << "literál";
```

- Môžeme vypísať aj viacej výrazov alebo literálov za jedným objektom cout:

```cpp
cout  << "Velkost typu int je " << sizeof(int) << "\n";
```

### Bežne používané špeciálne znaky

- \a pri výpise pípne
- \n koniec riadku
- \t tabulátor
- \\\ spätné lomítko
- \’ apostrof
- \“ úvodzovky

## Objekt cin (console input)

- Slúži na načítavanie informácií zo štandardného vstupu, väčšinou z klávesnice
- Je definovaný štandardným knižničným súborom iostream
- Používa sa s operátorom >> (extraktor)
- Spôsob zápisu:
  _cin >> [meno premennej];_
- Môžeme načítať aj viac premenných odrazu, užívateľ musí zadávané hodnoty oddeliť aspoň jednou medzerou
- Zadávanie hodnôt musíme ukončiť klávesou Enter

## Matematické operátory

Operátor je symbol, ktorý zastupuje určitú akciu. Podľa počtu operandov s ktorými operátor pracuje, operátory delíme na binárne a unárne.

### Binárne aritmetické operátory

| Operátor | Zápis  | Význam                    | Dátový typ |
| -------- | ------ | ------------------------- | ---------- |
| +        | x + y  | Súčet                     | int, float |
| -        | x - y  | Rozdiel                   | int, float |
| \*       | x \* y | Súčin                     | int, float |
| /        | x / y  | Podiel                    | int, float |
| %        | x % y  | Zvyšok po delení (modulo) | int        |

- Pracujú s dvomi operandami
- Pracujú s kladnými aj zápornými číslami a okrem modula aj s číslami celými a desatinnými
- Môže dôjsť k pretečeniu alebo podtečeniu
- Operátory delenia / a % nefungujú pre delenie nulou
- Operátor delenia / pre celé čísla robí celočíselný podiel: 9 / 4 = 2
- Modulo vracia zvyšok po celočíselnom delení: 9 % 4 = 1
- Existuje skrátená forma zápisu - a = a + 2 = a += 2 ...
- Operátor sčitovania funguje okrem čísiel aj na reťazcoch

### Unárne aritmetické operátory

| Operátor | Zápis | Význam                                                                       | Dátový typ |
| -------- | ----- | ---------------------------------------------------------------------------- | ---------- |
| +        | +x    | Kladné znamienko (identita)                                                  | int, float |
| -        | -x    | Záporné znamienko (negácia)                                                  | int, float |
| ++       | x++   | Postinkrement (zvýši hodnotu počasťovanej premennej po vyhodnotení výrazu)   | int, float |
| ++       | ++x   | Preinkrement (zvýši hodnotu počasťovanej premennej pred vyhodnotením výrazu) | int, float |
| --       | x--   | Postdekrement (zníži hodnotu počasťovanej premennej po vyhodnotení výrazu)   | int, float |
| --       | --x   | Predekrement (zníži hodnotu počasťovanej premennej pred vyhodnotením výrazu) | int, float |

- Pracujú s jedným operandom
- Pracujú s kladnými aj zápornými číslami a s číslami celými aj desatinnými
- Operátory + a - označujú znamienko čísla, unárne „-“ (mínus) slúži pre zmenu znamienka (odpovedá násobeniu -1)
- Operátory ++ a --sa označujú ako inkrement (zvýšenie o 1) a dekrement (zníženie o 1) a zapisujú sa pred premennou a lebo za premennou
- Ak je zapísaný pred premennou, má význam preinkrementu (++) resp. predekrementu (--). Predpona pre znamená „pred“. Hodnota premennej je najskôr zvýšená resp. znížená a ako taká vstupuje do výrazu.
- Ak je zapísaný za premennou, má význam postinkrementu (++) resp. postdekrementu (--). Predpona post znamená „po“. V rámci výrazu sa uvažuje pôvodná hodnota premennej, ku zvýšeniu resp. zníženiu dochádza až po určení hodnoty výrazu.

### Priorita a asociativita operátorov

- Priorita určuje poradie spracovania operandov pri použití rôznych operátorov. Zmeny priority docielime pomocou zátvoriek ( ).
- Asociativita určuje poradie (smer) vyhodnocovania operátorov s rovnakou prioritou.

| Operátory                               | Priorita | Asociativita |
| --------------------------------------- | -------- | ------------ |
| ()                                      | 1        | ->           |
| ++, --, +, -, (unárne), (typ), sizeof() | 2        | <-           |
| \*, /, %                                | 3        | ->           |
| Binárne +, -                            | 4        | ->           |
| =                                       | 5        | <-           |

_(typ) = typová konverzia_