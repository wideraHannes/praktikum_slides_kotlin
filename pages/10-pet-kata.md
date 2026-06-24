---
layout: section
class: text-center
---

# 🐾 Übergang: Digital Pet

## Was bauen wir jetzt?

---
layout: two-cols
layoutClass: gap-10
---

# Ein virtuelles Haustier 🐾

<v-clicks>

- Es hat **Hunger** und **Glück**
- Man kann es **füttern** und mit ihm **spielen**
- Man kann seinen **Status** abfragen
- Am Ende steuert man es über ein **Menü im Terminal**

</v-clicks>

<div v-click class="pt-6 opacity-80">
Ihr baut das Schritt für Schritt — Aufgabe für Aufgabe.
</div>

::right::

<div class="pt-4">

**Grundstruktur**

```kotlin
class Pet(val name: String) {
    var hunger: Int = 5
    // 0 = satt, 10 = am Verhungern

    var happiness: Int = 5
    // 0 = traurig, 10 = überglücklich
}
```

</div>

---
layout: section
class: text-center
---

# 📋 Cheat Sheet

## Komplett — bleibt offen für die Pet-Kata!

---
class: cheatsheet
---

<div class="cheat-head">
  <div class="cheat-title">Kotlin · Cheat Sheet — Komplett</div>
  <div class="cheat-sub">Grundlagen · Funktionen · Kontrollfluss · OOP — alles auf einer Seite</div>
</div>

<div class="cheat-grid">

<!-- ═══ SPALTE 1 — BASICS ═══ -->
<div class="cheat-col">

<div class="section-head section-blue">① Basics</div>

<div class="cheat-card">

**Programm-Skelett & Ausgabe**

```kotlin
fun main() {
    println("Text")    // mit Umbruch
    print("…")         // ohne
    val x = readln()   // Eingabe
}
```

</div>

<div class="cheat-card">

**Variablen**

```kotlin
val name = "Mia"   // fest
var punkte = 0     // änderbar
```

<div class="hint">Wenn möglich <code>val</code>, sonst <code>var</code>.</div>

</div>

<div class="cheat-card">

**Datentypen · Inferenz**

| Typ       | Beispiel  |
| --------- | --------- |
| `Int`     | `42`      |
| `Double`  | `3.14`    |
| `String`  | `"Hallo"` |
| `Boolean` | `true`    |

```kotlin
val a = 16              // Int erkannt
val pi: Double = 3.14   // explizit
```

</div>

<div class="cheat-card">

**String Templates**

```kotlin
"Hallo $name"
"Summe: ${a + b}"
```

</div>

<div class="section-head section-violet">② Funktionen</div>

<div class="cheat-card">

**Bestandteile**

```kotlin
fun gruss(name: String): String {
    return "Hallo $name"
}
```

| Teil | Bedeutung |
| --- | --- |
| `fun` | Schlüsselwort |
| `gruss` | Name |
| `(name: String)` | Parameter : Typ |
| `: String` | Rückgabetyp |
| `{ … }` | Rumpf |

</div>

<div class="cheat-card">

**Aufrufen**

```kotlin
fun main() {
    val text = gruss("Tom")
    println(text)
}
```

</div>

</div>

<!-- ═══ SPALTE 2 — OPERATOREN & KONTROLLFLUSS ═══ -->
<div class="cheat-col">

<div class="section-head section-amber">③ Mathe & Vergleiche</div>

<div class="cheat-card">

**Mathe**

```kotlin
+   -   *   /        // Grundrechnen
%                    // Rest (Modulo)
10 + 3   // → 13
10 / 3   // → 3      (Int-Division)
10.0 / 3 // → 3.33…  (Double)
15 % 5   // → 0      (5 teilt 15)
10 % 3   // → 1      (Rest)
```

</div>

<div class="cheat-card">

**Vergleiche → Boolean**

```kotlin
==  !=                // gleich / ungleich
<   <=   >   >=       // kleiner / größer
```

</div>

<div class="section-head section-emerald">④ Kontrollfluss</div>

<div class="cheat-card">

**Bedingung — `if` / `else`**

```kotlin
if (bedingung) {
    …
} else if (bedingung) {
    …
} else {
    …
}

if (zahl % 2 == 0) {
    println("Zahl ist gerade")
}
```

</div>

<div class="cheat-card">

**Schleifen — `for` & `while`**

```kotlin
for (i in 1..5)   { … }   // 1..5
while (i < 10)    { i++ } // solange wahr
```

</div>

<div class="cheat-card">

**Wert begrenzen mit `if`**

```kotlin
if (hunger > 10) hunger = 10
if (hunger < 0)  hunger = 0
```

</div>

</div>

<!-- ═══ SPALTE 3 — OOP ═══ -->
<div class="cheat-col">

<div class="section-head section-rose">⑤ OOP — Syntax</div>

<div class="cheat-card">

**Klasse — Skelett**

```kotlin
class Name(val p: Typ) {
    var eigenschaft: Typ = wert

    fun methode() {
        …
    }

    fun beschreibung(): String {
        return "…"
    }
}
```

