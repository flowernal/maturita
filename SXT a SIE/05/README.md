# Zadanie
pojem a princíp fungovania dynamických smerovacích protokolov, rozdiely medzi charakteristikami  classless - classful, IGRP - EGRP, distance-vector - link-state, fast - slow convergence, charakteristiky protokolov RIP a OSPF

## pojem a princíp fungovania dynamických smerovacích protokolov
Dynamické smerovacie protokoly sú základným prvkom moderných sieťových infraštruktúr, ktoré umožňujú smerovačom automaticky určiť najefektívnejšiu cestu pre prenos dát medzi rôznymi sieťovými uzlami. Na rozdiel od statických smerovacích protokolov, ktoré vyžadujú manuálnu konfiguráciu smerovacích tabuliek, dynamické protokoly dokážu automaticky reagovať na zmeny v sieti, ako sú výpadky, preťaženie alebo zmeny topológie. Tieto protokoly sú nevyhnutné pre udržanie vysokého výkonu a spoľahlivosti v komplexných a rýchlo sa meniacich sieťových prostrediach.

## Classful Routing Protokoly

Classful routing protokoly pracujú so sieťovými adresami, ktoré sú definované podľa tried (A, B, C). Typickými príkladmi classful protokolov sú RIP v1 a IGRP. Hlavné charakteristiky classful protokolov sú:

    1. Pevne dané masky podsietí:
        Classful protokoly neodovzdávajú informácie o maskách podsietí spolu s IP adresami.
        Siete sú identifikované na základe tried (A, B, C) a majú preddefinované masky (napr. trieda A má masku 255.0.0.0).

    2. Nepodpora variabilnej dĺžky masky podsietí (VLSM):
        Nie je možné používať rôzne masky podsietí v rámci tej istej siete.

    3. Zmenšovanie IP priestoru:
        Pevne dané masky podsietí často vedú k neefektívnemu využívaniu IP priestoru, pretože sieť môže obsahovať oveľa viac IP adries, než je potrebné.

    4. Nekompatibilita so súhrnným smerovaním (CIDR):
        Classful protokoly nedokážu využívať súhrnné smerovanie, čo môže viesť k väčšiemu počtu záznamov v smerovacích tabuľkách a k zníženej efektivite smerovania.

## Classless Routing Protokoly

Classless routing protokoly, ako sú RIP v2, OSPF, EIGRP a BGP, umožňujú flexibilnejšie a efektívnejšie smerovanie tým, že podporujú variabilné dĺžky masiek podsietí (VLSM) a CIDR. Hlavné charakteristiky classless protokolov sú:

    1. Podpora masky podsietí:
        Classless protokoly prenášajú informácie o maske podsietí spolu s IP adresami.
        To umožňuje presnejšie určenie veľkosti siete a lepšie využitie IP priestoru.

    2. Variabilná dĺžka masky podsietí (VLSM):
        Umožňuje použitie rôznych masiek podsietí v rámci tej istej siete.
        Zvyšuje flexibilitu pri plánovaní sietí a umožňuje prispôsobenie veľkosti podsietí podľa konkrétnych potrieb.

    3. Efektívne využitie IP priestoru:
        Vďaka VLSM je možné lepšie využiť dostupné IP adresy a minimalizovať ich plytvanie.

    4. Podpora súhrnného smerovania (CIDR):
        Classless protokoly podporujú súhrnné smerovanie, čo vedie k zníženiu počtu záznamov v smerovacích tabuľkách a zlepšeniu efektivity smerovania.

## IGRP - EIGRP
IGRP a EIGRP sú obidva proprietárne protokoly od Cisco, pričom EIGRP je vylepšená verzia IGRP s rýchlejšou konvergenciou a podporou modernejších technológií ako VLSM a CIDR. 

**IGRP**:
    - Typ protokolu: Distance-vector.
    - Konvergencia: Pomalšia.
    - Smerovacie metriky: Šírka pásma, oneskorenie, spoľahlivosť, zaťaženie, MTU.
    - Podpora VLSM/CIDR: Nie.
    - Maximálny počet skokov: 255.
    - Zabezpečenie: Žiadne moderné mechanizmy.
    - Štandardizácia: Proprietárny protokol Cisco.

**EIGRP**:
    - Typ protokolu: Hybridný (kombinácia distance-vector a link-state).
    - Konvergencia: Rýchla.
    - Smerovacie metriky: Šírka pásma, oneskorenie, spoľahlivosť, zaťaženie, MTU.
    - Podpora VLSM/CIDR: Áno.
    - Maximálny počet skokov: 224.
    - Zabezpečenie: Moderné mechanizmy autentifikácie.
    - Štandardizácia: Proprietárny protokol Cisco.

## RIP - OSPF
RIP je jednoduchý distance-vector protokol vhodný pre malé siete s obmedzenou škálovateľnosťou, zatiaľ čo OSPF je robustný link-state protokol vhodný pre veľké a komplexné siete s rýchlou konvergenciou a vynikajúcou škálovateľnosťou.

**RIP**:

    - Typ protokolu: Distance-vector.
    - Konvergencia: Pomalá.
    - Maximálny počet skokov: 15.
    - Smerovacie metriky: Počet skokov.
    - Podpora VLSM/CIDR: RIP v1 nie, RIP v2 áno.
    - Štandardizácia: Otvorený štandard.

**OSPF**:

    - Typ protokolu: Link-state.
    - Konvergencia: Rýchla.
    - Smerovacie metriky: Cost (založený na šírke pásma).
    - Podpora VLSM/CIDR: Áno.
    - Štandardizácia: Otvorený štandard.
    - Škálovateľnosť: Vysoká, vďaka hierarchickému smerovaniu.