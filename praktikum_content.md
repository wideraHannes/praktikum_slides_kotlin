# Einführung in die Programmierung

## Am Beispiel Kotlin

---

<!-- ============================================================ -->
<!-- TEIL 1 — THEORIE: WAS IST PROGRAMMIERUNG?                     -->
<!-- ============================================================ -->

# 📘 Teil 1 — Was ist Programmierung?

---

## Was ist Programmierung?

## Wo steckt überall Programmierung drin?

| Bereich  | Beispiele                                 |
| -------- | ----------------------------------------- |
| Apps     | Instagram, WhatsApp, TikTok               |
| Websites | YouTube, Google, Wikipedia                |
| Spiele   | Minecraft, Fortnite, FIFA                 |
| Geräte   | Roboter, Drohnen, Smartwatches            |
| Autos    | Autopilot, Einparkhilfe                   |
| KI       | ChatGPT, Bilderkennung, Sprachassistenten |

Praktisch alles, was einen Bildschirm hat (und vieles ohne), wird programmiert.

---

## Welche Programmiersprachen gibt es?

Hunderte — jede hat ihren Einsatzbereich:

| Sprache    | Typischer Einsatz                       |
| ---------- | --------------------------------------- |
| Python     | KI, Data Science, Automatisierung       |
| JavaScript | Websites, Web-Apps                      |
| Java       | Große Unternehmenssoftware, Android     |
| **Kotlin** | **Android-Apps, Server, Multiplatform** |
| Swift      | iPhone-Apps                             |
| C / C++    | Betriebssysteme, Spiele-Engines         |
| C#         | Spiele (Unity), Windows-Software        |

Keine Sprache ist "die beste" — es kommt darauf an, **was** man bauen will.

---

## Was ist Kotlin?

- Moderne Sprache von **JetBrains** (seit 2016 stabil)
- Von **Google** als bevorzugte Sprache für Android empfohlen
- Läuft auf der **JVM** (Java Virtual Machine)
- Klare, lesbare Syntax — weniger Code, gleiches Ergebnis
- Name kommt von der **Insel Kotlin** bei St. Petersburg 🏝️

---

## Wo läuft Kotlin?

```
                    Kotlin-Code
                        |
                        ▼
                    Compiler
                   /    |    \
                  ▼     ▼     ▼
               JVM   Native  JavaScript
               |       |        |
           Android   iOS    Websites
           Server   Desktop  Browser
```

Kotlin ist **Multiplatform** — ein Code, viele Plattformen.

---

## Warum Kotlin für uns?

**Zum Lernen:**

- Einfach zu lesen und schreiben
- Sofort im Browser testbar → kein Setup
- Fehler werden früh erkannt

**In der echten Welt:**

- Offizielle Sprache für Android
- Google, Netflix, Amazon, Uber nutzen Kotlin
- Wächst stark — gute Jobchancen

**Alternativen:**

- Websites → JavaScript
- KI → Python
- iPhone-Apps → Swift
- 3D-Spiele → C# / C++

---

## Unser Werkzeug: Kotlin Playground

Direkt im Browser — kein Setup nötig:

### → play.kotlinlang.org

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

Jedes Kotlin-Programm startet in der `main()` Funktion.

Alles was zwischen `{` und `}` steht, wird ausgeführt.

---

<!-- ============================================================ -->
<!-- TEIL 2 — THEORIE: GRUNDLAGEN                                  -->
<!-- ============================================================ -->

# 📘 Teil 2 — Kotlin Grundlagen

---

## `println` — Ausgabe

Mit `println()` gibst du Werte auf der Konsole aus.

```kotlin
println("Hallo Welt!")    // Text
println(42)               // Zahl
println(3 + 4)            // Berechnung → 7
```

`println` = **print line** → gibt eine Zeile aus.

---

## Variablen — Werte speichern

Variablen = **beschriftete Boxen** für Werte.

```kotlin
var punkte = 0            // veränderbar
val name = "Kotlin"       // fest
```

