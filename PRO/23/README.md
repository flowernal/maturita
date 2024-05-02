# Zadanie

Pojem reťazec, konkrétne príklady vytvorenia reťazca, rozdiel medzi triedou String a StringBuffer, príkazy požívané pri práci s reťazcami.

# Vypracovanie

## Pojem reťazec:
Reťazec v programovaní je postupnosť znakov. V Jave je reprezentovaný triedou `String` a slúži na prácu s textom.

## Konkrétne príklady vytvorenia reťazca:
```java
// Vytvorenie reťazca pomocou literálu
String text1 = "Hello, world!";

// Vytvorenie reťazca pomocou konštruktora triedy String
String text2 = new String("Hello, world!");

// Vytvorenie prázdneho reťazca
String emptyString = "";

// Vytvorenie reťazca z poľa znakov
char[] chars = {'H', 'e', 'l', 'l', 'o'};
String text3 = new String(chars);
```

## Rozdiel medzi triedou String a StringBuffer:
- **String**: Objekty typu `String` sú nemenné, čo znamená, že ich hodnota nemôže byť zmenená po vytvorení. Ak sa reťazec zmení, vytvorí sa nový objekt.
- **StringBuffer**: Objekty typu `StringBuffer` sú modifikovateľné, čo znamená, že ich hodnota môže byť zmenená. `StringBuffer` je vhodný pre prípady, keď sa reťazec často mení, pretože modifikácie sú efektívnejšie ako v prípade triedy `String`.

## Príkazy používané pri práci s reťazcami:
- **concat()**: Slúži na zlúčenie dvoch reťazcov.
- **length()**: Vráti dĺžku reťazca.
- **charAt()**: Vráti znak na zadanom indexe.
- **substring()**: Vráti podreťazec.
- **equals()**: Porovnáva dva reťazce na rovnosť obsahu.
- **toUpperCase()**: Vráti reťazec s veľkými písmenami.
- **toLowerCase()**: Vráti reťazec s malými písmenami.
- **indexOf()**: Vráti index prvého výskytu podreťazca.
- **replace()**: Nahradí všetky výskyty zadaného reťazca iným reťazcom.
