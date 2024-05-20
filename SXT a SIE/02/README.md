# 02

# Zadanie

- činnosť a úlohy služieb DHCP, DNS a mail
- možnosti použitia Active Directory
- princíp fungovania súborového, streaming media a deployment servera

---

# Vypracovanie

## Činnosť a úlohy DHCP, DNS a mail

### DHPC (Dynamic Host Configuration Protocol)

- Hlavnou úlohou DHCP je priraďovanie IP adries a konfiguračných parametrov zariadeniam.

1. **Priraďovanie IP adries**: DHCP dynamicky priraďuje IP adresy zariadeniam na sieti. Tým sa eliminuje potreba, aby sieťový administrátor manuálne priraďoval IP adresy všetkým sieťovým zariadeniam, čo znižuje riziko konfliktov IP adries a zjednodušuje správu siete.
2. **Konfiguračné parametre siete**: Okrem IP adries môže DHCP konfigurovať aj ďalšie sieťové nastavenia, ako napríklad:
    - **Maska podsiete**: Definuje sieťové a hostiteľské časti IP adresy.
    
    - **Predvolená brána**: Určuje IP adresu smerovača, ktorý by zariadenie malo použiť na odosielanie prevádzky do destinácií mimo miestnu sieť.
    - **DNS servery**: Poskytuje adresy serverov Domain Name System (DNS), ktoré by zariadenie malo použiť na preklad doménových mien na IP adresy.
3. **Mechanizmus prenájmu**: DHCP priraďuje IP adresy na určitú dobu prenájmu. To znamená, že priradená IP adresa je dočasná a bude vrátená do poolu dostupných adries, keď platnosť prenájmu vyprší, ak nebude obnovená. To umožňuje efektívne opätovné použitie IP adries v sieti.
4. **Centrálna správa**: Pomocou DHCP môžu sieťoví administrátori centrálne spravovať priraďovanie IP adries z DHCP servera. Táto centralizácia zjednodušuje správu siete, najmä v veľkých a dynamických sieťach.
5. **Podpora mobility zariadení**: DHCP podporuje mobilné zariadenia, ktoré sa pohybujú medzi rôznymi segmentmi siete. Keď sa zariadenie pripojí k novému segmentu, môže automaticky získať novú IP adresu a sieťovú konfiguráciu vhodnú pre tento segment.

### DNS (Domain Name System)

- zodpovedá za preklad doménových mien (www.sosst.sk) na IP adresy (188.121.181.143)

1. **Distribuovaná databáza**: DNS funguje ako distribuovaná databáza, čo znamená, že žiadna jediná entita nemá všetky informácie. Namiesto toho sú DNS informácie distribuované cez globálnu sieť serverov. Táto decentralizácia zlepšuje redundanciu a spoľahlivosť.
2. **Hierarchia a škálovateľnosť**: DNS používa hierarchickú štruktúru na správu doménových mien. Na vrchole sú root servery, nasledované doménami najvyššej úrovne (TLD) ako .com, .org, .net a krajiny kódy ako .uk a .sk. Pod nimi sú domény druhej úrovne (ako example.com) a ďalej. Tento hierarchický prístup pomáha spravovať obrovské množstvo doménových mien a umožňuje škálovateľnosť.
3. **Lokalizácia e-mailových serverov (MX záznamy)**: DNS sa tiež používa na lokalizáciu e-mailových serverov. Mail Exchange (MX) záznamy v DNS špecifikujú mailové servery zodpovedné za prijímanie e-mailov v mene domény.
4. **Bezpečnostné vylepšenia (DNSSEC)**: DNS Security Extensions (DNSSEC) pridávajú vrstvu bezpečnosti do DNS protokolu tým, že umožňujú overenie autenticity a integrity DNS odpovedí, čím chránia proti určitým typom útokov ako je DNS spoofing.

### Mail

1. **Zloženie správy**: Používatelia vytvárajú emaily pomocou emailových klientov (softvérových aplikácií) alebo webových rozhraní. Tieto klienty poskytujú funkcie na komponovanie, formátovanie a pripájanie súborov k emailu.
2. **Odosielanie emailu**:
    - **SMTP (Simple Mail Transfer Protocol)**: Keď používateľ odošle email, emailový klient komunikuje so serverom SMTP, aby doručil správu. SMTP je protokol používaný na odosielanie emailov z klienta na server a medzi emailovými servermi.
    - **Mailové servery**: Email je odoslaný zo servera SMTP používateľa na server prijímateľa. Mailové servery ukladajú a spravujú doručovanie emailov. Môžu byť konfigurované na zvládanie veľkého objemu emailovej prevádzky a poskytovanie bezpečnostných funkcií.
