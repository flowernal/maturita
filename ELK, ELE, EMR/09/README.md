# Zadanie

Tranzistorové zosilňovače, ich rozdelenie, parametre zosilňovačov a požiadavky na zosilňovače, rozbor zapojenia jednostupňového tranzistorového zosilňovača.

# Vypracovanie

## Zosilňovače

- Používajú sa na zosilňovanie signálov
- je aktívny nelineárny štvorpól tvorený zosilňovacím prvkom, pomocnými obvodmi na nastavenie a stabilizáciu polohy pracovného bodu a záťažou

## Rozdelenie

- Podľa použitia

  1. Napäťové (U)
  2. Prúdové (I)
  3. Výkonové (P)
   
- Podľa šírky prenášaného pásma
  
  1. Širokopásmové - rádio, TV
  2. Úzkopásmové - selektívne

- Podľa frekvencie zosilňovaného signálu

  1. Nízkofrekvenčné - do 20 kHz (audio)
  2. Vysokofrekvenčné - väčšie ako 20 kHz
  3. Jednosmerné - do 10 Hz

- Podľa počtu stupňov

  1. Jednostupňové
  2. Viacstupňové

- Podľa spôsobu väzby medzi stupňami

  1. Priama väzba - elektródy sú medzi sebou priamo (galvanicky) spojené, najmä v jednosmerných zosilňovačoch
  2. Kapacitná väzba (kondenzátorová) - prevažne v nízkofrekvenčných
  3. Indukčná (transformátorová) - stupne (elektródy) sú galvanicky oddelené, výkonové zosilňovače

- **Triedy zosilňovačov**

  1. Trieda A - pracovný bod v strede zaťažovacej priamky, výstupný prúd preteká počas celej periódy, teda uhol otvorenia je 360° ($2\pi$), účinnosť: 50%, veľmi malé skreslenie, NF zosilňovače
  2. Trieda B - pracovný bod $I_B=0$, prúd tečie len počas kladných polperiód, uhol otvorenia je 180°, účinnosť: 70-75%, skreslenie veľké (len jedna polperióda) dá sa odstrániť dvojicou tranzistorov, VF zosilňovače
  3. Trieda C - pracovný bod za oblasťou zániku C prúdu, uhol otvorenia je <180°, účinnosť: 90%, skreslenie veľké, nedá sa odstrániť, použitie tam, kde nevadí skreslenie, nikdy NF

## Parametre
1. napäťové zosilnenie
2. prúdové zosilnenie
3. výkonové zosilnenie
4. amplitúdová charakteristika
5. vstupný odpor
6. výstupný odpor
7. výstupný výkon
8. účinnosť
9. šírka pásma
10. citlivosť