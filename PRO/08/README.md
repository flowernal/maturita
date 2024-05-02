# Zadanie

Princíp vnorených podmienok, logické operátory, tvorba podmienok pomocou logických operátorov.
Príklad: vytvorte podmienky pre nasledovné výrazy:

- výraz je pravdivý, ak v premennej je uložená jedna z hodnôt 1, 3 alebo 10
- výraz je pravdivý, ak má premenná hodnotu v rozsahu 3 až 10

# Vypracovanie

## Vnorené podmienky

Vo vnútri príkazu if sa môže objaviť ďalší if, nazvaný vnorená podmienka. Pomocou vnorených podmienok sa dá zistiť, či 2 podmienky platia súčasne, prípadne či platí aspoň jedna z nich.

**Súčasná platnosť podmienok** (voliť môže len človek, ktorý má 18 a viac a zároveň je občanom republiky)

```cpp
if (vek >= 18)
	if (obcan == 'A')
		cout << "Volit mozete.\n";
	else
		cout << "Volit nemozete.\n";
else
	cout << "Volit nemozete.\n";
```

**Platnosť aspoň jednej z podmienok** (vstup zdarma má človek buď s vekom pod 12, alebo nad 65)

```cpp
if (vek > 12)
	if (vek > 65)
		cout << "Mate vstup zdarma.\n";
	else
		cout << "Musite zaplatit.\n";
else
	cout << "Mate vstup zdarma.\n";
```

## Logické operátory

Umožňujú spojiť niekoľko podmienok do jednej. Príkaz switch sa dá pri vyhodnocovaní booleovských výrazov použiť ako náhrada príkazu if. V praxi sa nevyužíva.

| Operátor | Názov     | Popis                                                  |
| -------- | --------- | ------------------------------------------------------ |
| &&       | A súčasne | Výraz je pravdivý, ak sú pravdivé všetky podmienky     |
| \|\|     | Alebo     | Výraz je pravdivý, ak je splnená aspoň jedna podmienka |
| !        | negácia   | Obráti pravdivostnú hodnotu výrazu                     |

### Operátor && - logický súčin (AND)

_if (vek >= 18 && obcan)_

| Prvý operand | Druhý operand | Súčin |
| ------------ | ------------- | ----- |
| true         | true          | true  |
| true         | false         | false |
| false        | true          | false |
| false        | false         | false |

### Operátor || - logický súčet (OR)

_if (vek< 12 || vek>65)_

| Prvý operand | Druhý operand | Súčin |
| ------------ | ------------- | ----- |
| true         | true          | true  |
| true         | false         | true  |
| false        | true          | true  |
| false        | false         | false |

### Operátor ! – negácia (NOT)

_if (!((vek> 12) &&(vek < 65)))_

| Operand | Negácia |
| ------- | ------- |
| true    | false   |
| false   | true    |

### Priorita operátorov

| Priorita | Operátor        |
| -------- | --------------- |
| 1        | !               |
| 2        | > >= < <= == != |
| 3        | &&              |
| 4        | \|\|            |

# Príklad

Príklad: vytvorte podmienky pre nasledovné výrazy:

- výraz je pravdivý, ak v premennej je uložená jedna z hodnôt 1, 3 alebo 10
- výraz je pravdivý, ak má premenná hodnotu v rozsahu 3 až 10

```cpp
#include <iostream>
using namespace std;

int main() {
	int a = 10;

	if (a == 1 || a == 3 || a == 10) {
		cout << "Pravda" << endl;
	} else {
		cout << "Nepravda" << endl;
	}

	if (a >= 3 && a <= 10) {
		cout << "Pravda" << endl;
	} else {
		cout << "Nepravda" << endl;
	}

	return 0;
}
```