3. **Transport emailu**:
    - **DNS a MX záznamy**: Na doručenie emailu, odosielajúci mailový server dopytuje systém DNS (Domain Name System) na nájdenie MX (Mail Exchange) záznamov domény prijímateľa. MX záznamy špecifikujú mailové servery zodpovedné za prijímanie emailov pre danú doménu.
    - **Smerovanie**: Na základe MX záznamov je email smerovaný cez internet, pričom môže prechádzať cez niekoľko medziľahlých serverov, kým nedorazí na server prijímateľa.
4. **Prijímanie emailu**:
    - **IMAP/POP3**: Emailový klient prijímateľa načítava email z jeho mailového servera pomocou protokolov ako IMAP (Internet Message Access Protocol) alebo POP3 (Post Office Protocol version 3). IMAP umožňuje spravovať emaily priamo na serveri, zatiaľ čo POP3 typicky sťahuje emaily do klienta a maže ich zo servera.
    - **Ukladanie emailov**: Mailový server prijímateľa uchováva prichádzajúce emaily v poštových schránkach, kým ich prijímateľ neprístupní. Používatelia môžu organizovať emaily do priečinkov a spravovať ich prostredníctvom svojho emailového klienta.
5. **Čítanie a správa emailov**: Prijímatelia čítajú a spravujú svoje emaily pomocou svojich emailových klientov alebo webových rozhraní. Tieto rozhrania poskytujú nástroje na organizáciu, odpovedanie, preposielanie a mazanie emailov.

## Možnosti použitia Active Directory (AD)

1. **Centralizovaná autentifikácia a autorizácia**:
    - **Autentifikácia používateľov a počítačov**: AD overuje identitu používateľov a počítačov v sieti. To zabezpečuje, že prístup k sieťovým zdrojom majú iba autorizovaní používatelia a zariadenia.
    - **Single Sign-On (SSO)**: Používatelia sa môžu prihlásiť raz a získať prístup k viacerým zdrojom bez nutnosti opakovaného zadávania prihlasovacích údajov, čo zvyšuje pohodlie a produktivitu používateľov.
2. **Správa zdrojov**:
    - **Centralizovaná správa zdrojov**: Administrátori môžu centrálne spravovať sieťové zdroje (ako počítače, tlačiarne a zdieľané súbory). Táto centralizácia zjednodušuje prideľovanie a správu zdrojov.
    - **Správa skupinovej politiky**: AD umožňuje administrátorom definovať a vynucovať politiky v celej sieti. Tieto politiky môžu kontrolovať nastavenia používateľov a počítačov, bezpečnostné konfigurácie, inštaláciu softvéru a ďalšie.
3. **Správa používateľov a skupín**:
    - **Používateľské účty**: Administrátori môžu vytvárať, spravovať a mazať používateľské účty v sieti. To zahŕňa nastavenie hesiel, definovanie oprávnení a správu atribútov používateľov.
    - **Skupiny a roly**: Používatelia môžu byť zoskupení na základe svojich rolí alebo oddelení, čo zjednodušuje správu oprávnení. Skupinové politiky môžu byť aplikované na skupiny namiesto jednotlivých používateľov, čo zjednodušuje administratívne úlohy.
4. **Bezpečnosť**:
    - **Kontrola prístupu**: AD umožňuje detailnú kontrolu prístupu k sieťovým zdrojom pomocou priradení oprávnení a práv. To pomáha chrániť citlivé dáta a zdroje pred neoprávneným prístupom.
    - **Bezpečnostné politiky**: Administrátori môžu vynucovať bezpečnostné politiky, ako napríklad komplexnosť hesiel a politiky ich vypršania, čím zvyšujú bezpečnosť siete.
5. **Adresárové služby**:
    - **Hierarchická štruktúra**: AD poskytuje hierarchickú organizačnú štruktúru, ktorá zahŕňa domény, stromy a lesy. Táto štruktúra pomáha efektívne organizovať a spravovať veľké a komplexné siete.
    - **Informácie o adresári**: AD uchováva podrobné informácie o sieťových objektoch (používatelia, skupiny, počítače atď.), čo uľahčuje ich vyhľadávanie a získavanie.
6. **Monitorovanie a reportovanie**:
    - **Záznam udalostí**: AD poskytuje rozsiahle zaznamenávanie udalostí súvisiacich s autentifikáciou, autorizáciou a adresárovými službami. Tieto záznamy sú kľúčové pre monitorovanie sieťovej aktivity, riešenie problémov a audit bezpečnosti.
    - **Nástroje na reportovanie**: AD obsahuje nástroje a funkcie na generovanie reportov o rôznych aspektoch adresárových služieb, ako je aktivita používateľov, členstvo v skupinách a súlad s politikami.

