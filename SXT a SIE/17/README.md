# Zadanie

- typy, vlastnosti a možnosti prístupových povolení súborových systémov používaných vo Windows
- typy, vlastnosti a možnosti prístupových povolení súborových systémov používaných v Linuxe
- príkazy pre prácu so súborovým systémom Linux
- príkazy pre prácu s partíciami v systéme Linux
- využívanie súborových systémov mimo PC a ich vlastnosti

# Vypracovanie

## Windows filesystémy

### Typy súborových systémov

- **FAT32**: Starší súborový systém, podporuje maximálnu veľkosť súboru 4 GB a veľkosť oddielu 8 TB, často používaný na USB kľúče a pamäťové karty kvôli svojej širokej kompatibilite.

- **NTFS** (New Technology File System): Moderný súborový systém s podporou veľkých súborov a diskových oddielov, poskytuje pokročilé funkcie ako šifrovanie, kompresiu, a správu prístupových práv.
- **exFAT** (Extended File Allocation Table): Navrhnutý pre flash pamäte, prekonáva obmedzenia FAT32, podporuje väčšie súbory a oddiely bez pokročilých funkcií NTFS.

### Vlastnosti

- **FAT32**: Jednoduchý a rýchly, ale bez pokročilých funkcií bezpečnosti a s obmedzením veľkosti súborov.

- **NTFS**: Podpora veľkých súborov a diskov, pokročilé bezpečnostné funkcie, spoľahlivosť a efektívnosť ukladania.
- **exFAT**: Kombinuje jednoduchý dizajn FAT32 s podporou veľkých súborov, ideálny pre prenosné úložiská.

### Možnosti prístupových povolení

- **NTFS**: Podporuje prístupové práva na úrovni súborov a priečinkov (čítanie, zápis, spúšťanie), šifrovanie pomocou EFS (Encrypting File System), a nastavenie kvót pre užívateľov.

- **FAT32** a **exFAT**: Nepodporujú prístupové práva a bezpečnostné funkcie, vhodné len pre základné úložiská bez potreby pokročilej bezpečnosti.

## Linux filesystémy

### Typy súborových systémov

- **ext4** (Fourth Extended Filesystem): Najpoužívanejší súborový systém pre Linux, ponúka vysoký výkon, spoľahlivosť a podporu veľkých súborov.

- **Btrfs** (B-tree File System): Moderný súborový systém s pokročilými funkciami ako snapshoty, zrkadlenie a kontrola integrity dát.
- **XFS**: Vysoko škálovateľný súborový systém vhodný pre veľké súbory a systémy s vysokým výkonom.
- **F2FS** (Flash-Friendly File System): Optimalizovaný pre flash pamäte, ako sú SSD a eMMC.

### Vlastnosti

- **ext4**: Rýchle prístupové časy, žurnálovanie, kontrola integrity dát, podpora súborov až do veľkosti 16 TB.

- **Btrfs**: Pokročilé funkcie správy úložiska, dynamická defragmentácia, snapshoty a kontrola integrity dát.
- **XFS**: Vysoká škálovateľnosť, efektívnosť správy veľkých súborov, robustnosť a rýchle obnovenie po zlyhaní.
- **F2FS**: Optimalizovaný pre minimalizáciu opotrebenia flash pamätí, zvyšuje výkon a životnosť SSD.

### Možnosti prístupových povolení

- **UNIX-ové povolenia**: Užívatelia a skupiny s právami čítania, zápisu a spúšťania pre súbory a priečinky. (rwx)

- **ACLs** (Access Control Lists): Umožňujú detailnejšiu správu prístupových práv, umožňujú nastaviť práva pre jednotlivých užívateľov a skupiny.
- **SELinux** (Security-Enhanced Linux) a **AppArmor**: Poskytujú dodatočné vrstvy bezpečnostných politík na základe kontextu a politiky prístupu.

## Príkazy pre prácu so súborovým systémom Linux

