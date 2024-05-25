# Zadanie

- vlastnosti statického smerovania
- vlastnosti dynamického smerovania
- pojmy metrika, administratívna vzdialenosť, konvergencia
- typy adries IPv4 uveďte súvislosť s VLSM, CIDR
- vplyv správnosti nastavenia IP, maska, brána a DNS na funkčnosť v sieti
- dôvody vzniku a vlastnosti IPv6

# Vypracovanie

## Statické smerovanie

Proces manuálneho konfigurovania smerovacích ciest v sieti administrátorom.

### Vlastnosti

- **Jednoduchosť**: Jednoduché nastavenie a údržba v malých sieťach.
- **Kontrola**: Umožňuje administrátorovi presnú kontrolu nad smerovacím správaním.
- **Bezpečnosť**: Menej náchylné na zneužitie a chyby spôsobené dynamickými protokolmi.
- **Nevýhody**: Neškálovateľnosť, náročnosť na správu pri zmene topológie alebo vo veľkých sieťach.

## Dynamické smerovanie

Automatický proces smerovania, ktorý používa smerovacie protokoly na výpočet a aktualizáciu ciest v sieti.

### Vlastnosti

- **Automatizácia**: Smerovacie protokoly automaticky zisťujú a udržiavajú trasy.

- **Škálovateľnosť**: Jednoduchšie spravovanie veľkých a zložitých sietí.
- **Konvergencia**: Automatické prispôsobenie sa zmenám v sieti.
- **Nevýhody**: Vyššia komplexnosť a riziko zraniteľnosti voči útokom na smerovacie protokoly.

## Pojmy metrika, administratívna vzdialenosť, konvergencia

- **Metrika**: Číselná hodnota používaná smerovacími protokolmi na určenie najlepšej cesty k cieľu; môže zahŕňať faktory ako počet skokov, šírka pásma, oneskorenie.
- **Administratívna vzdialenosť** (AD): Hodnota používaná na určenie priority smerovacích protokolov, ak existujú viaceré cesty k rovnakému cieľu; nižšia hodnota znamená vyššiu prioritu.
- **Konvergencia**: Proces, počas ktorého všetky smerovače v sieti aktualizujú svoje smerovacie tabuľky a dosiahnu konzistentný stav po zmene topológie.

## Typy adries IPv4

- **Verejné**: IP adresy sietí

- **Súkromné**: IP adresy zariadení v sieti (192.168.x.x; 172.16-31.x.x; 10.x.x.x ...)

---

- **Unicast**: Adresy priradené jednotlivým sieťovým rozhraniam.

- **Broadcast**: Adresy používané na odoslanie paketu všetkým uzlom v sieti. (192.168.1.255)
- **Multicast**: Adresy používané na odoslanie paketu skupine uzlov. (224.0.0.0 - 239.255.255.255)
- **Anycast**: Adresy priradené viacerým rozhraniam, kde paket je doručený najbližšiemu rozhraniu.

## VLSM a CIDR

**VLSM (Variable Length Subnet Masking)**: Technika umožňujúca použitie rôznych dĺžok masky podsiete v tej istej sieti, čím sa efektívnejšie využíva IP adresačný priestor.

**CIDR (Classless Inter-Domain Routing)**: Metóda zlepšujúca smerovanie a prideľovanie IP adries, ktorá umožňuje agregáciu viacerých IP sietí do jedného zápisu (napr. 192.168.0.0/16, 192.168.1.0/24).

- CIDR číslo - označuje rozsah IP adries pomocou formátu "prefix/adresa," kde prefix určuje počet bitov v sieti, napríklad 192.168.1.0/24.

## Vplyv správnosti nastavenia IP, maska, brána a DNS na funkčnosť v sieti

- **IP adresa**: Identifikuje konkrétne zariadenie v sieti; nesprávna adresa môže spôsobiť, že zariadenie nebude prístupné.

- **Maska podsiete**: Určuje veľkosť a rozsah podsiete; nesprávna maska môže spôsobiť problémy s komunikáciou v rámci siete.
- **Predvolená brána**: Poskytuje cestu pre prístup k iným sieťam; nesprávne nastavenie zabráni prístupu k externým sieťam (napr. internetu).
- **DNS** (Domain Name System): Prekladá doménové mená na IP adresy; nesprávne nastavenie DNS môže spôsobiť problémy s prístupom na webové stránky a služby podľa mena.

## Dôvody vzniku a vlastnosti IPv6

### Dôvody vzniku

- **Nedostatok adries IPv4**: Adresný priestor IPv4 (32-bitový) je obmedzený na približne 4,3 miliardy adries, čo nestačí pre rastúci počet zariadení.

- **Bezpečnosť**: IPv6 má zabudované bezpečnostné funkcie (IPsec) pre autentifikáciu a šifrovanie.
- **Efektivita**: IPv6 zjednodušuje smerovanie a správu siete, znižuje potrebu NAT (Network Address Translation).

### Vlastnosti

- **Veľký adresný priestor**: IPv6 používa 128-bitové adresy, čo poskytuje 340 undeciliónov (3,4×10^38) možných adries.

- **Zjednodušené smerovanie**: Menšie smerovacie tabuľky a efektívnejšia agregácia adries.
- **Bezpečnosť**: Povinná podpora pre IPsec, čo zlepšuje bezpečnosť komunikácie.
- **Automatická konfigurácia**: Podpora pre SLAAC (Stateless Address Autoconfiguration), umožňujúca zariadeniam automaticky získať adresy bez potreby DHCP servera.
- **Žiadna potreba NAT**: Každé zariadenie môže mať svoju jedinečnú verejnú IP adresu.