| Keyword | Bedeutung        | Änderbar? |
| ------- | ---------------- | --------- |
| `var`   | **var**iable     | ✅ Ja     |
| `val`   | **val**ue (Wert) | ❌ Nein   |

```kotlin
punkte = 10       // ✅ geht (var)
name = "Java"     // ❌ geht nicht (val)
```

---

## Datentypen — Was kann in die Box?

```kotlin
val alter: Int = 16           // Ganzzahl
val groesse: Double = 1.75    // Kommazahl
val name: String = "Alex"     // Text
val cool: Boolean = true      // Wahr / Falsch
```

| Typ       | Was?          | Beispiele             |
| --------- | ------------- | --------------------- |
| `Int`     | Ganzzahl      | `0`, `42`, `-7`       |
| `Double`  | Kommazahl     | `3.14`, `1.75`        |
| `String`  | Text          | `"Hallo"`, `"Kotlin"` |
| `Boolean` | Wahr / Falsch | `true`, `false`       |

Kotlin erkennt den Typ meistens automatisch — man muss ihn nicht hinschreiben.

---

## String Templates

Mit `$` baust du Variablen in Text ein:

```kotlin
val name = "Alex"
val alter = 16

println("Ich heiße $name und bin $alter Jahre alt.")
// → Ich heiße Alex und bin 16 Jahre alt.
```

Für Berechnungen → geschweifte Klammern `${}`:

```kotlin
println("In 2 Jahren bin ich ${alter + 2}.")
// → In 2 Jahren bin ich 18.
```

---

## Mathematische Operationen

```kotlin
println(10 + 3)    // 13     Addition
println(10 - 3)    // 7      Subtraktion
println(10 * 3)    // 30     Multiplikation
println(10 / 3)    // 3      Division (Ganzzahl!)
println(10 % 3)    // 1      Modulo (Rest)
```

### Modulo `%` = Der Rest einer Division

```
15 % 5 = 0   → 15 ist durch 5 teilbar (kein Rest)
16 % 5 = 1   → Rest 1
```

Perfekt um zu prüfen: **"Ist eine Zahl durch X teilbar?"**

→ `zahl % X == 0`

---

## Vergleiche → `true` / `false`

```kotlin
println(6 > 7)     // false
println(6 < 7)     // true
println(6 == 6)    // true
println(6 != 7)    // true
```

| Operator | Bedeutung           |
| -------- | ------------------- |
| `==`     | ist gleich          |
| `!=`     | ist ungleich        |
| `>`      | größer als          |
| `<`      | kleiner als         |
| `>=`     | größer oder gleich  |
| `<=`     | kleiner oder gleich |

---

## `for`-Loop — Schleifen

Wiederholt Code eine bestimmte Anzahl von Malen:

```kotlin
for (i in 1..5) {
    println(i)
}
// → 1  2  3  4  5
```

| Syntax         | Ergebnis            |
| -------------- | ------------------- |
| `1..5`         | 1, 2, 3, 4, 5       |
| `1 until 5`    | 1, 2, 3, 4 (ohne 5) |
| `5 downTo 1`   | 5, 4, 3, 2, 1       |
| `1..10 step 2` | 1, 3, 5, 7, 9       |

---

## `if` / `else` — Entscheidungen

```kotlin
val alter = 16

if (alter >= 18) {
    println("Volljährig!")
} else {
    println("Noch nicht 18.")
}
```

**Mehrere Fälle mit `else if`:**

```kotlin
if (x == 120) {
    println("YAAAY!")
} else if (x == 5050) {
    println("So you've heard of GAUSS :)")
} else if (x == 6) {
    println("You are just getting started!")
} else {
    println("NOOOO!")
}
```

---

<!-- ============================================================ -->
<!-- 🎤 LIVE DEMO                                                  -->
<!-- ============================================================ -->

# 🎤 Live Demo

## Wir bauen zusammen ein kleines Programm!

→ Playground öffnen: **play.kotlinlang.org**

---

## 🎤 Live Demo — Was wir bauen

Schritt für Schritt im Playground:

