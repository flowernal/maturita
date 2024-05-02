# Zadanie

Pojem metóda a vymenujte výhody používania metód, rozdiely medzi jednotlivými druhmi metód (funkcia - procedúra), vysvetliť pojem preťaženie metódy na konkrétnom príklade, pojem rekurzívna metóda.

# Vypracovanie

## Pojem metóda:
Metóda v programovaní je blok kódu, ktorý vykonáva určité úlohy. Môže prijímať vstupné hodnoty (parametre) a vracať výstupné hodnoty. Metódy môžu byť súčasťou triedy a používajú sa na organizáciu a znovupoužiteľnosť kódu.

## Výhody používania metód:
- **Modularita**: Kód je rozdelený na menšie časti, čo zjednodušuje čitateľnosť a údržbu.
- **Znovupoužiteľnosť**: Metódy môžu byť volané viackrát z rôznych častí programu.
- **Riadenie komplexity**: Rozdelenie úloh na menšie metódy znižuje zložitosť kódu.
- **Ľahké údržba**: Zmeny v kóde môžu byť vykonané len v jednej metóde a tým sa minimalizuje riziko chýb.

## Rozdiely medzi jednotlivými druhmi metód (funkcia – procedúra):
- **Funkcia**: Vráti hodnotu späť po vykonaní určitej úlohy. Môže prijímať vstupné hodnoty a vracať výstupné hodnoty.
- **Procedúra**: Vykonáva určitú úlohu, ale nevracia hodnotu späť. Môže prijímať vstupné hodnoty, ale nemá návratovú hodnotu.

## Vysvetlenie pojmu preťaženie metódy na konkrétnom príklade:
Preťaženie metódy je možnosť definovať viacero metód s rovnakým názvom, ale s rôznymi parametrami. Napríklad:
```java
public class Kalkulacka {
    public int sucet(int a, int b) {
        return a + b;
    }
    
    public double sucet(double a, double b) {
        return a + b;
    }
}
```
V tomto príklade je metóda `sucet` preťažená, pretože existujú dve verzie tej istej metódy, ale každá prijíma iné typy parametrov.

## Pojem rekurzívna metóda:
Rekurzívna metóda je metóda, ktorá volá sama seba. Tento prístup sa používa na riešenie problémov, ktoré môžu byť rozdelené na menšie inštancie toho istého problému. Napríklad:
```java
public class Rekurzia {
    public static int faktorial(int n) {
        if (n == 0) {
            return 1;
        } else {
            return n * faktorial(n - 1);
        }
    }
}
```
V tomto príklade je metóda `faktorial` rekurzívna, pretože volá sama seba na menšie hodnoty až do dosiahnutia podmienky ukončenia rekurzie.
