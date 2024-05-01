# Zadanie

základné dátové typy v C++, spôsob pretypovania dátového typu premennej, pojem pretečenie a podtečenie

# Vypracovanie

## Základné dátové typy:

- int – celé čísla
- float – rálne čísla
- char – znakové
- bool – logické

### Celočíselné dátové typy

| Dátový typ         | Veľkosť v B | Rozsah                                                 | Rozsah exp.    |
| ------------------ | ----------- | ------------------------------------------------------ | -------------- |
| short              | 2           | -32 768 – 32 767                                       | -2^15 – 2^15-1 |
| unsigned short     | 2           | 0 – 65 535                                             | 0 – 2^16-1     |
| int                | 4           | -2 147 483 648 – 2 147 483 647                         | -2^31 – 2^31-1 |
| unsigned int       | 4           | 0 – 4 294 967 295                                      | 0 – 2^32-1     |
| long               | 4           | -2 147 483 648 – 2 147 483 647                         | -2^31 – 2^31-1 |
| unsigned long      | 4           | 0 – 4 294 967 295                                      | 0 – 2^32-1     |
| long long          | 8           | -9 223 372 036 854 775 808 – 9 223 372 036 854 775 807 | -2^63 – 2^63-1 |
| unsigned long long | 8           | 0 – 18 446 744 073 709 551 615                         | 0 – 2^64-1     |

### Dátové typy pre reálne čísla (s desatinnou čiarkou)

| Dátový typ  | Veľkosť v B | Rozsah                  |
| ----------- | ----------- | ----------------------- |
| float       | 4           | ±1.2E-38 to ±3.4E38     |
| double      | 8           | ±2.2E-308 to ±1.8E308   |
| long double | 16          | ±3.4E-4932 to ±1.2E4932 |

### Textové dátové typy

| Dátový typ | Veľkosť v B        | Rozsah             |
| ---------- | ------------------ | ------------------ |
| char       | 1                  | 1 znak             |
| string     | Podľa počtu znakov | Väčší počet znakov |

### Dátový typ bool (logické)

| Dátový typ | Veľkosť v B | Rozsah                  |
| ---------- | ----------- | ----------------------- |
| bool       | 1           | 2 hodnoty – true, false |

### Zistenie veľkosti dátových typov - pomocou operátora sizeof(názov typu)

#### Charakteristiky celočíselných dátových typov

- Rozsahy jednotlivých číselných typov zistíme pomocou funkcií zo súboru limits.h - SHRT_MIN, SHRT_MAX, USHRT_MAX, INT_MIN, INT_MAX, UINT_MAX...

#### Charakteristiky reálnych dátových typov

- Rozsahy jednotlivých číselných typov zistíme pomocou funkcií zo súboru float.h - FLT_DIG, FLT_MIN, FLT_MAX, DBL_DIG, LDBL_DIG...

## Implicitná a explicitná typová konverzia

Ak v rámci jedného výrazu použijeme premenné rôznych dátových typov dôjde ku prevodom (konverzii) údajov. Prekladač môže vykonať 2 druhy konverzie:

- **Implicitná typová konverzia** (automatická) – vykoná sa automaticky, vždy keď je to nutné
- **Explicitná typová konverzia** – je zadaná programátorom pomocou operátora pretypovania

### Implicitná typová konverzia

dochádza k nej v nasledovných prípadoch:

1. Konverzia samostatných operandov:
   Pred vyhodnotením výrazu sa samostatné operandy prevedú nasledovne:

   - char alebo short -> int,
   - unsigned char alebo unsigned short -> int (ak by došlo k pretečeniu ->unsigned int)
     Prečo ? (lebo máme 4 bytovú aritmetiku a char má 1B a short má 2B )

2. Binárne operácie:
   Ak majú operandy binárnej operácie rôzny typ, konvertuje sa typ operandu s nižšou prioritou na typ s vyššou prioritou. Typy char a short sa najskôr konvertujú na int. Int má najnižšiu prioritu.

   _Int –> unsigned int –> long –> unsigned long –> long long –> unsigned long long –> float –> double –> long double_

3. Prevod vynútený priradením:
   V priraďovacích príkazoch je typ na pravej strane konvertovaný na typ na ľavej strane. Pozor: Môže dôjsť ku strate informácie (pri jej orezaní na menší počet bytov).

### Explicitná typová konverzia

- Existujú situácie, kedy do typovej konverzie musí zasiahnuť programátor.
- Def.: _(dátový typ) výraz ==> (long)cislo_

**Pretečenie** je jav, ku ktorému dochádza, ak premennej priradíte hodnotu, ktorá je na jej rozsah príliš veľká. Výstup programu(short): -32768 = dôjde k pretečeniu a hodnota premennej sa pretočí na najnižšiu možnú hodnotu jej typu

**Podtečenie** je jav, ku ktorému dochádza, ak premennej priradíte hodnotu, ktorá je na jej rozsah príliš malá. Výstup programu(short): 32767 = dôjde k podtečeniu a hodnota premennej sa pretočí na najvyššiu možnú hodnotu jej typu
