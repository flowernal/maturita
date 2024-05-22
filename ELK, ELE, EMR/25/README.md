# Zadanie

Sekvenčné obvody všeobecné a ich rozdelenie, zapojenia RS, RST, JK, D a T sekvenčných obvodov, praktické využitie sekvenčných obvodov (čítače, registre, deličky frekvencie).

# Vypracovanie

## Sekvenčné logické obvody

- Číslicové elektronické obvody, u ktorých závisí stav výstupov okrem aktuálneho stavu vstupov aj od minulého stavu vstupov
- Majú pamäťové vlastnosti
- Najjednoduchšie základné sekvenčné obvody sa nazývajú **preklápacie obvody**:
  - **Monostabilný** - jeden stabilný stav
  - **Astabilný** - nemá stabilný stav, výstup sa stále prepína medzi 0 a 1, používa sa ako generátor impulzu
  - **Bistabilný** - dva stabilné stavy, môže v nich zostať ľubovoľnú dobu, preklopí sa na vonkajší podnet, využívame ako napr. pamäť, na počítadlá atď.
- Časť sekvenčných obvodov je konštruovaná tak, že sa ich výstupy menia, len ak sa mení v niektorom smere jeden zo vstupov, tzv. **hodinový vstup** (angl. clock)
- Táto reakcia može byť na **nábežnú** hranu - čelo impulzu (zmena z 0 na 1) alebo **dobežnú** hranu - (zmena z 1 na 0) hodinového signálu, zriedkavo aj na obe hrany
- Sekvenčné obvody majú obvykle aj vstup pre reset, ktorým sa obvod dá uviesť do definovaného (počiatočného) stavu, napr. po pripojení napájacieho napätia
- Elementárne sekvenčné obvody - **preklápacie obvody typu RS, T, D, JK**

### RS

- Najjednoduchší asynchrónny BPO.
- **Vstup S** (Set - nastavenie) slúži ako vstup signálu, ktorým sa nastavuje klopný obvod do log1
- **Vstup R** (Reset - nulovanie) slúži ako vstup signálu pre nulovanie klopného obvodu
- Kombinácia R = S = log1 sa nazýva zakázaný (alebo tiež nestabilný, hazardný) stav, pretože pri ňom nie je definované v akom stave zostane obvod po návrate R a S na log0
- **Pri zapisovaní musí byť na vstupe S úroveň log0**, na výstupe Q je úroveň log1. **Ak treba zmeniť stav na opačnú hodnotu, musí byť na vstupe R úroveň log1**

| S   | R   | Q+1 | Q̅+1 | Poznámka      |
| --- | --- | --- | --- | ------------- |
| 0   | 0   | Q   | Q̅   | pôvodný stav  |
| 0   | 1   | 0   | 1   | vynulovanie   |
| 1   | 0   | 1   | 0   | nastavenie    |
| 1   | 1   | ?   | ?   | zakázaný stav |

### RST

- Vychádza z preklápacieho obvodu RS, je doplnený o hodinový vstup **T (C-clock)**, čiže **informácia sa zapisuje len ak je hodnota na vstupe T log1**
- Princíp zostáva zachovaný ako u RS, avšak k preklopeniu obvodu dochádza len v závislosti od hodnoty signálu na hodinovom vstupe T (time/clock)
- Ak je na T privedená log0 obvod nereaguje na zmeny na vstupoch R a S.
- **Obvod RST je synchronizovaný úrovňou hodinového signálu, jeho stav je možné meniť po celú dobu trvania hodinového impulzu.**

| S   | R   | T   | Q+1 | Q̅+1 | Poznámka      |
| --- | --- | --- | --- | --- | ------------- |
| x   | x   | 0   | Q   | Q̅   | pôvodný stav  |
| 0   | 0   | 1   | Q   | Q̅   | pôvodný stav  |
| 0   | 1   | 1   | 0   | 1   | vynulovanie   |
| 1   | 0   | 1   | 1   | 0   | nastavenie    |
| 1   | 1   | 1   | ?   | ?   | zakázaný stav |

### JK

- Vznikol z 2-čínného RST zavedením spätných väzieb
- Spätné väzby zabraňujú vzniku **neurčitého stavu**
- Môžu byť použité ako základ čítačov

### D

- Vznikol zapojením vstupov RST tak, aby na jeho vstupoch nemohla vzniknúť kombinácia pre neurčitý stav
- Dosiahlo sa to zapojením invertora medzi vstupy RS
- Slúžia pre zápis dát prichádzajúcich po jednom vodiči

### T

- Špeciálne zapojenie JK alebo D
- 1 vstup - T - hodinový
- Ak je na T log0, obvod zachováva pôvodný stav, po privedení log1 sa stav zneguje

### Praktické využitie sekvenčných obvodov

- **Registre** - ukladanie dát = obvody D
- **Čítače** - počítanie impulzov = obvody T
- **Deličky frekvencie** - obvody T
