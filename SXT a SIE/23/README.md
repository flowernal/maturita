# Zadanie

- analýza služieb a zariadení pri návrhu siete, výber zariadení, vplyv parametrov a hierarchia zapojenia a zakreslenie návrhu
- výkresová dokumentácia fyzického rozmiestenia častí siete (PC, LP, Racky, AP, kamery, prístupové systémy, IP telefóny,....)
- napájanie a technická správa
- logická schéma siete popis a konfigurácie zariadení
- zálohovanie a udržovanie dokumentácie v aktuálnom stave pri prevádzke

# Vypracovanie

## Analýza služieb a zariadení pri návrhu siete

**Analýza služieb**:

- **Identifikácia potrieb**: Zistite, aké služby budú v sieti potrebné (napr. internet, intranet, VoIP, video dohľad).

- **Požiadavky na šírku pásma**: Určite požadovanú šírku pásma pre každú službu.
- **Bezpečnosť**: Posúďte potrebu bezpečnostných opatrení (firewally, VPN, IDS/IPS).
- **Redundancia a spoľahlivosť**: Zohľadnite potrebu záložných spojení a zariadení.

**Výber zariadení**:

- **Routery a Switche**: Vyberte na základe požadovanej priepustnosti, počtu portov, funkcií (VLAN, PoE).

- **Servery**: Výber na základe výpočtového výkonu, úložnej kapacity a redundancie.
- **Bezpečnostné zariadenia**: Firewally, IDS/IPS, VPN brány.
- **Koncové zariadenia**: Počítače, tlačiarne, IP telefóny, kamery, AP.
- **Káble a konektory**: UTP/STP káble kategórie 5e, 6, 6a alebo 7, optické vlákna.

**Vplyv parametrov**:

- **Šírka pásma**: Ovplyvňuje výber switche a routerov.

- **Latencia**: Dôležité pre aplikácie ako VoIP a video konferencie.
- **Bezpečnosť**: Požiadavky na bezpečnostné protokoly a zariadenia.
- **Rozsah a škálovateľnosť**: Plánovanie budúceho rastu a možnosť rozšírenia siete.

**Hierarchia zapojenia a zakreslenie návrhu**:

- **Hierarchické vrstvy**: Core, Distribution, Access.

- **Core Layer**: Zaisťuje rýchle a spoľahlivé prepojenie medzi hlavnými segmentmi siete.
- **Distribution Layer**: Prepája Access Layer s Core Layer, implementuje smerovanie, firewalling, QoS.
- **Access Layer**: Prístup pre koncové zariadenia, implementuje VLANy, PoE.

## Výkresová dokumentácia fyzického rozmiestenia častí siete

**Fyzické umiestnenie**:

- **PC a pracovné stanice**: Rozmiestnenie podľa kancelárií alebo pracovných oblastí.

- **Tlačiarne** (LP): Centrálne umiestnené pre jednoduchý prístup.
- **Racky**: Miesta pre servery, switche a iné sieťové zariadenia, zvyčajne v serverovniach.
- **AP** (Access Pointy): Umiestnenie na pokrytie signálom celej potrebnej oblasti.
- **Kamery**: Strategické umiestnenie pre maximálne pokrytie a bezpečnosť.
- **Prístupové systémy**: Umiestnenie pri vstupoch a dôležitých miestach.
- **IP telefóny**: Na každom pracovnom mieste.

**Nástroje**: CAD softvér (napr. AutoCAD), špeciálny sieťový dizajn softvér (napr. Visio).

## Napájanie a technická správa

**Napájanie**:

- **Záložné zdroje** (UPS): Pre dôležité zariadenia ako servery a switche.

- **PoE** (Power over Ethernet): Pre napájanie AP, IP telefónov a kamier cez sieťové káble.
- **Záložné generátory**: Pre dôležité oblasti, kde nesmie dôjsť k výpadku napájania.

**Technická správa**:

- **Monitorovanie**: Nástroje na sledovanie výkonnosti a stavu zariadení (napr. Nagios, Zabbix).

- **Údržba**: Pravidelná kontrola a aktualizácia zariadení a softvéru.
- **Bezpečnosť**: Pravidelné zálohovanie konfigurácií, aktualizácie bezpečnostných opatrení.

## Logická schéma siete

Zobrazuje logické prepojenie zariadení a sieťové vrstvy, vrátane IP adresovania, VLAN a smerovacích protokolov.

**Konfigurácie zariadení**:
- **Switche**: Nastavenie VLAN, trunk portov, QoS.
- **Routery**: Smerovacie protokoly (OSPF, BGP), NAT, ACL.
- **Firewally**: Pravidlá pre prístup, VPN nastavenia.
- **AP**: SSID, bezpečnostné protokoly (WPA2, WPA3).

## Zálohovanie a udržovanie dokumentácie v aktuálnom stave pri prevádzke

**Zálohovanie**:

- **Konfigurácie zariadení**: Pravidelné zálohovanie konfiguračných súborov routerov, switchov, firewallov.
- **Dáta**: Pravidelné zálohovanie dôležitých dát na serveroch a pracovných staniciach, implementácia redundancie.

**Udržovanie dokumentácie**:

- **Aktualizácie**: Pravidelná aktualizácia sieťovej dokumentácie, vrátane fyzického a logického usporiadania.
- **Nástroje**: Používanie softvéru na správu dokumentácie a verzionovanie (napr. Git).
- **Audit**: Pravidelné audity na overenie správnosti a aktuálnosti dokumentácie.