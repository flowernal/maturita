# Zadanie

Pojem súbor, zápis a čítanie zo súboru, základné kroky pri práci so súborom,  použitie triedy File, PrintWriter a Scaner, význam blokov try a catch.

# Vypracovanie

## Zápis a čítanie zo súboru

### Základné kroky

1. **Otvorenie súboru:** Na začiatku musíme súbor otvoriť. To sa robí pomocou triedy `File`, ktorá predstavuje súbor alebo adresár na disku.
2. **Zápis:** Po otvorení súboru môžeme použiť triedu `PrintWriter` na zápis údajov do súboru.
3. **Čítanie:** Pre čítanie zo súboru používame triedu `Scanner`, ktorá umožňuje jednoduché a efektívne čítanie dát.

### Príklad zápisu do súboru

```java
import java.io.*;

public class WriteToFileExample {
    public static void main(String[] args) {
        try {
            PrintWriter writer = new PrintWriter("output.txt");
            writer.println("Hello, world!");
            writer.close();
            System.out.println("Zápis do súboru bol úspešný.");
        } catch (IOException e) {
            System.out.println("Nastala chyba pri zápise do súboru: " + e.getMessage());
        }
    }
}
```

### Príklad čítania zo súboru

```java
import java.io.*;

public class ReadFromFileExample {
    public static void main(String[] args) {
        try {
            File file = new File("input.txt");
            Scanner scanner = new Scanner(file);
            while (scanner.hasNextLine()) {
                String data = scanner.nextLine();
                System.out.println(data);
            }
            scanner.close();
        } catch (FileNotFoundException e) {
            System.out.println("Súbor sa nenašiel: " + e.getMessage());
        }
    }
}
```

## Bloky try a catch

Pri práci so súbormi je dôležité ošetriť možné výnimky. Na to slúžia bloky `try` a `catch`, ktoré zachytávajú a spracúvajú výnimky, ktoré môžu vzniknúť počas práce so súbormi.

```java
try {
    // blok kódu, v ktorom môže vzniknúť výnimka
} catch (IOException e) {
    // ošetrenie výnimky
    System.out.println("Nastala chyba pri práci so súborom: " + e.getMessage());
}
```

Takto zachytené výnimky umožňujú aplikácii elegantne reagovať na nečakané udalosti a zabraňujú pádu programu.