**1. Ausgabe & Variablen**

```kotlin
fun main() {
    var x = 0
    println(x)
}
```

**2. Vergleiche**

```kotlin
    println(3 > 7)     // false
    println(3 < 7)     // true
```

**3. Mathe**

```kotlin
    println(6 / 7)     // 0 (Int!)
    println(6f / 7f)   // 0.857... (Float!)
    println(16 % 7)    // 2
```

---

## 🎤 Live Demo — For-Loop & Bedingungen

**4. For-Loop → Variable hochzählen**

```kotlin
    var x = 0
    for (i in 1..3) {
        x = x + i
    }
    println(x)     // → 6
```

**5. if / else if / else**

```kotlin
    if (x == 120) {
        println("YAAAY!")
    } else if (x == 5050) {
        println("So you've heard of GAUSS :)")
    } else if (x == 6) {
        println("You are just getting started!")
    } else {
        println("NOOOO!")
    }
```

💡 **Aufgabe an die Klasse:** Was muss der Loop sein, damit x = 120 rauskommt?

---

<!-- ============================================================ -->
<!-- 🖐️ HANDS-ON: SELBER AUSPROBIEREN                             -->
<!-- ============================================================ -->

# 🖐️ Hands-on

## Jetzt seid ihr dran — probiert selbst rum!

→ **play.kotlinlang.org**

Experimentiert mit `println`, Variablen, Operatoren, Schleifen, `if`/`else`.

Kaputt machen erlaubt — aus Fehlern lernt man am meisten! 💥

---

<!-- ============================================================ -->
<!-- 📋 CHEAT SHEET 1 — Bleibt offen!                              -->
<!-- ============================================================ -->

# 📋 Cheat Sheet — Grundlagen

```
println("Text")              Ausgabe
var x = 5                    Variable (änderbar)
val y = "Hi"                 Variable (fest)
```

```
Int   String   Boolean   Double       Datentypen
"Hallo $name"                         String Template
```

```
+   -   *   /   %                     Mathe (% = Rest)
==  !=  >  <  >=  <=                  Vergleiche → Boolean
```

```
for (i in 1..100) { ... }            Schleife
```

```
if (bedingung) {
    ...
} else if (bedingung) {
    ...
} else {
    ...
}
```

**→ Dieses Sheet bleibt offen!**

---

<!-- ============================================================ -->
<!-- 🎯 CHALLENGE: FIZZBUZZ                                        -->
<!-- ============================================================ -->

# 🎯 Challenge: FizzBuzz

## Könnt ihr dieses Rätsel knacken?

Das Cheat Sheet bleibt offen — nutzt es!

---

## 🎯 FizzBuzz — Aufgabe 1

### Zahlen ausgeben

Schreibe ein Programm, das die **Zahlen von 1 bis 100** untereinander ausgibt.

**Erwartete Ausgabe:**

```
1
2
3
4
...
99
100
```

💡 Tipp: `for`-Loop + `println`

---

## 🎯 FizzBuzz — Aufgabe 2

### Fizz!

Manche Zahlen sollen **übersetzt** werden:

Für **Vielfache von 3** wird `"Fizz"` ausgegeben.

**Erwartete Ausgabe:**

```
1
2
Fizz
4
5
Fizz
7
...
```

💡 Tipp: `if` + Modulo (`%`)
→ Wie prüft man "ist durch 3 teilbar"?

---

## 🎯 FizzBuzz — Aufgabe 3

### Buzz!

Zusätzlich: `"Buzz"` bei **Vielfachen von 5**.

**Erwartete Ausgabe:**

```
1
2
Fizz
4
Buzz
Fizz
7
...
```

💡 Tipp: `else if` hinzufügen

---

## 🎯 FizzBuzz — Aufgabe 4

### FizzBuzz!

Zusätzlich: `"FizzBuzz"` bei Zahlen, die **sowohl durch 3 als auch durch 5** teilbar sind.

**Erwartete Ausgabe:**

```
...
13
14
FizzBuzz
16
...
```

