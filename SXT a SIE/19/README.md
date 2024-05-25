# Zadanie

- štruktúrovaná kabeláž, generická sieť
- optika, kategórie, typy prenosu, norma
- metalické káble, kategórie a rýchlosti, parametre Twisted Pair, norma
- POE, POE+, PPOE - druhy a možná záťaž
- certifikácia štruktúrovanej kabeláže (ako prebieha, čo sa meria, čo je jej výsledkom)

# Vypracovanie

## Štruktúrovaná kabeláž, generická sieť

### Štruktúrovaná kabeláž

- **Definícia**: Systém univerzálnej kabeláže, ktorý je navrhnutý na podporu rôznych komunikačných služieb (dáta, hlas, video) v budovách a medzi nimi.

- **Súčasti**: Zahrnuje horizontálnu kabeláž, vertikálnu (chrbtovú) kabeláž, prepojovacie káble, patch panely a rozvodné skrine.
- **Výhody**: Flexibilita, škálovateľnosť, jednoduchá údržba a upgrade, minimalizácia rizika prerušenia služby.

### Generická sieť

- **Definícia**: Univerzálna infraštruktúra siete, ktorá môže podporovať rôzne typy zariadení a technológie. (TV, IP kamery, smart domácnosť..., nie len počítače)

- **Použitie**: Môže zahŕňať štruktúrovanú kabeláž, bezdrôtové siete, optické aj metalické káble na zabezpečenie rôznych komunikačných služieb.

## Optika

- **Definícia**: Použitie optických vlákien na prenos dát pomocou svetelných impulzov.
- **Výhody**: Vysoká rýchlosť prenosu dát, veľká šírka pásma, odolnosť voči elektromagnetickému rušeniu, dlhší dosah.

### Kategórie

- **Monovid** (Single-mode SMF): Tenké jadro (9 µm), prenáša svetlo jedným režimom, vhodné na dlhé vzdialenosti (až do 100 km).
- **Multivid** (Multi-mode MMF): Hrubšie jadro (50 µm alebo 62,5 µm), prenáša svetlo viacerými režimami, vhodné na kratšie vzdialenosti (do 2 km).

### Typy prenosu

- **Point-to-point Prenosy**: Tieto prenosy využívajú optické vlákno na priamu komunikáciu medzi dvoma bodmi. Sú ideálne pre prenosy s vysokou priamou kapacitou a rýchlosťou.

- **Vlnovodné Prenosy**: V tomto prípade sa využívajú rôzne vlnovodné technológie, ktoré umožňujú optimalizovaný prenos svetelných signálov v rôznych médiách a prostrediach.

- **Multiplexovanie a Demultiplexovanie**: Procesy multiplexovania a demultiplexovania umožňujú kombináciu viacerých signálov do jedného optického vlákna a ich následné rozdelenie na pôvodné signály.

### Normy

- **IEEE 802.3**: Štandard pre Ethernet pre optické siete.
- **TIA/EIA-568**: Štandard pre štruktúrovanú kabeláž, ktorý definuje špecifikácie pre inštaláciu a výkonnosť optických a metalických káblov.
- **ITU-T G.xxx**: Štandardy pre rôzne typy optických káblov a sietí

## Metalické káble

- **Definícia**: Použitie kovových vodičov (zvyčajne medených) na prenos dát pomocou elektrických signálov.

### Kategórie

| Kategória | Frekvencia | Rýchlosť | Vyhotovenie              | Aplikácia            |
| --------- | ---------- | -------- | ------------------------ | -------------------- |
| Cat 5e    | 100 MHz    | 1 Gbps   | UTP, F/UTP, U/FTP        | 1000BASE-T           |
| Cat 6     | 250 MHz    | 10 Gbps  | UTP, F/UTP, U/FTP        | 5GBASE-T, 10GBASE-T  |
| Cat 6A    | 500 MHz    | 10 Gbps  | UTP, F/UTP, U/FTP, S/FTP | 5GBASE-T, 10GBASE-T  |
| Cat 7     | 600 MHz    | 10 Gbps  | S/FTP, F/FTP             | 5GBASE-T, 10GBASE-T  |
| Cat 7A    | 1 GHz      | 10 Gbps  | S/FTP, F/FTP             | 5GBASE-T, 10GBASE-T  |
| Cat 8.1   | 2 GHz      | 25 Gbps  | F/UTP, U/FTP             | 25GBASE-T, 40GBASE-T |
| Cat 8.2   | 2.1 GHz    | 40 Gbps  | S/FTP, F/FTP             | 25GBASE-T, 40GBASE-T |

### Parametre Twisted Pair (krútená dvojlinka)

- **Impedancia**: Typicky 100 ohmov.

- **Krútenie**: Redukuje elektromagnetické rušenie medzi páry vodičov.
- **Prierez vodičov**: Priemer medených vodičov v kábli ovplyvňuje odolnosť kábla a maximálnu rýchlosť prenosu dát.
- **Tienenie**: STP (Shielded Twisted Pair) pre vyššiu odolnosť voči rušeniu, UTP (Unshielded Twisted Pair) bez tienenia.
- **Maximálna dĺžka**: Každá kategória kábla TP má špecifikovanú maximálnu dĺžku na spoľahlivý prenos údajov pri menovitej rýchlosti.

### Normy

- **IEEE 802.3**: Definuje normy pre Ethernet vrátane špecifikácií pre kabeláž TP a rozhrania Ethernet.
- **TIA/EIA-568**: Štandard pre štruktúrovanú kabeláž, ktorý definuje špecifikácie pre metalické káble vrátane kategórií a parametrov výkonu.

## POE, POE+, PPOE - druhy a možná záťaž

**POE (Power over Ethernet)**

- **Definícia**: Technológia na prenos elektrickej energie spolu s dátami cez ethernetové káble.

### Druhy

- **IEEE 802.3af (PoE)**: Poskytuje až 15.4 W na port.
- **IEEE 802.3at (PoE+)**: Poskytuje až 25.5 W na port.
- **IEEE 802.3bt (PoE++ alebo PPoE)**: Poskytuje až 60 W (Typ 3) a 100 W (Typ 4) na port.

**Použitie**: Napájanie zariadení ako IP kamery, bezdrôtové prístupové body, VoIP telefóny bez potreby samostatného napájania.

## Certifikácia štruktúrovanej kabeláže (ako prebieha, čo sa meria, čo je jej výsledkom)

### Ako prebieha

- **Inštalácia kabeláže**: Realizácia podľa noriem a špecifikácií (napr. TIA/EIA-568, IEEE 802.3).

- **Testovanie**: Použitie testovacích prístrojov na overenie správnosti inštalácie a výkonnostných parametrov kabeláže.

### Čo sa meria

- **Kontinuita vodičov**: Overuje, či sú všetky vodiče správne zapojené.

- **Dĺžka kabeláže**: Meria celkovú dĺžku každého kábla.
- **Skreslenie signálu** (NEXT, FEXT): Meria úroveň rušenia medzi pármi vodičov.
- **Útlm**: Meria stratu signálu pri prenose cez kabeláž.
- **Return Loss**: Meria odrazy signálu, ktoré môžu ovplyvniť kvalitu prenosu.

### Výsledok

- **Certifikát**: Potvrdenie o splnení noriem a špecifikácií pre inštalovanú kabeláž.

- **Výkonnostný report**: Detailný záznam o výsledkoch testov, vrátane meraných hodnôt a ich porovnanie s požadovanými štandardmi.
