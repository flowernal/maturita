# Zadanie

Pojmy objekt, trieda, abstraktná trieda, premenné v definícii triedy, metódy triedy, príklad deklarácie triedy, základné princípy dedičnosti a OOP v Jave.

# Vypracovanie

## Objekt

Objekt je konkrétna inštancia triedy. Reprezentuje konkrétnu entitu so stavom a správaním. Napríklad, ak máme triedu `Auto`, inštancie tejto triedy ako "môjAuto" alebo "tvojeAuto" sú objekty.

## Trieda

Trieda je šablóna alebo definícia, ktorá popisuje správanie a vlastnosti objektov danej triedy. Obsahuje atribúty (premenné) a metódy (funkcie). Trieda `Auto` by mohla mať atribúty ako farba, značka, rok výroby a metódy ako "štartovať" alebo "zastaviť".

## Abstraktná trieda

Abstraktná trieda je trieda, ktorá nemôže byť priamo inštanciovaná a slúži ako základ pre odvodené triedy. Obsahuje aspoň jednu abstraktnú metódu, ktorá musí byť implementovaná v odvodených triedach.

## Premenné v definícii triedy

Premenné v definícii triedy sú známe ako atribúty alebo členovia triedy. Môžu byť rôznych typov a slúžia na uchovávanie dát. Napríklad, v triede `Auto` by atribúty mohli byť `farba`, `značka`, `rokVyroby` atď.

## Metódy triedy

Metódy triedy sú funkcie alebo operácie, ktoré môžu byť vykonávané s inštanciami triedy. Mohli by to byť napríklad metódy `štartovať()`, `zastaviť()`, `zmeniťFarbu()` v triede `Auto`.

## Príklad deklarácie triedy

```java
public class Auto {
    // Atribúty
    String farba;
    String značka;
    int rokVyroby;

    // Konštruktor
    public Auto(String farba, String značka, int rokVyroby) {
        this.farba = farba;
        this.značka = značka;
        this.rokVyroby = rokVyroby;
    }

    // Metóda štartovať
    public void štartovať() {
        System.out.println("Auto štartuje.");
    }

    // Metóda zastaviť
    public void zastaviť() {
        System.out.println("Auto zastavuje.");
    }
}
```

## Základné princípy dedičnosti v OOP v Jave

Dedičnosť je kľúčovým konceptom v OOP, ktorý umožňuje jednej triede zdieľať vlastnosti a metódy inej triedy. V Jave dedičnosť funguje nasledovne:

- **Rodičovská trieda:** Trieda, ktorá poskytuje základnú implementáciu.
- **Potomkovská trieda:** Trieda, ktorá dedí vlastnosti a metódy z rodičovskej triedy a môže rozšíriť alebo prepísať ich podľa potreby.

Princípy dedičnosti v Jave zahŕňajú:

1. **Rodičovská trieda:** Definuje sa klíčovým slovom `extends`. Napríklad `public class PotomkovskaTrieda extends RodicovskaTrieda`.
2. **Metódy a atribúty:** Potomkovská trieda môže používať všetky verejné a chránené metódy a atribúty rodičovskej triedy.
3. **Prepísanie metód:** Potomkovská trieda môže prepísať metódy rodičovskej triedy pomocou anotácie `@Override`.
4. **Konštruktory:** Konštruktory nie sú dedené, ale môžu byť volané z konštruktora potomkovej triedy pomocou kľúčového slova `super()`.

Dedičnosť umožňuje znovupoužitie kódu, a tým zjednodušuje a zlepšuje organizáciu kódu v Jave.