⚠️ **Achtung:** Die Reihenfolge der `if`-Bedingungen ist entscheidend!

Welche Bedingung muss **zuerst** geprüft werden?

---

<!-- ============================================================ -->
<!-- TEIL 3 — THEORIE: OBJEKTORIENTIERUNG                          -->
<!-- ============================================================ -->

# 📘 Teil 3 — Objektorientierte Programmierung

---

## Warum Objektorientierung?

Bisher: Variablen und Funktionen — alles einzeln.

**Problem:** Was wenn wir ein Haustier mit Name, Hunger und Glück beschreiben wollen?

```kotlin
// So? Wird schnell unübersichtlich...
var pet1Name = "Fluffy"
var pet1Hunger = 5
var pet1Happiness = 5

var pet2Name = "Rex"
var pet2Hunger = 3
var pet2Happiness = 8
```

**Besser:** Alles was zusammengehört in einen **Bauplan** packen → **Klasse**!

---

## Klassen = Baupläne

Eine **Klasse** beschreibt, wie ein Ding aufgebaut ist.
Ein **Objekt** ist ein konkretes Exemplar nach diesem Bauplan.

```
Klasse "Hund"              Objekte
┌──────────────┐
│ name         │    →    Rex, Bella, Lucky
│ alter        │    →    3, 7, 1
│ hunger       │    →    5, 2, 8
│              │
│ bellen()     │    →    "Wuff!", "Wuff!", "Wuff!"
│ füttern()    │
└──────────────┘
```

Ein Bauplan, **beliebig viele** Objekte.

---

## Klasse in Kotlin

```kotlin
class Hund(val name: String) {
    var alter: Int = 3
    var hunger: Int = 5

    fun bellen() {
        println("$name sagt: Wuff!")
    }
}
```

| Bestandteil          | Was ist das?                     |
| -------------------- | -------------------------------- |
| `class Hund`         | Name des Bauplans                |
| `(val name: String)` | Parameter beim Erstellen         |
| `var alter: Int = 3` | Eigenschaft (Property)           |
| `fun bellen()`       | Methode (Funktion in der Klasse) |

---

## Objekte erstellen & verwenden

```kotlin
fun main() {
    val rex = Hund("Rex")       // Objekt erstellen
    val bella = Hund("Bella")   // noch eins

    rex.bellen()                // Rex sagt: Wuff!
    bella.bellen()              // Bella sagt: Wuff!

    println(rex.hunger)         // 5
    rex.hunger = 3              // Property ändern
}
```

Der **Punkt `.`** ist der Zugang:

```
objekt.eigenschaft       → Wert lesen/ändern
objekt.methode()         → Funktion ausführen
```

---

<!-- ============================================================ -->
<!-- 📋 CHEAT SHEET 2 — Grundlagen + OOP                           -->
<!-- ============================================================ -->

# 📋 Cheat Sheet — Grundlagen + OOP

```
println("Text")                       Ausgabe
var x = 5  /  val y = "Hi"           Variablen
"Hallo $name"                         String Template
+  -  *  /  %                         Mathe (% = Modulo)
==  !=  >  <  >=  <=                  Vergleiche
```

```
for (i in 1..10) { ... }             Schleife
if (bed) { } else if { } else { }    Bedingung
```

```kotlin
class MeineKlasse(val name: String) {    // Klasse
    var wert: Int = 0                    // Property
    fun methode() { ... }               // Methode
}

val obj = MeineKlasse("Test")           // Objekt erstellen
obj.methode()                           // Methode aufrufen
obj.wert                                // Property lesen
```

**→ Dieses Sheet bleibt offen!**

---

<!-- ============================================================ -->
<!-- 🎯 TASK: STECKBRIEF                                           -->
<!-- ============================================================ -->

# 🎯 Aufgabe: Steckbrief-Klasse

## Erstellt euren eigenen digitalen Steckbrief!

---

## 🎯 Steckbrief — Grundgerüst

Dieses Gerüst bekommt ihr von mir:

