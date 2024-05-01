# Zadanie

Pojem premenná, deklarácia premennej a čo všetko na jej základe vykoná prekladač, pravidlá pre tvorbu názvu premennej, možnosti vkladania údajov do premennej, oblasť platnosti premennej – globálna a lokálna premenná.

# Vypracovanie

## Premenné

V programovaní je premenná pomenované pamäťové miesto v pamäti, ktoré sa používa na uchovávanie údajov, ktoré sa môžu meniť počas vykonávania programu. V jazyku C++ majú premenné špecifický typ, ktorý určuje veľkosť a rozloženie pamäte premennej, ako aj rozsah hodnôt, ktoré môžu byť v tejto pamäti uložené.

### Deklarovanie premenných

Slúži na vymedzenie miesta v pamäti a pridelenie mena premennej. Prekladač si zároveň uchová aký je rozsah hodnôt danej premennej a aké sú povolené operácie.

_[dátový typ] [meno premennej];_

```cpp
int pocetBodov;
int x , y, z, vyska; // viacej premenných rovnakého typu
float vaha;
```

### Inicializácia premennej

Nastavenie hodnoty premennej súčasne s jej deklaráciou
_[dátový typ] [meno premennej] = [východzia hodnota];_

```cpp
int pocet=10,x,y,koniec=0; // deklarácia spojená s inicializáciou
```

### Pomenovanie premennej

- Názov premennej musí začínať písmenom abecedy (A – Z, a - z), môže obsahovať aj číslice
- Názov premennej nesmie obsahovať medzery ani iné tzv. „biele“ znaky, interpunkciu; špeciálne znaky (napr. +,-,\*,/,#, atd.). Jedinou výnimkou je podtržítko.
- Názov premennej sa musí vyhýbať vyhradeným slovám jazyka samotného, napr. main alebo int
- Premenná sa nesmie volať rovnako ako už skôr deklarovaná premenná.
- Prekladač rozlišuje veľkosť písmen (case sensitive)

```cpp
int 7cisiel; // chyba
int vaha tela; // chyba
int vaha_tela // správne
char Jano, jAno,jaNo,janO; // správne
```

### Operátor adresy

Pri deklarácii premennej dôjde k vymedzeniu miesta v pamäti. Adresu tejto rezervovanej oblasti dostaneme operátorom adresy (&). Jeho zápis vyzerá nasledovne: _&[názov premennej]_.

### Priraďovanie hodnôt

- Hodnota sa do premennej ukladá operátorom priradenia (=)
- Hodnotu je možné do premennej uložiť aj objektom cin, ktorý uloží obdržanú hodnotu zo vstupu.

### Rozsah premenných

Rozsah premennej určuje, kde v programe je možné k nej pristupovať. V jazyku C++ môžu mať premenné:

- Lokálny rozsah: Premenné deklarované v rámci bloku({}) sú lokálne pre tento blok. Premenná je prístupná aj v blokoch vyššej úrovne, ktoré sú súčasťou bloku, kde bola deklarovaná.
- Globálny rozsah: Premenné deklarované mimo akejkoľvek funkcie alebo bloku majú globálny rozsah a sú prístupné v celom programe.
