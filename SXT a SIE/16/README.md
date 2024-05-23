# Zadanie

- parametre procesorov architektúry x86 a príklady označenia typov
- iné architektúry a názvy procesorov
- parametre operačných pamätí pre PC a notebooky

# Vypracovanie

## Procesory x86

### Parametre

- **Počet jadier a vlákien**:
  - *Jadrá*: Fyzické jednotky, ktoré vykonávajú úlohy.
  - *Vlákna*: Logické jednotky, ktoré môžu spracovávať paralelné úlohy na každom jadre (Hyper-Threading).
- **Taktovacia frekvencia**:
  - Meraná v GHz (gigahertz).
  - Určuje rýchlosť spracovania inštrukcií.
- **Cache pamäť**:
  - L1, L2, a L3 cache.
  - Slúži na dočasné ukladanie často používaných dát pre rýchlejší prístup.
- **TDP** (Thermal Design Power):
  - Udáva maximálny tepelný výkon, ktorý procesor vyžaruje.
  - Vyjadrené vo wattoch (W).
- **Výrobné technológie**:
  - 3nm (Apple M3) 7nm , 10nm, 14nm procesory.
  - Menšie číslo znamená vyššiu hustotu tranzistorov a často lepšiu energetickú efektivitu.
- **Podpora inštrukčných sád**:
  - SSE, AVX, AVX2, AVX-512.
  - Dodatočné inštrukcie pre špecifické výpočtové úlohy.
- **Podpora pamäťových typov**:
  - DDR4, DDR5.
  - Maximálna podporovaná kapacita a rýchlosť.
- **Integrovaná grafika** (ak je prítomná):
  - Typ a výkon iGPU.
  - Podpora pre video výstupy a dekódovanie.

### Príklady označenia

**Intel Core**:

- Intel Core i3-14100: 4 jadrá, 8 vlákien, 3.5 GHz (base), 4.7 GHz (boost), 12 MB L3 cache, 110W TDP.
- Intel Core i5-14600K: 14 jadier, 20 vlákien, 3.5 GHz (base), 5.3 GHz (boost), 24 MB L3 cache, 181W TDP.
- Intel Core i7-14700K: 20 jadier, 28 vlákien, 3.4 GHz (base), 5.6 GHz (boost), 33 MB L3 cache, 253W TDP.
- Intel Core i9-14900K: 24 jadier, 32 vlákien, 3.2 GHz (base), 6 GHz (boost), 36 MB L3 cache, 253W TDP.

**AMD Ryzen**:

- AMD Ryzen 3 3300X: 4 jadrá, 8 vlákien, 3.8 GHz (base), 4.3 GHz (boost), 16 MB L3 cache, 65W TDP.
- AMD Ryzen 5 7600X: 6 jadier, 12 vlákien, 4.7 GHz (base), 5.3 GHz (boost), 32 MB L3 cache, 105W TDP.
- AMD Ryzen 7 7800X3D: 8 jadier, 16 vlákien, 4.2 GHz (base), 5 GHz (boost), 96 MB L3 cache, 120W TDP.
- AMD Ryzen 9 7900X: 12 jadier, 24 vlákien, 4.7 GHz (base), 5.6 GHz (boost), 64 MB L3 cache, 170W TDP.

## Iné architektúry

**ARM** (Advanced RISC Machine):

- ARM Cortex-A78: Používaný v high-end mobilných zariadeniach.
- Apple M3: Používaný v Apple MacBookoch, Macoch a iPadoch, 8 jadier, vysoká energetická efektivita.

**PowerPC**:

- Používané v starších Apple počítačoch a v herných konzolách ako PS3 a Xbox 360.
- IBM Power9: Používané v high-performance serveroch a superpočítačoch.

**RISC-V**:

- Open-source architektúra.
- Používaná vo výskume a v niektorých embedded systémoch.
  
**SPARC** (Scalable Processor Architecture):

- Používané v serveroch a superpočítačoch, vyvinuté spoločnosťou Sun Microsystems.
- Oracle SPARC M8: Používané v high-end serverových aplikáciách.

## Parametre operačných pamätí

**Typy pamäte**:

- Double Data Rate - DDR3, DDR4, DDR5, LPDDR5 (Low Power)...
- Každá nasledujúca generácia prináša vyššiu rýchlosť a efektivitu.

**Kapacita**:

- Udáva sa v GB (gigabajty).
- Bežne dostupné kapacity sú od 4 GB do 128 GB.

**Rýchlosť**:

- Udáva sa v MHz (megahertz), respektíve MT (megatransfer).
- Napríklad 2400 MHz, 3200 MHz, 3600 MHz.

**CAS Latency (CL)**:

- Časový interval medzi zadávaním príkazu a vykonaním operácie.
- Nižšie CL hodnoty znamenajú rýchlejšiu pamäť.

**Napätie**:

- Bežne 1.2V pre DDR4, 1.1V pre DDR5.
- Nižšie napätie znamená vyššiu energetickú efektivitu.

**Form factor**:

- DIMM (Dual Inline Memory Module) pre stolné počítače.
- SO-DIMM (Small Outline DIMM) pre notebooky.

**ECC** (Error-Correcting Code):

- Používa sa v serveroch pre zvýšenú spoľahlivosť.
- Dokáže detekovať a opraviť chyby v pamäťových dátach.