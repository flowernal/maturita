# Zadanie

Booleova algebra a jej základné logické funkcie, vytváranie logických sietí a ich zjednodušovanie, príklady na logické siete.

# Vypracovanie

## Booleova algebra

- Sústava zákonov, pravidiel a znakov určených na popis vzťahov medzi logickými premennými
- Logické premenné nadobúdajú 2 hodnoty - 0 a 1

## Základné logické funkcie

1. **AND (Logický súčin):** Výstup je pravdivý (1), iba ak sú obe vstupné hodnoty pravdivé (1).
   - $Y = A * B$ alebo $AB$

2. **OR (Logický súčet):** Výstup je pravdivý (1), ak je aspoň jeden z vstupov pravdivý (1).
   - $Y = A + B$

3. **NOT (Negácia):** Mení vstupnú hodnotu na opak.
   - $Y = !A$ alebo A̅

4. **NAND (Negovaný logický súčin)** 
   - Y = A̅ ̅*̅ ̅B̅

5. **NOR (Negovaný logický súčet)** ⊕   
   - Y = A̅ ̅+̅ ̅B̅

6. **XOR (Výhradný logický súčet)** ⊕   
   - Y = A ⊕ B = A̅B + B̅A

7. **XNOR (Výhradný negovaný logický súčet)** ⊕   
   - Y = A̅ ⊕̅ B̅ = A̅B̅ + AB

## Vytváranie logických sietí a ich zjednodušovanie

**Vytváranie logických sietí:**
- Logické siete sú tvorené spojením logických brán (AND, OR, NOT...) a vstupných premenných na vytvorenie žiadaného logického výstupu.

**Zjednodušovanie logických sietí:**
- Zjednodušovanie logických sietí zahŕňa minimalizáciu počtu a použitie logických brán a výrazov na dosiahnutie ekvivalentného logického výstupu s čo najmenším počtom komponentov.