```kotlin
class Steckbrief(val name: String) {
    var alter: Int = 0
    var hobby: String = ""

    fun print() {
        println("Hallo ich heiße $name, bin $alter Jahre alt und mag $hobby.")
    }
}

fun main() {
    val ich = Steckbrief("Euer Name")
    ich.alter = 16
    ich.hobby = "Zocken"
    ich.print()
}
```

---

## 🎯 Steckbrief — Eure Aufgabe

**1.** Tragt eure eigenen Daten ein und lasst es laufen.

**2.** Fügt **mindestens 2 neue Properties** hinzu, z.B.:

- `groesse_in_cm`
- `lieblingsessen`
- `lieblingsfach`
- `haustier`
- ... was euch einfällt!

**3.** Erweitert die `print()`-Methode, damit die neuen Properties auch ausgegeben werden.

**4.** Bonus: Erstellt ein **zweites Objekt** für euren Sitznachbarn!

---

<!-- ============================================================ -->
<!-- ÜBERGANG ZU PET KATA                                           -->
<!-- ============================================================ -->

# 📘 Übergang: Digital Pet

---

## Was bauen wir jetzt?

Ein **interaktives virtuelles Haustier** 🐾

- Es hat **Hunger** und **Glück**
- Man kann es **füttern** und mit ihm **spielen**
- Man kann seinen **Status** abfragen
- Am Ende steuert man es über ein **Menü im Terminal**

Ihr baut das Schritt für Schritt — Aufgabe für Aufgabe.

---

## Pet — Grundstruktur

```kotlin
class Pet(val name: String) {
    var hunger: Int = 5        // 0 = satt, 10 = am Verhungern
    var happiness: Int = 5     // 0 = traurig, 10 = überglücklich
}
```

**Testen mit:**

```kotlin
fun main() {
    val pet = Pet("Fluffy")
    println("Name: ${pet.name}")
    println("Hunger: ${pet.hunger}")
    println("Happiness: ${pet.happiness}")
}
```

---

<!-- ============================================================ -->
<!-- 📋 CHEAT SHEET 3 — Komplett, bleibt offen für Pet Kata        -->
<!-- ============================================================ -->

# 📋 Cheat Sheet — Komplett

```
println("Text")                       Ausgabe
var x = 5  /  val y = "Hi"           var=änderbar, val=fest
"Hallo $name"  "${a + b}"            String Templates
```

```
+  -  *  /  %                         Mathe (% = Rest)
==  !=  >  <  >=  <=                  Vergleiche → Boolean
```

```
for (i in 1..100) { ... }            For-Loop
while (bedingung) { ... }            While-Loop
```

```
if (bed) { }
else if (bed) { }                    Bedingungen
else { }

when { bed -> ... else -> ... }      When-Expression
```

```kotlin
class Name(val p: String) {          Klasse
    var x: Int = 0                   Property
    fun m() {                        Methode
        x = (x + 1).coerceIn(0, 10) Wert begrenzen
    }
}
val obj = Name("..."); obj.m()       Objekt erstellen & nutzen
```

**→ Bleibt offen für die Pet-Aufgaben!**

---

<!-- ============================================================ -->
<!-- 🎯 CODING KATA: DIGITAL PET                                   -->
<!-- ============================================================ -->

# 🎯 Coding Kata: Digital Pet 🐾

## Baut Schritt für Schritt euer eigenes Haustier!

---

## 🎯 Pet — Aufgabe 1: Klasse erstellen

Erstelle eine Klasse `Pet`, die beim Erstellen einen **Namen** bekommt.

Das Pet startet mit:

- `hunger: 5` → (0 = satt, 10 = am Verhungern)
- `happiness: 5` → (0 = traurig, 10 = überglücklich)

**Teste mit:**

```kotlin
fun main() {
    val pet = Pet("Fluffy")
    println("Name: ${pet.name}")
    println("Hunger: ${pet.hunger}")
    println("Happiness: ${pet.happiness}")
}
```

---

## 🎯 Pet — Aufgabe 2: `feed()`

