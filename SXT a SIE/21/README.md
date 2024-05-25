# Zadanie

- princíp symetrického šifrovania DES, IDEA a vlastnosti hash algoritmov
- princíp nesymetrického šifrovania RSA
- princíp použitia elektronického podpisu
- kombinácia šifrovania a podpisu PGP

# Vypracovanie

## Princíp symetrického šifrovania DES, IDEA

**DES (Data Encryption Standard)**

- **Princíp**: Symetrický šifrovací algoritmus, ktorý používa 56-bitový kľúč na šifrovanie 64-bitových blokov dát cez 16 kôl permutácií a substitúcií.

- **Vlastnosti**: Relatívne rýchly, ale považovaný za nebezpečný pre svoju krátku dĺžku kľúča, ktorá je náchylná na útok hrubou silou.

**IDEA (International Data Encryption Algorithm)**

- **Princíp**: Symetrický šifrovací algoritmus, ktorý používa 128-bitový kľúč na šifrovanie 64-bitových blokov dát cez 8 kôl algebraických operácií, ako sú XOR, adícia a násobenie.

- **Vlastnosti**: Vyššia bezpečnosť ako DES, rýchly a efektívny, používaný napríklad v PGP.

## Vlastnosti hash algoritmov

Transformujú ľubovoľne dlhý vstup na pevne dlhý výstup (hash), ktorý je jedinečný pre každý unikátny vstup.

- **Jednosmernosť**: Ťažko získať pôvodný vstup z hash hodnoty.

- **Deterministickosť**: Rovnaký vstup vždy produkuje rovnaký hash.
- **Kolízna odolnosť**: Ťažko nájsť dva rôzne vstupy, ktoré produkujú rovnaký hash.
- **Rýchlosť**: Rýchle generovanie hash hodnôt.

## Princíp nesymetrického šifrovania RSA

- **Princíp**: Nesymetrický šifrovací algoritmus, ktorý používa dvojicu kľúčov: verejný kľúč na šifrovanie a súkromný kľúč na dešifrovanie. Bezpečnosť RSA spočíva v obtiažnosti faktorizácie veľkých prvočísel.

- **Vlastnosti**: Vysoká bezpečnosť, široko používaný na zabezpečenie dát, podpisovanie a výmenu kľúčov, avšak pomalší v porovnaní so symetrickými algoritmami.

## Princíp použitia elektronického podpisu

- **Princíp**: Elektronický podpis využíva nesymetrické šifrovanie, kde odosielateľ používa svoj súkromný kľúč na vytvorenie podpisu dokumentu (hash hodnoty dokumentu), ktorý môže byť overený pomocou verejného kľúča odosielateľa.

- **Vlastnosti**: Zaručuje autentickosť, integritu a nepopierateľnosť podpisovaného dokumentu.

## Kombinácia šifrovania a podpisu PGP

- **Princíp**: PGP (Pretty Good Privacy) kombinuje symetrické šifrovanie na rýchlu a efektívnu šifráciu dát a nesymetrické šifrovanie na bezpečný prenos kľúčov a elektronický podpis na overenie identity a integrity.
- **Proces**:
  - **Šifrovanie dát**: Dokument je zašifrovaný pomocou symetrického kľúča (napr. IDEA).

  - **Šifrovanie kľúča**: Symetrický kľúč je zašifrovaný pomocou verejného kľúča príjemcu (napr. RSA).
  - **Elektronický podpis**: Hash dokumentu je vytvorený a podpísaný súkromným kľúčom odosielateľa.
  - **Príjemca**: Dešifruje symetrický kľúč pomocou svojho súkromného kľúča a následne dešifruje dokument pomocou symetrického kľúča; overí elektronický podpis verejným kľúčom odosielateľa.