## Princíp fungovania súborového, streaming media a deployment servera

### File server

1. **Hardvér a softvér:** 
    - Súborový server pozostáva z dedikovaného hardvéru a softvéru (operačný systém ako Windows Server, Linux alebo špecializovaný OS NAS (Network Attached Storage)). Hardvér servera je vybavený významnou kapacitou úložiska, RAM a výpočtovou silou na spracovanie viacerých súčasných požiadaviek.
2. **Správa úložiska:**
    - **Súborový systém:** Súborový server používa súborový systém (ako NTFS, ext4 alebo ZFS) na správu toho, ako sú údaje ukladané a získavané na jeho úložiskových zariadeniach.
    - **Štruktúra adresára:** Administrátori vytvárajú štruktúrovanú hierarchiu adresárov na usporiadanie súborov do priečinkov a podpriečinkov. Táto organizácia pomáha pri jednoduchom navigovaní a správe súborov.
3. **Správa používateľov a prístupu:**
    - **Používateľské účty**: Administrátori vytvárajú používateľské účty a skupiny s konkrétnymi oprávneniami. Tým sa zabezpečuje, že len autorizovaní používatelia môžu pristupovať k určitým súborom a adresárom.
    - **Zoznamy kontrol prístupu (ACL):** Oprávnenia sú definované pomocou ACL, ktoré určujú, aké akcie (čítanie, zápis, vykonávanie) môže každý používateľ alebo skupina vykonávať na konkrétnych súboroch alebo adresároch.
4. **Ukladanie a zdieľanie súborov:**
    - **Ukladanie súborov:** Používatelia nahrajú súbory na súborový server, ktoré sú potom uložené v určených adresároch.
    - **Zdieľanie súborov**: Súborový server umožňuje používateľom zdieľať súbory a adresáre s inými v sieti. Zdieľané adresáre môžu byť mapované ako sieťové jednotky na počítačoch používateľov pre jednoduchý prístup.
5. **Prenos údajov:**
    - **Sieťové protokoly:** Súborové servery používajú sieťové protokoly ako SMB/CIFS (Server Message Block/Common Internet File System) pre Windows siete alebo NFS (Network File System) pre Unix/Linux siete na uľahčenie zdieľania súborov a komunikácie medzi serverom a klientmi.
    - **Prístup k súborom:** Keď používateľ požiada o súbor, zariadenie klienta pošle požiadavku na súborový server pomocou jedného z týchto protokolov. Server spracuje požiadavku a prenáša údaje o súbore späť klientovi.
6. **Bezpečnosť a šifrovanie:**
    - **Overenie:** Používatelia sa musia overiť (zvyčajne pomocou používateľského mena a hesla), aby pristúpili k súborovému serveru. Tým sa zabezpečuje, že len autorizované osoby môžu pristupovať k serveru.
    - **Šifrovanie:** Údaje môžu byť šifrované tak pri prenose (použitím protokolov ako TLS/SSL) aj v pohybe (použitím šifrovania disku), aby sa chránili pred neoprávneným prístupom a porušeniami údajov.
7. **Zálohovanie a redundancia:**
    - **Pravidelné zálohy:** Súborové servery často obsahujú automatizované riešenia zálohovania na vytvorenie kópií uložených údajov pravidelne. Tieto zálohy sa môžu ukladať na samostatné úložiskové zariadenia alebo do cloudu.
    - **Redundancia:** Techniky ako RAID (Redundant Array of Independent Disks) sa používajú na poskytnutie redundantnosti údajov

### Streaming

1. **Kódovanie Obsahu a Ukladanie**:
    - formáty môžu zahŕňať štandardy ako MPEG-DASH, HLS (HTTP Live Streaming) alebo RTMP (Real-Time Messaging Protocol).
    - Kódovaný obsah sa ukladá na streamingový server alebo príslušné úložiskové systémy.
2. **Požiadavka Klienta**:
    - Keď používateľ chce pristupovať k streamingovému obsahu, jeho zariadenie pošle požiadavku na streamingový server
3. **Vyjednávanie o Streamingovom Protokole**:
    - Streamingový server prijíma požiadavku klienta a vyjednáva vhodný streamingový protokol a bitovú rýchlosť na základe faktorov, ako sú stav siete, schopnosti zariadenia a dostupné formáty obsahu.
    - Napríklad, ak zariadenie klienta podporuje HLS, server môže doručiť obsah pomocou protokolu HLS a vybrať vhodnú variantu bitového prúdu na základe rýchlosti siete zariadenia.
