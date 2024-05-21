# Zadanie

- bezdrôtové siete podľa dosahu, typy BT, WiFi, SAT, IR, ....,
- jednotlivé kategórie, pásma a ich prenosové rýchlosti,
- popíšte používané technológie (mesh, MIMO, multi-RU, ...),
- norma pre siete WiFi a jej varianty,
- možnosti konfigurácie bezdrôtovej WiFi siete,
- kontrola integrity a šifrovanie TKIP a AES (WEP, WPA, WPA2, WPA3,...)

# Vypracovanie

## Rozdelenie sietí podľa dosahu

### Bluetooth

- Bluetooth je najčastejšie používaný v P2P (Peer to Peer) komunikácii. Jeho efektívna vzdialenosť je približne 10 metrov.

### WiFi

- Využíva sa hlavne v LAN sieťach. Používaná do vzdialenosti 50 metrov.

### Satelite

- Využíva satelity umiestnené na obežnej dráhe Zeme. Poskytuje vysokorýchlostné pripojenie pre rozsiahlu oblasť, alebo slúži pre prenos informácií na väčšie vzdialenosti.

### Infrared

- Infračervené site majú veľmi krátky dosah, väčšinou používané na miestach, kde má vysielač priamy výhľad na prijímač.

## Kategórie WiFi

### WiFi 0

- Prenosová rýchlosť: 2 Mbps
- Využívané pásma: 2.4GHz

### WiFi 1

- Prenosová rýchlosť: 11 Mbps
- Využívané pásma: 2.4GHz

### WiFi 2

- Prenosová rýchlosť: 54 Mbps
- Využívané pásma: 5 GHz

### WiFi 3

- Prenosová rýchlosť: 54 Mbps
- Využívané pásma: 2.4GHz

### WiFi 4

- Prenosová rýchlosť: 150-300 Mbps (Maximum 600 Mbps)
- Využívané pásma: 2.4GHz a 5 GHz

### WiFi 5

- Prenosová rýchlosť: 6.9 Gbps
- Využívané pásma: 5 GHz

### WiFi 6

- Prenosová rýchlosť: 9.6 Gbps
- Využívané pásma: 2.4GHz a 5 GHz

### WiFi 7

- Prenosová rýchlosť: 40 Gbps
- Využívané pásma: 2.4GHz, 5 GHz a 6GHz

## Používané technológie

### Mesh

Mesh systém využíva sústava dobre umiestnených AP (Access Point) po objekte.

Tieto AP sú navzájom prepojené a užívateľa si predávajú v závislosti od toho, pri ktorom AP je užívateľ bližšie. Vo výsledku to pre užívateľa znamená to, že sa nemusí prepájať medzi niekoľkými sieťami ale stále je pripojený k jednej.

### MIMO

MIMO je technológia, ktorá umožňuje AP vysielať viacero signálov súčasne pomocou viacerých antén.

V tradičných systémoch Wi-Fi prístupový bod komunikuje s klientmi postupne, čo môže viesť k oneskoreniam, ak je veľa klientov súčasne pripojených. S MU-MIMO môže prístupový bod komunikovať s viacerými klientmi súčasne, pričom každému klientovi poskytuje vlastné dáta.

### Multi Resource Units

V sieti Wi-Fi je rámcová jednotka (RU) časový interval, počas ktorého jedno zariadenie komunikuje s prístupovým bodom. Tento časový interval je rozdelený do rámcov pre jednotlivých klientov.

Pri použití technológie Multi-RU v sieti Wi-Fi má prístupový bod schopnosť priradiť viacero rámcových jednotiek (RU) rôznym klientom súčasne. To znamená, že prístupový bod môže súčasne obslúžiť viac klientov a poskytnúť im prístup k pripojeniu bez nutnosti čakať na ich postupné spracovanie.

## Norma pre siete WiFi

Norma pre siete Wi-Fi je séria štandardov vytvorených organizáciou IEEE (Institute of Electrical and Electronics Engineers), ktoré špecifikujú technické parametre pre bezdrôtové siete.

Tento štandard bol prvýkrát zavedený v roku 1997 a bol zameraný na bezdrôtové siete. Definuje rôzne fyzické a linkové vrstvy pre bezdrôtovú komunikáciu.

