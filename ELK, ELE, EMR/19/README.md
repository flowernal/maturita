# Zadanie

Princíp činnosti LC a RC oscilátorov, oscilátor riadený kryštálom, príklady využitia oscilátorov.

# Vypracovanie

Oscilátory sú druhy generátorov

## Generátory

- Obvody, ktoré vyrábajú periodický signál - určitá časť signálu sa pravidelne opakuje = perióda
- **Rozdelenie**:
  - Podľa časového priebehu výstupného signálu
    - 1. generátory harmonického (sínusového) signálu $u(t) = U_m \sin(\omega t + \phi)$ (**LC, RC oscilátory**)
    - 2. generátory neharmonického (nesínusového) signálu
  - Podľa frekvencie výstupného signálu
    - 1. generátory NF signálu - (RC) - do 100 kHz
    - 2. generátory VF signálu - (LC) - nad 100 kHz
    - 3. generátory VVF signálu - (vedenia s rozloženými parametrami) - desiatky GHz

## LC oscilátory (L - indukcia, C - kapacita)

- Rezonančný obvod tvorí kondenzátor s cievkou
- Používajú sa na výrobu harmonického signálu s $f > 100 kHz$ (pre nižšie $f$ nadobúdajú cievky a kondenzátory veľké hodnoty - veľké rozmery a hmotnosť)
- Rezonančná frekvencia je daná Thomsonovým vzťahom
- Podľa spôsobu realizácie spätnej väzby sa rozdeľujú na:
  - **Oscilátory s indukčnou väzbou** - Meisnerov, Schnellov
  - **Oscilátory trojbodové** - Hartleyov, Colpittsov, Clappov

## RC oscilátory (R - odpor, C - kapacita)

- Výhodnejšie pre výrobu frekvencií do 100 kHz, max 1 MHz
- Spätnoväzbový štvorpól zložený z rezistorov R a kondenzátorov C
- Spätnoväzbový štvorpól určuje frekvenciu oscilácií
- Podľa spôsobu zapojenia spätnoväzobného štvorpólu sa rozdeľujú na:
  - **Oscilátory s kaskádnym radením štvorpólov**
  - **Oscilátory s pásmovými filtrami**

## Oscilátory riadené kryštálom

- Ak privedieme na prívody kryštálu striedavý elektrický signál, spôsobí premenlivé deformácie platničky kryštálového rezonátora
- Pri deformáciách naopak kryštálový rezonátor vytvára na svojich prívodoch premenlivé napätie, ktorým sa udržiavajú elektrické kmity v obvode oscilátora

## Príklady využitia oscilátorov

1. **Elektronické hodiny a časovače:** Oscilátory sú kľúčovou súčasťou elektronických hodín a časovačov na generovanie presných časových signálov.

2. **Rádiové vysielače a prijímače:** V rádiových komunikačných systémoch sa využívajú oscilátory na generovanie nosnej frekvencie a iných signálov.

3. **Mikroprocesory a počítačové systémy:** Oscilátory sú nevyhnutné pre fungovanie mikroprocesorov a počítačov na synchronizáciu časovania a riadenie operácií.

4. **Frekvenčné syntetizátory:** Používajú sa vo frekvenčných syntetizátoroch na generovanie presných frekvencií pre rôzne aplikácie, ako sú rádiové pásmá a komunikačné systémy.
