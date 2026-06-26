---
layout: section
class: text-center
---

# 🐾 Übergang: Digital Pet

## Was bauen wir jetzt?

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

Das Tier startet mit zwei Werten — **Startwerte dürft ihr euch selbst aussuchen** (z. B. 5):

- `hunger` &nbsp; (0 = satt, 10 = am Verhungern)
- `happiness` &nbsp; (0 = todtraurig, 10 = überglücklich)

Erstelle anschließend dein Digital Pet in `main()` und **gib alle Attribute in der Konsole aus**.

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

**Zum Testen:** Füttere dein Tier in `main()` und gib die Attribute danach erneut aus — verändern sie sich wie erwartet?

<div v-click>

💡 Tipp: Mit `if` begrenzen, damit nichts unter 0 oder über 10 geht:

```kotlin
if (hunger > 10) {
    hunger = 10
}
if (hunger < 0) {
    hunger = 0
}
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

        if (hunger < 0) {
            hunger = 0
        }
        if (happiness > 10) {
            happiness = 10
        }

        println("$name wurde gefüttert! 🍖")
    }
}
```

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 3

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

    if (happiness > 10) {
        happiness = 10
    }
    if (hunger > 10) {
        hunger = 10
    }

    println("$name hat gespielt! 🎾")
}
```

</div>

---

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Pet — Aufgabe 4

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

# 🎯 Pet — Aufgabe 5

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

::right::

<div class="pt-12">

💡 **Neue Bausteine**

- `while (running) { ... }` → Schleife mit Abbruch
- `readln()` → Eingabe vom Benutzer lesen
- `if (eingabe == "1") { ... }` → Eingabe auswerten

</div>

---

# 🎯 Pet — Aufgabe 5

## ✅ Lösung — Kern: `while`-Loop

```kotlin
var running = true
while (running) {
    println("Was möchtest du tun?")
    println("  1 → Füttern")
    println("  2 → Spielen")
    println("  3 → Status")
    println("  0 → Beenden")

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
```

---
layout: two-cols
layoutClass: gap-8 pet-solution-full
---

# 🎯 Pet — Komplette Lösung

## Klasse `Pet` (Aufgaben 1–4)

```kotlin
class Pet(val name: String) {
    var hunger: Int = 5
    var happiness: Int = 5

    fun feed() {
        hunger = hunger - 2
        happiness = happiness + 1

        if (hunger < 0) {
            hunger = 0
        }
        if (happiness > 10) {
            happiness = 10
        }

        println("$name wurde gefüttert! 🍖")
    }

    fun play() {
        happiness = happiness + 2
        hunger = hunger + 1

        if (happiness > 10) {
            happiness = 10
        }
        if (hunger > 10) {
            hunger = 10
        }

        println("$name hat gespielt! 🎾")
    }

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
}
```

::right::

<div class="pt-12">

## `main()` (Aufgabe 5)

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

<style>
.pet-solution-full h1 { font-size: 1.1rem !important; margin-bottom: 0.3rem !important; }
.pet-solution-full h2 { font-size: 0.7rem !important; margin: 0.15rem 0 0.2rem !important; }
.pet-solution-full pre,
.pet-solution-full .slidev-code {
  font-size: 0.42rem !important;
  line-height: 1.2 !important;
  padding: 0.25rem 0.45rem !important;
}
.pet-solution-full pre code,
.pet-solution-full .slidev-code code,
.pet-solution-full pre .line,
.pet-solution-full pre span { font-size: 0.42rem !important; line-height: 1.2 !important; }
.pet-solution-full .pt-12 { padding-top: 0.3rem !important; }
</style>

---
layout: two-cols
layoutClass: gap-8
---

# 🚀 Erweiterungen — wer noch Zeit hat

## Macht euer Pet einzigartig!

<v-clicks>

- 🎭 **Gesicht im Terminal** — Pet zeigt seine Laune mit ASCII-Art
- 🐣 **Tamagotchi-Modus** — neue Attribute: `energy`, `hygiene`, `alter`
- 💤 **`sleep()`-Methode** — Energie zurück, kostet etwas Zeit
- 🗣️ **Tier kann reden** — zufällige Sprüche je nach Laune
- 💀 **Pet kann sterben** — wenn `hunger == 10` zu lange
- ⏰ **Zeit vergeht automatisch** — Werte sinken pro Runde
- 🎲 **Zufall mit `Random`** — mal frech, mal müde
- 🤖 **Mini-KI** — Pet schlägt selbst vor, was es will

</v-clicks>

::right::

<div v-click="9" class="pt-8">

## 🎭 Beispiel: Gesicht zeigen

```kotlin
fun zeigeGesicht() {
    if (happiness >= 7) {
        println("  ( ^_^ )")
        println("  /     \\")
    } else if (happiness >= 4) {
        println("  ( -_- )")
        println("  /     \\")
    } else {
        println("  ( T_T )")
        println("  /     \\")
    }
}
```

</div>

<div v-click="10" class="pt-4 text-sm opacity-80">
💡 Tipp: Mit <code>kotlin.random.Random.nextInt(0, 3)</code> bekommst du eine Zufallszahl 0/1/2 — damit kannst du z. B. zwischen verschiedenen Sprüchen wählen.
</div>
