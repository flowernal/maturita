# Zadanie

Pojem cyklus, typy cyklov a ich použitie, vývojový diagram a zápis cyklov v Jave.
Príklad: Napíšte blok programu v ktorom vypočítate súčet prvých 10 čísel postupnosti danej vzorcom pre n-tý člen:   
$a_n = \frac{{2n - 3}}{{n + 1}}, \quad n \in \mathbb{N}$

Na záver vypíšte hodnotu súčtu.

# Vypracovanie

## Pojem cyklus:
Cyklus v programovaní je konštrukcia, ktorá opakovane vykonáva určitý blok kódu, kým je splnená určitá podmienka.

## Typy cyklov a ich použitie:
V Jave existujú dva hlavné typy cyklov:
- **for cyklus**: Používa sa, keď počet iterácií je známy vopred.
- **while cyklus**: Používa sa, keď počet iterácií nie je známy vopred a závisí od podmienky.

## Vývojový diagram a zápis cyklov v Jave:
Vývojový diagram môže reprezentovať cykly pomocou symbolov ako sú šípky a textové označenia. V Jave sa cykly zapisujú pomocou klávesových slov ako `for` a `while`.

## Príklad:
Napíšte blok programu v ktorom vypočítate súčet prvých 10 čísel postupnosti danej vzorcom pre n-tý člen:   
$a_n = \frac{{2n - 3}}{{n + 1}}, \quad n \in \mathbb{N}$

Na záver vypíšte hodnotu súčtu.

```java
public class Main {
    public static void main(String[] args) {
        double sucet = 0;

        for (int n = 1; n <= 10; n++) {
            double clen = (2 * n - 3) / (double)(n + 1); // Vypočítanie hodnoty n-tého člena
            sucet += clen; // Pridanie hodnoty člena do súčtu
        }

        System.out.println("Súčet prvých 10 čísel postupnosti: " + sucet);
    }
}
```
V tomto programe sa používa for cyklus na vypočítanie súčtu prvých 10 čísel postupnosti danej vzorcom.