| Teil | Bedeutung |
| --- | --- |
| `class Name` | Bauplan-Name |
| `(val p: Typ)` | Konstruktor-Parameter |
| `var … = …` | Property (Zustand) |
| `fun …() { … }` | Methode (Verhalten) |
| `: String` + `return` | Rückgabewert |

</div>

<div class="cheat-card">

**Objekt erstellen & nutzen**

```kotlin
val a = Name("…")        // erstellen
val b = Name("…")        // beliebig viele

a.eigenschaft = …        // ändern
println(a.eigenschaft)   // lesen
a.methode()              // aufrufen
val t = a.beschreibung() // Rückgabe
```

<div class="hint">Der <b>Punkt <code>.</code></b> ist der Zugang zum Objekt. Jedes Objekt hat seinen <b>eigenen</b> Zustand.</div>

</div>

</div>

</div>

<style>
.slidev-layout.cheatsheet {
  padding: 0.4rem 0.6rem 0.3rem;
  background: #ffffff !important;
  color: #1f2937;
  font-size: 0.46rem;
  line-height: 1.18;
  display: flex;
  flex-direction: column;
  gap: 0.18rem;
  overflow: hidden;
}
.cheatsheet .cheat-head {
  border-bottom: 1px solid #e2e8f0;
  padding-bottom: 0.12rem;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
.cheatsheet .cheat-title {
  font-size: 0.7rem;
  font-weight: 600;
  color: #1e293b;
  letter-spacing: -0.01em;
  line-height: 1.1;
}
.cheatsheet .cheat-sub {
  font-size: 0.44rem;
  color: #64748b;
}
.cheatsheet .cheat-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.25rem;
  flex: 1 1 auto;
  min-height: 0;
}
.cheatsheet .cheat-col {
  display: flex;
  flex-direction: column;
  gap: 0.16rem;
  min-width: 0;
}
.cheatsheet .section-head {
  font-size: 0.48rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  padding: 0.08rem 0.3rem;
  border-radius: 2px;
  color: #475569;
  background: #f1f5f9;
  border-left: 2px solid #94a3b8;
  margin-top: 0.08rem;
}
.cheatsheet .section-head:first-child { margin-top: 0; }
.cheatsheet .section-blue,
.cheatsheet .section-violet,
.cheatsheet .section-amber,
.cheatsheet .section-emerald,
.cheatsheet .section-rose {
  color: #475569;
  background: #f1f5f9;
  border-left-color: #94a3b8;
}
.cheatsheet .cheat-card {
  background: #ffffff;
  border: 1px solid #e2e8f0;
  border-radius: 3px;
  padding: 0.14rem 0.28rem 0.2rem;
}
.cheatsheet .cheat-card > p:first-child,
.cheatsheet .cheat-card > p:first-child strong {
  margin: 0 0 0.1rem 0;
  font-size: 0.44rem;
  color: #475569;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.cheatsheet .cheat-card pre,
.cheatsheet .cheat-card .slidev-code {
  margin: 0 !important;
  padding: 0.16rem 0.28rem !important;
  font-size: 0.42rem !important;
  line-height: 1.22 !important;
  background: #0f172a !important;
  border-radius: 2px;
}
.cheatsheet .cheat-card code {
  font-size: 0.42rem;
}
.cheatsheet .cheat-card ul {
  margin: 0.1rem 0 0;
  padding-left: 0.65rem;
}
.cheatsheet .cheat-card li {
  margin: 0.02rem 0;
}
.cheatsheet .cheat-card table {
  width: 100%;
  font-size: 0.44rem;
  border-collapse: collapse;
  margin: 0.12rem 0;
}
.cheatsheet .cheat-card table + pre,
.cheatsheet .cheat-card pre + table {
  margin-top: 0.14rem !important;
}
.cheatsheet .cheat-card th,
.cheatsheet .cheat-card td {
  padding: 0.02rem 0.2rem;
  border-bottom: 1px solid #f1f5f9;
  text-align: left;
}
.cheatsheet .cheat-card th {
  color: #64748b;
  font-weight: 500;
  font-size: 0.4rem;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.cheatsheet .cheat-card td code {
  background: #f1f5f9;
  padding: 0 0.12rem;
  border-radius: 2px;
}
.cheatsheet .hint {
  font-size: 0.42rem;
  color: #64748b;
  margin-top: 0.1rem;
}
.cheatsheet .hint code {
  background: #f1f5f9;
  padding: 0 0.1rem;
  border-radius: 2px;
}
</style>

---
layout: section
class: text-center
---

# 🎯 Coding Kata: Digital Pet 🐾

## Baut Schritt für Schritt euer eigenes Haustier!

<div class="pt-8 text-center text-xl opacity-80">
Alles im <b>Playground</b> — bis Aufgabe 5, da wechseln wir zu IntelliJ.
</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 1

## Klasse erstellen

Erstelle die Klasse `Pet`, die beim Erstellen einen **Namen** bekommt.

Das Tier startet mit zwei Werten:

- `hunger: 5` &nbsp; (0 = satt, 10 = am Verhungern)
- `happiness: 5` &nbsp; (0 = todtraurig, 10 = überglücklich)

::right::

<div v-click>

## ✅ Lösung

```kotlin
class Pet(val name: String) {
    var hunger: Int = 5
    var happiness: Int = 5
}

fun main() {
    val pet = Pet("Fluffy")
    println("Name: ${pet.name}")
    println("Hunger: ${pet.hunger}")
    println("Happiness: ${pet.happiness}")
}
```

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 2

## Haustier füttern 🍖

Füge der Klasse `Pet` eine Methode `feed()` hinzu.

**Regeln**

- `hunger` **sinkt um 2** (Futter macht satt)
- `happiness` **steigt um 1** (Essen macht glücklich)

Kein Wert darf unter 0 oder über 10 gehen!

<div v-click>

💡 Tipp: Mit `if` begrenzen, damit nichts unter 0 oder über 10 geht:

```kotlin
if (hunger > 10) hunger = 10
if (hunger < 0)  hunger = 0
```

</div>

::right::

<div v-click>

## ✅ Lösung

```kotlin
class Pet(val name: String) {
    var hunger: Int = 5
    var happiness: Int = 5

    fun feed() {
        hunger = hunger - 2
        happiness = happiness + 1

        if (hunger < 0) hunger = 0
        if (happiness > 10) happiness = 10

        println("$name wurde gefüttert! 🍖")
    }
}
```

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 3 _(10 min)_

## Mit Haustier spielen 🎾

Füge eine Methode `play()` hinzu.

**Regeln**

- `happiness` **steigt um 2** (Spielen macht Spaß!)
- `hunger` **steigt um 1** (Spielen macht hungrig)

Weiterhin gilt: Kein Wert darf unter 0 oder über 10 gehen!

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun play() {
    happiness = happiness + 2
    hunger = hunger + 1

    if (happiness > 10) happiness = 10
    if (hunger > 10) hunger = 10

    println("$name hat gespielt! 🎾")
}
```

</div>

---

# 🎯 Pet — Aufgabe 4 _(30 min)_

## Status anzeigen 📊

Erstelle eine Methode `getStatus()`, die einen **beschreibenden Text** des Haustiers zurückgibt.

Dabei soll der Text widerspiegeln, **wie glücklich und hungrig** das Haustier gerade ist.

**Der Text könnte zum Beispiel lauten**

`hunger = 4` und `happiness = 10`:<br>
→ _„Fluffy ist etwas hungrig und super glücklich 😄"_

`hunger = 2` und `happiness = 5`:<br>
→ _„Fluffy ist voll gefressen und ganz zufrieden"_

::right::

<div v-click>

## ✅ Lösung mit `if`/`else if`

```kotlin
fun getStatus(): String {
    var hungerText = "voll gefressen 😊"
    if (hunger >= 7) {
        hungerText = "am Verhungern 😫"
    } else if (hunger >= 4) {
        hungerText = "etwas hungrig 😐"
    }

    var happinessText = "traurig 😢"
    if (happiness >= 7) {
        happinessText = "super glücklich 😄"
    } else if (happiness >= 4) {
        happinessText = "ganz zufrieden 🙂"
    }

    return "$name ist $hungerText und $happinessText"
}
```

</div>

---

# ⚠️ Ab hier wechseln wir zu IntelliJ

## Aufgabe 5 ist interaktiv — dafür brauchen wir ein richtiges Terminal

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 5 _(60 min)_

## Interaktiv mit dem Haustier spielen

Wenn du das Programm startest, wird zunächst der **Name des Haustieres** abgefragt.

Anschließend kann der Benutzer **beliebig oft** zwischen den folgenden Optionen wählen, indem er die entsprechende Nummer im Terminal eingibt:

```text
1 → Füttern
2 → Spielen
3 → Status ansehen
0 → Beenden
```

Nach jeder Aktion wird dem Nutzer ein Text angezeigt, der beschreibt, welche Optionen ihm zur Verfügung stehen.

<div v-click class="pt-3">

💡 **Neue Bausteine**

- `while (running) { ... }` → Schleife mit Abbruch
- `readln()` → Eingabe vom Benutzer lesen
- `if (eingabe == "1") { ... }` → Eingabe auswerten

</div>

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun main() {
    println("=== DIGITALES HAUSTIER ===")
    print("Wie soll dein Haustier heißen? ")
    val name = readln()
    val pet = Pet(name)

    var running = true
    while (running) {
        println("\n--- Runde ---")
        println(pet.getStatus())
        println("Was möchtest du tun?")
        println("  1 → Füttern 🍖")
        println("  2 → Spielen 🎾")
        println("  3 → Status ansehen 📊")
        println("  0 → Beenden 👋")
        print("> ")

        val eingabe = readln()
        if (eingabe == "1") {
            pet.feed()
        } else if (eingabe == "2") {
            pet.play()
        } else if (eingabe == "3") {
            println(pet.getStatus())
        } else if (eingabe == "0") {
            running = false
        } else {
            println("Ungültige Eingabe!")
        }
    }
    println("Tschüss! 👋")
}
```

</div>
