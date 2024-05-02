# Zadanie

Dátový typ pole, deklarácia jednorozmerného a viacrozmerného poľa, indexovanie prvkov poľa, dynamické polia.

# Vypracovanie

## Pole

- spája niekoľko položiek rovnakého dátového typu,
- je štruktúrovaný dátový typ, pretože je ďalej deliteľný na jednotlivé položky.

## Prvok poľa

- Jednotlivá položka poľa,
- všetky prvky poľa majú to isté meno,
- jednotlivé prvky rozlišujeme poradovým číslom – indexom.

## Deklarácia poľa

**Jednorozmerné pole**

```cpp
int a[3]; // dátový typ, identifikátor, [počet prvkov];
```

**Dvojrozmerné pole**

```cpp
int b[2][3]; // dátový typ, identifikátor, [počet riadkov][počet stĺpcov];
```

## Indexovanie

- Index je pozícia prvku v poli.
- Prvý prvok poľa má vždy index 0, posledný prvok má index rovný počtu prvkov -1.

```cpp
int a [3]; // má prvky a[0], a[1], a[2]
```

### Uloženie v pamäti

- Na najnižšiu adresu sa ukladá prvok indexom 0. Na vyššie adresy sa ukladajú postupne prvky s vyššími indexami.
- U dvojrozmerných polí sa najskôr ukladajú prvky 1. riadku, potom prvky 2. riadku, atď.

## Inicializácia prvkov poľa

2 spôsoby:

1. priradením hodnoty do každého prvku – `a[0]=1, a[1]=8, a[2]=4`
2. spojením deklarácie s inicializáciou - hodnoty jednotlivých prvkov zapisujeme do zložených zátvoriek – `int a[3] = {1,8,4}`

- Ak realizujeme iba samotnú deklaráciu poľa, musíme uviesť počet jeho prvkov.
- Ak spojíme deklaráciu s inicializáciou, môžeme vynechať počet prvkov poľa, prekladač ich určí sám. V prípade dvojrozmerných polí je potrebné uviesť počet stĺpcov, počet riadkov dopočíta prekladač.

## Dynamické polia

```cpp
int velkost;
cin >> velkost;

int *pole = new int[velkost];

delete [] pole;
```

- Rozmer poľa je zadaný užívateľom a uložený do premennej `velkost`.
- `new int[velkost]` dynamicky alokuje v „heape“ pole celých čísel s veľkosťou `velkost`.
- Operátor `new` sa používa na dynamické prideľovanie pamäte v jazyku C++. To znamená, že pamäť pre pole sa alokuje počas behu (keď program beží), a nie v čase kompilácie.
- Operátor `delete []` de-alokuje pamäť, ktorá bola predtým alokovaná pre pole. Pri de-alokácii dynamicky alokovaných polí je dôležité používať operátor `delete []` (s hranatými zátvorkami). Tento riadok uvoľní pamäť, ktorá bola alokovaná pre premennú poľa, čím sa zabráni úniku pamäte.
