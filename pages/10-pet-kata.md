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

# Cheat Sheet — Komplett

<div class="grid grid-cols-2 gap-6 text-xs">

<div>

**Ein- & Ausgabe**

```kotlin
println("Text")      // Zeile
print("Text")        // ohne Umbruch
val x = readln()     // Eingabe (String)
```

**Variablen & Templates**

```kotlin
var x = 5     // änderbar
val y = "Hi"  // fest
"Hallo $name"   "${a + b}"
```

**Operatoren**

```kotlin
+  -  *  /  %         // % = Rest
==  !=  >  <  >=  <=  // → Boolean
```

**Kontrollfluss**

```kotlin
for (i in 1..10) { }
while (bedingung) { }
if (b) { } else if (b) { } else { }
when { bed -> ...  else -> ... }
```

</div>

<div>

**Klassen**

```kotlin
class Name(val p: String) {
    var x: Int = 0
    fun m() {
        x = (x + 1).coerceIn(0, 10)
    }
}

val obj = Name("…")
obj.m()
obj.x
```

**Praktische Helfer**

```kotlin
x.coerceIn(0, 10)   // Wert begrenzen
"42".toInt()        // String → Int
```

</div>

</div>

<div class="pt-2 text-center opacity-80">
👉 Bleibt offen für die Pet-Aufgaben!
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

💡 Tipp: `.coerceIn(0, 10)` begrenzt einen Wert:

```kotlin
hunger = (hunger - 2).coerceIn(0, 10)
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
        hunger = (hunger - 2).coerceIn(0, 10)
        happiness = (happiness + 1).coerceIn(0, 10)
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
    happiness = (happiness + 2).coerceIn(0, 10)
    hunger = (hunger + 1).coerceIn(0, 10)
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

## ✅ Lösung mit `when`

```kotlin
fun getStatus(): String {
    val hungerText = when {
        hunger >= 7 -> "am Verhungern 😫"
        hunger >= 4 -> "etwas hungrig 😐"
        else        -> "voll gefressen 😊"
    }

    val happinessText = when {
        happiness >= 7 -> "super glücklich 😄"
        happiness >= 4 -> "ganz zufrieden 🙂"
        else           -> "traurig 😢"
    }

    return "$name ist $hungerText und $happinessText"
}
```

<div class="pt-2 opacity-75 text-sm">
<code>when { ... }</code> ist die saubere Alternative zu langen <code>if/else if</code>-Ketten.
</div>

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
- `when (eingabe) { "1" -> ... }` → Eingabe auswerten

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

        when (readln()) {
            "1" -> pet.feed()
            "2" -> pet.play()
            "3" -> println(pet.getStatus())
            "0" -> running = false
            else -> println("Ungültige Eingabe!")
        }
    }
    println("Tschüss! 👋")
}
```

</div>
