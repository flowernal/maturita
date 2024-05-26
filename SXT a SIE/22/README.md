# Zadanie

- BIOS, UEFI, POST, MBR, GPT
- účel boot loadera, uveďte názvy používaných vo Windows a v Linuxe
- proces spustenia PC od zapnutia po načítanie operačného systému Linux
- bootloader grub

# Vypracovanie

## BIOS, UEFI, POST, MBR, GPT

**BIOS (Basic Input/Output System)**

- **Definícia**: Starší firmvér používaný na inicializáciu hardvéru a načítanie zavádzača operačného systému.
- **Funkcie**: Testovanie a inicializácia hardvéru (POST), nastavenie systémových parametrov, načítanie boot sektora.

**UEFI (Unified Extensible Firmware Interface)**

- **Definícia**: Modernejší firmvér, ktorý nahrádza BIOS a poskytuje viac funkcionality a lepšiu podporu pre veľké disky a bezpečnostné funkcie.
- **Funkcie**: Inicializácia hardvéru, správna bezpečnosť (Secure Boot), rýchlejšie bootovanie, podpora pre GPT.

**POST (Power-On Self Test)**

- **Definícia**: Proces, ktorý prebieha po zapnutí počítača a kontroluje základnú funkčnosť hardvéru.
- **Funkcie**: Skontroluje pamäť, procesor, grafiku, klávesnicu a ďalšie základné komponenty, hlási chyby ak sa nájdu.

**MBR (Master Boot Record)**

- **Definícia**: Tradičný formát tabuľky rozdelenia oddielov na pevných diskoch, obsahuje zavádzač a tabuľku rozdelenia disku.
- **Vlastnosti**: Podpora pre disky do 2 TB, limit 4 primárne oddiely.

**GPT (GUID Partition Table)**

- **Definícia**: Modernejší formát tabuľky rozdelenia diskov, ktorý prekonáva limity MBR.
- **Vlastnosti**: Podpora pre disky väčšie ako 2 TB, neobmedzený počet oddielov (teoreticky), lepšia redundancia a zotavenie z chýb.

## Boot loader

- **Definícia**: Softvér, ktorý načíta a spustí operačný systém pri štarte počítača.
- **Funkcie**: Inicializuje operačný systém, môže ponúknuť výber medzi viacerými OS, poskytuje parametre na zavedenie systému.

**Názvy boot loaderov**:

- **Windows**: Windows Boot Manager (BOOTMGR).
- **Linux**: GRUB (GRand Unified Bootloader), LILO (LInux LOader).

## Proces spustenia PC od zapnutia po načítanie operačného systému Linux

1. **Zapnutie počítača**:
   - Napájanie sa zapne, základná doska a ďalšie komponenty dostanú energiu.
2. **POST (Power-On Self Test)**:
   - BIOS alebo UEFI vykoná základné testy hardvéru, ako je kontrola RAM, procesora a ďalších komponentov.
3. **Inicializácia firmvéru (BIOS/UEFI)**:
   - BIOS alebo UEFI vyhľadá a načíta boot loader z určeného boot zariadenia (pevný disk, SSD, USB).
4. **Boot loader**:
   - Boot loader (napr. GRUB) sa načíta do pamäte a zobrazí boot menu (ak je dostupné).
   - Boot loader načíta jadro Linuxu (kernel) a initramfs (initial RAM filesystem).
5. **Kernel loading**:
   - Jadro sa načíta do pamäte a inicializuje hardvér, mountuje **initramfs** a vykonáva základné nastavenia systému.
6. **Init system (Systemd alebo iný)**:
   - Kernel prevezme kontrolu a spustí init systém (napr. systemd), ktorý načíta a spustí potrebné systémové služby a démony.
7. **Načítanie operačného systému**:
   - Init systém spustí potrebné služby, mountuje súborové systémy a pripraví prostredie pre užívateľa.
   - Na konci tohto procesu sa spustí login manager alebo príkazový riadok pre prihlásenie používateľa.

## Bootloader GRUB

**GRUB** (GRand Unified Bootloader) je flexibilný a výkonný boot loader používaný v mnohých Linuxových distribúciách.

**Vlastnosti**:

- **Podpora viac OS**: Môže načítať a zaviesť viacero operačných systémov.
- **Konfigurovateľnosť**: Konfiguračný súbor `/etc/grub2/grub.cfg` alebo `/boot/grub/grub.cfg` umožňuje pridať rôzne voľby a parametre zavádzania.
- **Interaktivita**: Poskytuje boot menu a príkazový riadok na úpravu parametrov zavádzania v reálnom čase.
- **Modularita**: Podporuje moduly, ktoré môžu byť dynamicky načítané na rozšírenie funkcionality.
- **Verzie**: GRUB Legacy (staršia verzia) a GRUB 2 (novšia verzia s vylepšenou funkcionalitou a podporou).