- IEEE 802.11 (WiFi 0)
- IEEE 802.11b (WiFi 1)
- IEEE 802.11a (WiFi 2)
- IEEE 802.11g (WiFi 3)
- IEEE 802.11n (WiFi 4)
- IEEE 802.11ac (WiFi 5)
- IEEE 802.11ax (WiFi 6)
- IEEE 802.11be (WiFi 7)

## Možnosti konfigurácie bezdrôtovej WiFi siete

### **Názov siete (SSID)**

Názov siete je identifikátor, ktorý umožňuje klientom nájsť a pripojiť sa k našej sieti. Pri konfigurácii môžeme zvoliť jedinečný a ľahko zapamätateľný názov.

### **Zabezpečenie siete**

Zabezpečenie siete je dôležité na ochranu siete pred neoprávneným prístupom. Môžeme zvoliť rôzne typy zabezpečenia, ako sú WPA2 alebo WPA3, a nastaviť heslo na prístup k sieti.

### **Kanál siete**

Wi-Fi siete používajú rôzne kanály na prenos dát. Pri konfigurácii môžeme zvoliť optimálny kanál, aby ste minimalizovali rušenie a maximalizovali výkon siete. Na Slovensku existuje 13 týchto kanálov. V praxi sa často využíva automatické prepínanie tých kanálov ktoré si riadi sám router.

### **Guest Network (Hostiteľská sieť)**

Ak chceme oddeliť pripojenia hostí od našej hlavnej siete, môžeme vytvoriť samostatnú hostiteľskú sieť. Toto umožňuje hosťom prístup na internet, ale obmedzuje im prístup k zariadeniam v našej hlavnej sieti.

### **Nastavenie DHCP**

DHCP (Dynamic Host Configuration Protocol) prideľuje IP adresy zariadeniam v sieti automaticky. Môžeme upraviť rozsah IP adries, aby sa zabránilo konfliktom adries alebo priradiť špecifické IP adresy konkrétnym zariadeniam.

### **Port Forwarding**

Port forwarding umožňuje zariadeniam na vonkajšej strane siete (WAN) pristupovať k službám alebo aplikáciám v našej sieti. To je užitočné napríklad pre vzdialený prístup k zariadeniam alebo hostovanie serverov.

### **VPN (Virtual Private Network)**

Nastavenie VPN v routri umožňuje zabezpečené pripojenie klientov z externej siete do našej siete cez internet. To poskytuje zvýšenú bezpečnosť a ochranu dát pri pripájaní k verejnej sieti.

### **Správa rôznych pásiem**

Umožňuje nám spravovať ktoré pásma WiFi siete sa budú používať (2.4GHz, 5GHz, 6GHz).

## Kontrola integrity a šifrovanie bezdrôtovej siete

### WEP (Wired Equivalent Privacy)

Šifrovanie WEP používa slabé šifrovacie metódy na ochranu komunikácie, čo ho robí zraniteľným voči útokom a nie je viac považovaný za bezpečný štandard. Kontrola integrity WEP používa 24-bitový kontrolný kód (CRC-32) na kontrolu integrity rámcov dát. Avšak táto metóda je pomerne slabá a ľahko prelomiteľná.

### WPA (Wi-Fi Protected Access):

Šifrovanie WPA používa TKIP (Temporal Key Integrity Protocol), ktorý vylepšuje šifrovaciu metódu WEP tým, že používa dynamické kľúče a periodickú zmenu kľúčov. Kontrola integrity: TKIP používa MIC (Message Integrity Check) na kontrolu integrity pre každý rámec datagramu. Tento mechanizmus poskytuje vyššiu úroveň ochrany integrity než WEP.

### WPA2 (Wi-Fi Protected Access 2)

Šifrovanie WPA2 je vylepšená verzia WPA, ktorá používa šifrovaciu metódu AES (Advanced Encryption Standard), ktorá je oveľa bezpečnejšia než TKIP. Kontrola integrity AES nepotrebuje samostatný mechanizmus kontroly integrity, pretože šifrovací algoritmus sám o sebe poskytuje integritu dát.

### WPA3 (Wi-Fi Protected Access 3)

Šifrovanie: WPA3 je najnovšia verzia štandardu Wi-Fi, ktorá ponúka vyššiu úroveň bezpečnosti. Používa šifrovaciu metódu Simultaneous Authentication of Equals (SAE) a vylepšenú ochranu pred útokmi Brute Force.