Füge eine Methode `feed()` hinzu.

**Regeln:**

- hunger **sinkt um 2** (Füttern macht satt)
- happiness **steigt um 1** (Essen macht glücklich)
- Kein Wert darf **unter 0** oder **über 10** gehen!

**Ausgabe:** `"$name wurde gefüttert! 🍖"`

💡 Tipp: `.coerceIn(0, 10)` begrenzt einen Wert:

```kotlin
hunger = (hunger - 2).coerceIn(0, 10)
```

---

## 🎯 Pet — Aufgabe 3: `play()`

Füge eine Methode `play()` hinzu.

**Regeln:**

- happiness **steigt um 2** (Spielen macht Spaß!)
- hunger **steigt um 1** (Spielen macht hungrig)
- Kein Wert unter 0 oder über 10!

**Ausgabe:** `"$name hat gespielt! 🎾"`

🌟 **Bonus:** Sucht mal ob es in Kotlin eine Methode gibt, die den Wert begrenzt — ohne `if`!

---

## 🎯 Pet — Aufgabe 4: `getStatus()`

Erstelle eine Methode `getStatus()` die einen **Text** zurückgibt, der beschreibt wie es dem Pet geht.

**Hunger-Text:**
| Bedingung | Text |
|-----------------|-------------------------|
| `hunger >= 7` | `"am Verhungern 😫"` |
| `hunger >= 4` | `"etwas hungrig 😐"` |
| sonst | `"satt und zufrieden 😊"` |

**Happiness-Text:**
| Bedingung | Text |
|--------------------|------------------------|
| `happiness >= 7` | `"super glücklich 😄"` |
| `happiness >= 4` | `"ganz okay 🙂"` |
| sonst | `"traurig 😢"` |

💡 Tipp: Nutzt `when { }` — das ist sauberer als viele `if`s!

**Rückgabe:** `"$name ist $hungerText und $happinessText"`

---

## 🎯 Pet — Aufgabe 5: Interaktives Menü

⚠️ **Ab hier arbeiten wir in IntelliJ!**

Baue eine `main()`-Funktion, die ein **Menü** im Terminal zeigt:

```
=== DIGITALES HAUSTIER ===
Wie soll dein Haustier heißen? Fluffy

--- Runde ---
Fluffy ist etwas hungrig und ganz okay
Was möchtest du tun?
  1 → Füttern 🍖
  2 → Spielen 🎾
  3 → Status ansehen 📊
  0 → Beenden 👋
> _
```

**Neue Konzepte:**

- `while (running) { ... }` → Endlosschleife mit Abbruch
- `readln()` → Eingabe vom Benutzer lesen
- `when (readln()) { "1" -> ... }` → Eingabe auswerten

---

<!-- ============================================================ -->
<!-- FINALES CHEAT SHEET                                            -->
<!-- ============================================================ -->

# 📋 Cheat Sheet — Alles auf einen Blick

**Ausgabe & Eingabe**

```
println("Text")          Zeile ausgeben
print("Text")            Ohne Umbruch
val x = readln()         Eingabe lesen (→ String)
```

**Variablen & Typen**

```
var x = 5                änderbar       Int String
val y = "Hi"             fest           Boolean Double
"Hallo $name"            String Template
```

**Operatoren**

```
+  -  *  /  %            Mathe          % = Rest
==  !=  >  <  >=  <=     Vergleiche     → Boolean
```

**Kontrollstrukturen**

```
for (i in 1..10) { }                   Schleife
while (bedingung) { }                  While-Loop
if (b) { } else if (b) { } else { }   Bedingung
when { bed -> ...  else -> ... }       When
```

**Klassen**

```
class Name(val p: Typ) {    Klasse definieren
    var x: Int = 0           Property
    fun m() { }              Methode
}
val obj = Name("X")          Objekt erstellen
obj.x   obj.m()              Zugriff mit Punkt
```

**Extras**

```
x.coerceIn(0, 10)           Wert begrenzen
"42".toInt()                 String → Int
```
