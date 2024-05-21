# Zadanie

- delenie útokov na generické siete
- princíp útoku MitM a DoS
- pojmy botnet, social engineering, phishing

# Vypracovanie

## Delenie útokov na generické siete

### Malware útoky

Môže infikovať siete prostredníctvom škodlivých programov, ako sú vírusy, červy, trojské kone, alebo ransomware. Tieto programy môžu spôsobiť škody tým, že kradnú údaje, poškodia systémy alebo ich ukrývajú, alebo požadujú výkupné za obnovenie prístupu k dátam.

Keď sa malware dostane do počítača, môže spôsobiť niekoľko druhov škôd:

- Spyware ukradne údaje a pošle ich späť autorom malweru. Bežnou formou spyware sú keyloggery, programy, ktoré sledujú všetko, čo používateľ napíše, vrátane ich hesiel.
- Adware zobrazuje vyskakovacie reklamy, tento malware obvykle vydáva peniaze autorom.
- Ransomware (zašifruje užívateľské dáta alebo blokuje prístup ku aplikáciám a žiada užívateľa, aby zaplatil výkupné anonymným autorom.
- Malware pre ťažbu kryptomien zneužíva počítač na ťažbu. To tvorcom umožňuje získavať kryptomenu bez výdavkov na prevádzku vlastných počítačov.

### DNS Poisoning

Pomocou tejto metódy môžu hackeri oklamať DNS server ľubovoľného počítačač, aby považoval falošné dáta za reálne a overené. Tieto falošné informácie sú uložené vo vyrovnávacej pamäti po určitú dobu, za túto dobu hacker prepíše DNS odpovede z IP adries. Výsledkom je, že používatelia, ktorí chcú pristupovať na danú webovú stránku, sťahujú vírusy namiesto originálneho obsahu.

<img src="https://github.com/flowernal/maturita/blob/main/SXT%20a%20SIE/09/09%20d14daed486e14d14bc0f469b41408dd3/Untitled.png" width="500">

## Princíp útoku MitM a DoS

### MitM (Man In The Middle)

Je označenie pre druh útoku na bezpečnosť používateľa, pri ktorom útočník potajomky zasahuje do komunikácie medzi dvoma subjektmi a to tak aby verili že komunikujú spolu. V skutočnosti je komunikácia riadená útočníkom uprostred - preto ten názov **Man In The Middle**. Cieľom MitM útokov je získanie možnosti čítať, kontrolovať, vkladať vlastné, alebo modifikovať existujúce informácie v rámci komunikácia dvoch strán.

MITM útok je veľmi zákerný, pretože z pohľadu užívateľa je veľmi zle rozoznateľný. Jedna z foriem útočí na sieťovú infraštruktúru, pri ktorej sa útočník sústredí na káble, bezdrôtovú komunikáciu alebo nejaký aktívny sieťový prvok. Útočník v takom prípade buď preruší káble alebo iné sieťové zariadenie a vloží tam vlastné zariadenie ktoré umožňuje odpočúvať a narušovať komunikáciu.

**Ako zabrániť MitM útokom?**

Z pohľadu komunikácie je určite dobré využívať šifrovanú komunikáciu HTTPS so silnou šifrou. Pre firmy je dôležité mať chránenú sieť proti vniknutiu. Ak sa odpočúvanie deje na sieti, a komunikácia nie je vôbec šifrovaná, tak používatelia nemajú ani najmenšiu šancu. Z pohľadu zariadenie je dôležité neinštalovať podozrivé aplikácie a používať antivírusové programy iba preverených spoločností.

<img src="https://github.com/flowernal/maturita/blob/main/SXT%20a%20SIE/09/09%20d14daed486e14d14bc0f469b41408dd3/Untitled%201.png" width="500">

### DDoS (**Distributed denial-of-Service)**

DDoS útok záplavou požiadaviek preťaží webový server s väčším množstvom požiadaviek, než aké môže zvládnuť. To preťaží server tak, že následne nie je schopný reagovať na požiadavky bežných používateľov, výrazne spomalí webovú stránku alebo ju spraví nedostupnou.

<img src="https://github.com/flowernal/maturita/blob/main/SXT%20a%20SIE/09/09%20d14daed486e14d14bc0f469b41408dd3/Untitled%202.png" width="500">

## Pojmy Botnet, Social engineering a phishing

### Botnet

Botnet je sieť počítačov alebo zariadení, ktoré boli infikované škodlivým softvérom a prevzaté pod kontrolu útočníka. Tieto infikované zariadenia môžu byť vzdialene riadené cez príkazy od centrálneho servera. Botnety sa často používajú na vykonávanie škodlivých aktivít, ako sú DoS útoky, šírenie spamu, ťažba kryptomeny, špionáž alebo krádež údajov. Veľkosť botnetu môže byť od niekoľkých desiatok počítačov až po státisíce alebo dokonca milióny infikovaných zariadení. Tieto botnety môžu byť veľmi ťažko odhaliteľné a zastaviteľné, čo ich robí obľúbeným nástrojom pre kybernetických útočníkov.

Pre zaujímavosť najväčším botnetom doteraz bol Conficker, ktorý ovládal 10,5 milióna počítačov.

<img src="https://github.com/flowernal/maturita/blob/main/SXT%20a%20SIE/09/09%20d14daed486e14d14bc0f469b41408dd3/Untitled%203.png" width="500">

### Social engineering

Jedným z najefektívnejších nástrojov pre získavanie citlivých informácií zo zabezpečených systémov je social engineering. Nevyžaduje takmer žiadne technické schopnosti a napriek tomu je s jeho využitím možné infikovať informácie aj z technicky dobre zabezpečených informačných systémov. Je to možné vďaka tomu, že sa tento typ útoku zameriava práve na samotného človeka.
Zameriavajú na manipuláciu bežných spôsobov ľudského chovania a existuje len obmedzená množina technických opatrení na ochranu pred týmito útokmi. Najlepším spôsobom ochrany je zvyšovanie bezpečnostného povedomia o jednotlivých technikách social engineeringu.
Základ social engineeringu je dôvera. Hacker si u človeka vybuduje dôveru a následne ju využije.
Na to, aby obeť zmanipuloval, potrebuje útočník falošný príbeh alebo zámienku, ktorú je možné vytvoriť s pomocou verejne dostupných informácií o organizácii a následné zneužiť vlastnosti obete, ku ktorým patrí ochota pomáhať, slabé povedomie o hrozbách na internete, slabé povedomie o bezpečnostných zásadách organizácie, prípadne umiestňovanie citlivých informácií na sociálne média.

### Phishing

Phishing je to keď útočníci sa vydávajú za dôveryhodné osoby alebo organizácie prostredníctvom e-mailov,správ alebo webových stránok s cieľom získať citlivé informácie, ako napríklad prihlasovacie údaje, heslá alebo finančné údaje.

Spearphishing je sofistikovanejšia metóda neoprávneného získavania údajov, pri ktorej je útok zameraný na konkrétne skupiny, organizácie alebo dokonca jednotlivcov. Autori spearphishingových e-mailov si o svojich cieľoch vždy najskôr spravia podrobný prieskum, na základe ktorého pripravia hodnoverne vyzerajúci e-mail s takým obsahom, ktorý obeť len ťažko odhalí ako podvodný.

**Ako rozpoznať phising?**

Všeobecné alebo neformálne oslovenia, žiadosť o osobné informácie, dotyčný má slabú jazykovú úroveň, dávajú pocit naliehavosti, podozrivá doména.