- **ls**: Zobrazenie obsahu adresára.
  - `ls -l`: Podrobný výpis súborov s právami.
- **cd**: Zmena aktuálneho adresára.
  - `cd /path/to/directory`: Prechod do zadaného adresára.
  - `cd`: Prechod do domovského adresára.
- **mkdir**: Vytvorenie nového adresára.
  - `mkdir new_directory`: Vytvorí adresár new_directory.
- **rm**: Odstránenie súborov alebo adresárov.
  - `rm file`: Odstráni súbor file.
  - `rm -r directory`: Rekurzívne odstráni adresár directory.
- **cp**: Kopírovanie súborov alebo adresárov.
  - `cp source destination`: Skopíruje súbor source na destination.
  - `cp -r source_dir destination_dir`: Rekurzívne skopíruje adresár source_dir na destination_dir.
- **mv**: Premiestnenie alebo premenovanie súborov alebo adresárov.
  - `mv old_name new_name`: Premenuje súbor alebo adresár old_name na new_name.
  - `mv file /path/to/directory`: Premiestni súbor file do zadaného adresára.
- **chmod**: Zmena prístupových práv súborov alebo adresárov.
  - `chmod 755 file`: Nastaví prístupové práva súboru file.
- **chown**: Zmena vlastníka súborov alebo adresárov.
  - `chown user:group file`: Nastaví vlastníka user a skupinu group pre súbor file.

## Príkazy pre prácu s partíciami v systéme Linux

- **fdisk**: Nástroj na manipuláciu s diskovými oddielmi.
  - `fdisk /dev/sda`: Otvorí disk /dev/sda pre úpravy.
- **parted**: Pokročilý nástroj na manipuláciu s diskovými oddielmi.
  - `parted /dev/sda`: Otvorí disk /dev/sda pre úpravy.
- **mkfs**: Vytvorenie súborového systému na oddieli.
  - `mkfs.ext4 /dev/sda1`: Vytvorí ext4 súborový systém na oddieli /dev/sda1.
- **mount**: Pripojenie súborového systému.
  - `mount /dev/sda1 /mnt`: Pripojí oddiel /dev/sda1 do adresára /mnt.
- **umount**: Odpojenie súborového systému.
  - `umount /mnt`: Odpojí súborový systém pripojený do adresára /mnt.
- **lsblk**: Zobrazenie informácií o blokových zariadeniach.
  - `lsblk`: Zobrazí zoznam všetkých blokových zariadení a ich oddielov.
- **df**: Zobrazenie informácií o využití diskového priestoru.
  - `df -h`: Zobrazí informácie o využití diskového priestoru v ľahko čitateľnom formáte.

## Využívanie súborových systémov mimo PC a ich vlastnosti

- **NAS** (Network Attached Storage): Používa súborové systémy ako ext4, Btrfs, ZFS, určené pre ukladanie dát a ich zdieľanie cez sieť, ponúkajú funkcie ako snapshoty, RAID, a kontrolu integrity dát.

- **SAN** (Storage Area Network): Používa súborové systémy ako NTFS, ext4, VMFS, ktoré umožňujú rýchly a spoľahlivý prístup k veľkým objemom dát, často používané v podnikových prostrediach.
- **SD karty a USB kľúče**: Bežne používajú súborové systémy FAT32 a exFAT, ktoré sú kompatibilné s mnohými zariadeniami vrátane fotoaparátov, smartfónov a multimediálnych prehrávačov.
- **Smartfóny a tablety**: Používajú súborové systémy ako ext4, F2FS (pre Android) alebo APFS (pre iOS), optimalizované pre rýchly prístup a správu dát na flash pamätiach.
- **Cloudové úložiská**: Používajú distribuované súborové systémy ako HDFS (Hadoop Distributed File System) alebo CephFS, ktoré umožňujú škálovateľné a redundantné ukladanie dát v distribuovanom prostredí.