4. **Prenos Dát**:
    - Streamingový server začína prenášať multimediálny obsah klientovému zariadeniu vo forme malých, postupných paketov alebo častí cez štandardné internetové protokoly ako HTTP alebo RTMP.
    - Na rozdiel od tradičného sťahovania súborov, kde sa celý súbor stiahne pred začatím prehrávania, streamingový server dodáva obsah postupne, umožňujúc používateľom začať konzumovať obsah, kým sa zvyšok obsahu stále sťahuje na pozadí.
5. **Ukladanie do Buffra a Prehrávanie**:
    - Kým klientové zariadenie prijíma streamingové dáta, ukladá si istú časť obsahu do buffra na zabezpečenie plynulého prehrávania a kompenzáciu variácií rýchlosti siete. Tento buffer pomáha zabrániť prerušeniam alebo pauzám počas prehrávania.
    - Klientové zariadenie dekóduje a vykresľuje streamingové dáta v reálnom čase, čo umožňuje používateľom sledovať alebo počúvať obsah, ako prichádza.
6. **Adaptívny Bitový Streaming (ABR)**:
    - Mnohé moderné streamingové servery podporujú adaptívne streamovanie s rôznymi úrovňami kvality (bitových rýchlostí). Klientové zariadenie dynamicky prepína medzi týmito úrovňami na základe podmienok siete.
    - Techniky ABR, ako je MPEG-DASH a HLS s viacerými variantami bitových prúdov, pomáhajú optimalizovať zážitok z streamovania pre používateľov na rôznych zariadeniach a podmienkach siete.
7. **Ochrana Obsahu a Správa Digitálnych Práv (DRM)**:
    - Streamingové servery často zahŕňajú bezpečnostné funkcie na ochranu autorských práv pred neoprávneným prístupom a pirátstvom. To môže zahŕňať implementáciu riešení DRM na šifrovanie a bezpečné doručovanie obsahu autorizovaným používateľom a zamedzenie neoprávnenej redistribúcie.

### Deployment server

- Deployment Server je typ servera používaný v softvérovom vývoji a operačných činnostiach IT na riadenie nasadenia softvérových aplikácií a aktualizácií cez sieť alebo viacero prostredí.
1. **Centralizované Nasadenie Softvéru**:
    - Deployment Server poskytuje centralizovanú platformu pre ukladanie softvérových balíkov a aktualizácií. Funguje ako repozitár, z ktorého sa softvér distribuuje na rôzne zariadenia a systémy v rámci siete.
2. **Automatizované Procesy Nasadenia**:
    - Deployment servery často podporujú automatizačné nástroje a skripty, ktoré zjednodušujú proces nasadenia. Automatizované nasadenie znižuje manuálnu intervenciu, minimalizuje chyby a zrýchľuje nasadenie aktualizácií a opráv softvéru.
3. **Verziovací Systém a Rollback**:
    - Deployment servery zvyčajne podporujú mechanizmy verziovania, ktoré umožňujú administrátorom sledovať rôzne verzie softvérových balíkov. To umožňuje jednoduchý rollback na predchádzajúce verzie v prípade problémov po nasadení.
4. **Správa Prostredí**:
    - Deployment servery môžu riadiť viacero nasadzovaných prostredí, ako sú vývojové, testovacie, stagingové a produkčné. To umožňuje kontrolované a konzistentné nasadenie v rôznych fázach životného cyklu softvéru.
5. **Správa Konfigurácie**:
    - Okrem nasadenia softvéru často deployment servery riešia aj úlohy správy konfigurácie. Môžu posielať zmeny konfigurácie na servery a zariadenia, čím zabezpečujú konzistenciu prostredia softvéru.
6. **Správa Závislostí**:
    - Deployment servery môžu spravovať závislosti medzi softvérovými komponentami. Zabezpečujú, aby boli všetky potrebné závislosti nainštalované alebo aktualizované spolu s hlavným softvérovým balíkom, čo znižuje problémy s kompatibilitou.
7. **Bezpečnosť a Riadenie Prístupu**:
    - Deployment servery uplatňujú prístupové kontroly, aby sa zabezpečilo, že softvér môže nasadzovať iba autorizovaný personál. Tiež podporujú šifrovanie a bezpečné komunikačné protokoly na ochranu citlivých údajov počas nasadenia.
8. **Monitorovanie a Reportovanie**:
    - Deployment servery poskytujú monitorovacie funkcie na sledovanie stavu nasadení v reálnom čase. Generujú správy o úspešnosti nasadení, chybách a výkonnostných metrikách, čo pomáha pri riešení problémov a optimalizácii.
