---
theme: default
title: Einführung in die Programmierung — Kotlin
info: |
  ## Einführung in die Programmierung
  Am Beispiel Kotlin — für die 10. Klasse
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  sans: 'Inter'
  mono: 'JetBrains Mono'
colorSchema: light
---

# Einführung in die Programmierung

## Am Beispiel **Kotlin** 🏝️

<div class="pt-12">
  <span class="px-2 py-1 rounded bg-white/10 text-sm">
    Drücke <kbd>→</kbd> oder <kbd>Leertaste</kbd> um weiterzublättern
  </span>
</div>

<!--
Willkommen zum Kotlin-Praktikum. Heute: Was ist Programmierung, Grundlagen Kotlin, FizzBuzz, Klassen, und am Ende ein digitales Haustier.
-->

---
layout: two-cols
layoutClass: gap-8
---

# Fahrplan — 2 Tage

<v-clicks>

📘 **Teil 1** — Was ist Programmierung?

📘 **Teil 2** — Kotlin Grundlagen

🎤 **Live Demo** — Wir programmieren zusammen

🖐️ **Hands-on** — FizzBuzz Challenge

📘 **Teil 3** — Objektorientierung

🖐️ **Hands-on** — Steckbrief

🐾 **Coding Kata** — Digital Pet

</v-clicks>

::right::

<div class="pt-12 text-center text-6xl opacity-80">
🧠 → 💻 → 🎮
</div>

<div class="pt-6 text-center opacity-70">
Theorie · Demo · Selber bauen
</div>

<div class="pt-8 text-center text-sm opacity-60">
Wir wechseln zwischen <b>Theorie</b>, <b>Live-Demo</b> und <b>Hands-on</b>.
</div>

---
layout: two-cols
layoutClass: gap-8
---

# Was lernen wir — und was nicht?

**Diese 2 Tage**

<v-clicks>

- ✅ Grundbausteine: Variablen, Schleifen, `if`/`else`
- ✅ Daten in Klassen organisieren
- ✅ Ein kleines, vollständiges Programm bauen
- ✅ Wie ein Programmierer **denken**

</v-clicks>

::right::

<div class="pt-12">

**Das schaffen wir nicht (heute)**

<v-clicks>

- ❌ Eigene Android-App veröffentlichen
- ❌ 3D-Spiele bauen
- ❌ Datenbanken, Web, Netzwerk
- ❌ Künstliche Intelligenz

</v-clicks>

<div v-click class="pt-6 opacity-75 text-sm">
Aber: Mit den Grundlagen von heute könnt ihr <b>jede</b> dieser Sachen später lernen — die Konzepte sind in allen Sprachen ähnlich.
</div>

</div>

---

# Bestandteile einer Programmiersprache

Fast jede Programmiersprache hat dieselben Grundbausteine:

<div class="grid grid-cols-2 gap-x-10 gap-y-3 pt-4 text-sm">

<div v-click>

**🧱 Werte & Typen**<br>
Zahlen, Text, Wahrheitswerte
<div class="opacity-60">→ `42`, `"Hallo"`, `true`</div>

</div>

<div v-click>

**📦 Variablen**<br>
Werte mit einem Namen speichern
<div class="opacity-60">→ `var x = 5`</div>

</div>

<div v-click>

**➕ Operatoren**<br>
Werte verknüpfen und vergleichen
<div class="opacity-60">→ `+`, `-`, `==`, `>`</div>

</div>

<div v-click>

**🔀 Kontrollfluss**<br>
Entscheidungen und Wiederholungen
<div class="opacity-60">→ `if`, `for`, `while`</div>

</div>

<div v-click>

**🔧 Funktionen**<br>
Wiederverwendbare Code-Bausteine
<div class="opacity-60">→ `fun begruessen() { … }`</div>

</div>

<div v-click>

**🏗️ Klassen & Objekte**<br>
Daten + zugehörige Funktionen bündeln
<div class="opacity-60">→ `class Pet(val name: String)`</div>

</div>

</div>

<div v-click class="pt-6 text-center opacity-80">
👉 All das schauen wir uns in Kotlin an.
</div>

---
layout: section
class: text-center
---

# 📘 Teil 1
## Was ist Programmierung?

---

# Was ist Programmierung?

Computer sind **dumm** — sie können nur genau das tun, was man ihnen<br>**Schritt für Schritt** sagt.

<v-click>

Programmieren = dem Computer **Anweisungen** geben, in einer Sprache die er versteht.

</v-click>

<v-click>

```text
1. Nimm eine Zahl
2. Wenn sie durch 3 teilbar ist → sag "Fizz"
3. Sonst → sag die Zahl
```

</v-click>

<v-click>

<div class="mt-6 text-center opacity-80">
Das ist im Prinzip schon ein Programm.
</div>

</v-click>

---

# Wo steckt überall Programmierung drin?

| Bereich      | Beispiele                                   |
| ------------ | ------------------------------------------- |
| 📱 Apps      | Instagram, WhatsApp, TikTok                 |
| 🌐 Websites  | YouTube, Google, Wikipedia                  |
| 🎮 Spiele    | Minecraft, Fortnite, FIFA                   |
| 🤖 Geräte    | Roboter, Drohnen, Smartwatches              |
| 🚗 Autos     | Autopilot, Einparkhilfe                     |
| 🧠 KI        | ChatGPT, Bilderkennung, Sprachassistenten   |

<div class="pt-6 text-center opacity-75">
Praktisch alles, was einen Bildschirm hat (und vieles ohne) wird programmiert.
</div>

---

# Welche Programmiersprachen gibt es?

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

<div class="pt-4 opacity-75">
Keine Sprache ist <i>"die beste"</i> — es kommt darauf an, <b>was</b> man bauen will.
</div>

---
layout: two-cols
layoutClass: gap-12
---

# Was ist Kotlin?

<v-clicks>

- Moderne Sprache von **JetBrains** (seit 2016 stabil)
- Von **Google** als bevorzugte Sprache für Android empfohlen
- Läuft auf der **JVM** (Java Virtual Machine)
- Klare, lesbare Syntax — weniger Code, gleiches Ergebnis
- Name kommt von der **Insel Kotlin** bei St. Petersburg 🏝️

</v-clicks>

::right::

<div class="pt-8">

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

</div>

<div class="pt-4 opacity-70 text-sm">
Kein Semikolon, keine Klassen-Hülle nötig —<br>einfach loslegen.
</div>

---

# Wo läuft Kotlin?

```text
                    Kotlin-Code
                        │
                        ▼
                    Compiler
                   ╱    │    ╲
                  ▼     ▼     ▼
                JVM   Native  JavaScript
                 │      │        │
             Android   iOS    Websites
             Server   Desktop  Browser
```

<div class="pt-6 text-center text-lg">
Kotlin ist <b>Multiplatform</b> — ein Code, viele Plattformen.
</div>

---
layout: two-cols
layoutClass: gap-8
---

# Warum Kotlin für uns?

**Zum Lernen**

- Einfach zu lesen und schreiben
- Sofort im Browser testbar → kein Setup
- Fehler werden früh erkannt

**In der echten Welt**

- Offizielle Sprache für Android
- Google, Netflix, Amazon, Uber nutzen Kotlin
- Wächst stark — gute Jobchancen

<div class="pt-3 text-sm opacity-80">
👉 Echte Case Studies: <a href="https://kotlinlang.org/case-studies/" target="_blank">kotlinlang.org/case-studies</a>
</div>

::right::

<div class="pt-8">

**Wann eher etwas Anderes?**

| Aufgabe       | Sprache       |
| ------------- | ------------- |
| Websites      | JavaScript    |
| KI            | Python        |
| iPhone-Apps   | Swift         |
| 3D-Spiele     | C# / C++      |

</div>

---
layout: center
class: text-center
---

# Unser Werkzeug: Kotlin Playground

Direkt im Browser — kein Setup nötig:

## 👉 [play.kotlinlang.org](https://play.kotlinlang.org)

<div class="pt-8 text-left max-w-md mx-auto">

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

</div>

<div class="pt-6 opacity-75 text-sm">
Jedes Kotlin-Programm startet in der <code>main()</code>-Funktion.<br>
Alles zwischen <code>{</code> und <code>}</code> wird ausgeführt.
</div>

---
layout: section
class: text-center
---

# 📘 Teil 2
## Kotlin Grundlagen

---
layout: two-cols
layoutClass: gap-10
---

# Was ist eine Funktion?

Eine **Funktion** ist ein **Mini-Programm** mit Namen.

<v-clicks>

- Du kannst sie **immer wieder aufrufen**
- Sie macht **eine bestimmte Sache**
- Sie hat einen **Namen**, der beschreibt was sie tut

</v-clicks>

<div v-click class="pt-6 opacity-75 text-sm">
Wie eine Mikrowelle: Knopf drücken (aufrufen) → sie macht ihr Ding.
</div>

::right::

<div class="pt-2">

**Aufbau in Kotlin**

```kotlin
fun begruessen() {
    println("Hallo!")
    println("Wie geht's?")
}
```

<div class="pt-2 text-sm">

| Teil          | Bedeutung                |
| ------------- | ------------------------ |
| `fun`         | „Hier kommt eine Funktion" |
| `begruessen`  | **Name** der Funktion    |
| `()`          | (Eingaben — später)      |
| `{ … }`       | **Was sie tut**          |

</div>

<div v-click class="pt-3">

**Aufrufen:**
```kotlin
begruessen()    // führt den Code drin aus
```

</div>

</div>

---

# `main()` — wo alles startet

Jedes Kotlin-Programm hat **eine besondere Funktion**: `main()`.

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

<v-click>

Sie wird vom Computer **automatisch aufgerufen**, wenn das Programm startet.

</v-click>

<v-click>

<div class="mt-6 p-3 rounded border border-sky-400/40 bg-sky-400/10">
👉 Alles was passieren soll, schreibst du <b>zwischen die <code>{ }</code> von <code>main</code></b>.
</div>

</v-click>

---

# `println` — Ausgabe

Mit `println()` gibst du Werte auf der Konsole aus.

```kotlin
fun main() {
    println("Hallo Welt!")    // Text
    println(42)               // Zahl
    println(3 + 4)            // Berechnung → 7
}
```

<div class="pt-6 opacity-80">
<code>println</code> = <b>print line</b> → gibt eine Zeile aus.
</div>

---
layout: two-cols
layoutClass: gap-10
---

# Variablen — Werte speichern

Variablen = **beschriftete Boxen** für Werte.

```kotlin
var punkte = 0       // veränderbar
val name = "Kotlin"  // fest
```

| Keyword | Bedeutung        | Änderbar? |
| ------- | ---------------- | --------- |
| `var`   | **var**iable     | ✅ Ja     |
| `val`   | **val**ue (Wert) | ❌ Nein   |

::right::

<div class="pt-8">

```kotlin
punkte = 10       // ✅ geht (var)
name = "Java"     // ❌ Fehler (val)
```

<div class="pt-4 opacity-75 text-sm">
Faustregel: Schreibe so oft wie möglich <code>val</code>.<br>
Nur <code>var</code> wenn der Wert sich wirklich ändern muss.
</div>

</div>

---

# Datentypen — Was passt in die Box?

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

<div class="pt-4 opacity-75 text-sm">
Kotlin erkennt den Typ meistens automatisch — man muss ihn oft nicht hinschreiben.
</div>

---

# String Templates

Mit `$` baust du Variablen direkt in Text ein:

```kotlin
val name = "Alex"
val alter = 16

println("Ich heiße $name und bin $alter Jahre alt.")
// → Ich heiße Alex und bin 16 Jahre alt.
```

<v-click>

Für **Berechnungen** → geschweifte Klammern `${...}`:

```kotlin
println("In 2 Jahren bin ich ${alter + 2}.")
// → In 2 Jahren bin ich 18.
```

</v-click>

---
layout: two-cols
layoutClass: gap-10
---

# Mathematische Operationen

```kotlin
println(10 + 3)    // 13   Addition
println(10 - 3)    //  7   Subtraktion
println(10 * 3)    // 30   Multiplikation
println(10 / 3)    //  3   Division (Int!)
println(10 % 3)    //  1   Modulo (Rest)
```

::right::

<div class="pt-8">

### Modulo `%` = der Rest

```text
15 % 5 = 0   → 15 teilbar durch 5
16 % 5 = 1   → Rest 1
```

Perfekt um zu prüfen:<br>
**"Ist eine Zahl durch X teilbar?"**

```kotlin
zahl % X == 0
```

</div>

---

# Vergleiche → `true` / `false`

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
layout: two-cols
layoutClass: gap-10
---

# `for`-Loop — Schleifen

Wiederholt Code eine bestimmte Anzahl von Malen:

```kotlin
for (i in 1..5) {
    println(i)
}
// → 1  2  3  4  5
```

::right::

<div class="pt-8">

| Syntax           | Ergebnis              |
| ---------------- | --------------------- |
| `1..5`           | 1, 2, 3, 4, 5         |
| `1 until 5`      | 1, 2, 3, 4 (ohne 5)   |
| `5 downTo 1`     | 5, 4, 3, 2, 1         |
| `1..10 step 2`   | 1, 3, 5, 7, 9         |

</div>

---

# `if` / `else` — Entscheidungen

```kotlin
val alter = 16

if (alter >= 18) {
    println("Volljährig!")
} else {
    println("Noch nicht 18.")
}
```

<v-click>

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

</v-click>

---
layout: section
class: text-center
---

# 📋 Cheat Sheet
## Grundlagen — bleibt offen!

---

# Cheat Sheet — Grundlagen

<div class="grid grid-cols-2 gap-6 text-sm">

<div>

**Ausgabe & Variablen**
```kotlin
println("Text")        // Ausgabe
var x = 5              // änderbar
val y = "Hi"           // fest
```

**Datentypen & Templates**
```kotlin
Int  String  Boolean  Double
"Hallo $name"
"Summe: ${a + b}"
```

**Operatoren**
```kotlin
+   -   *   /   %        // % = Rest
==  !=  >  <  >=  <=     // → Boolean
```

</div>

<div>

**Schleife**
```kotlin
for (i in 1..100) {
    println(i)
}
```

**Bedingung**
```kotlin
if (bedingung) {
    ...
} else if (bedingung) {
    ...
} else {
    ...
}
```

</div>

</div>

<div class="pt-2 text-center opacity-80">
👉 Lass dieses Sheet offen für die nächsten Aufgaben
</div>

---
layout: section
class: text-center
---

# 🎤 Live Demo
## Wir bauen zusammen ein kleines Programm!

👉 **play.kotlinlang.org**

---

# 🎤 Live Demo — Erste Schritte

**1. Ausgabe & Variablen**

```kotlin
fun main() {
    var x = 0
    println(x)
}
```

<v-click>

**2. Vergleiche**

```kotlin
    println(3 > 7)     // false
    println(3 < 7)     // true
```

</v-click>

<v-click>

**3. Mathe**

```kotlin
    println(6 / 7)     // 0  (Int-Division!)
    println(6f / 7f)   // 0.857...  (Float)
    println(16 % 7)    // 2
```

</v-click>

---

# 🎤 Live Demo — Loops & Bedingungen

**4. For-Loop → Variable hochzählen**

```kotlin
    var x = 0
    for (i in 1..3) {
        x = x + i
    }
    println(x)     // → 6
```

<v-click>

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

</v-click>

<v-click>

<div class="mt-4 p-3 rounded border border-amber-400/40 bg-amber-400/10">
💡 <b>Aufgabe an die Klasse:</b> Was muss der Loop sein, damit <code>x = 120</code> rauskommt?
</div>

</v-click>

---
layout: section
class: text-center
---

# 🖐️ Jetzt seid ihr dran!
## Experimentiert mit `println`, Variablen, Schleifen, `if`/`else`

👉 **play.kotlinlang.org**

<div class="pt-6 opacity-80">
Kaputt machen erlaubt — aus Fehlern lernt man am meisten 💥
</div>

---
layout: section
class: text-center
---

# 🎯 Challenge: FizzBuzz
## Könnt ihr dieses Rätsel knacken?

Das Cheat Sheet bleibt offen — nutzt es!

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Aufgabe 1 — Zahlen ausgeben

Schreibe ein Programm, das die **Zahlen von 1 bis 100** untereinander ausgibt.

**Erwartete Ausgabe:**

```text
1
2
3
4
...
99
100
```

<div v-click>

💡 Tipp: `for`-Loop + `println`

</div>

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun main() {
    for (i in 1..100) {
        println(i)
    }
}
```

<div class="pt-2 opacity-75 text-sm">
<code>1..100</code> erzeugt eine Range von 1 bis einschließlich 100.
</div>

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Aufgabe 2 — Fizz!

Manche Zahlen sollen **übersetzt** werden:

Für **Vielfache von 3** wird `"Fizz"` ausgegeben.

**Erwartete Ausgabe:**

```text
1
2
Fizz
4
5
Fizz
7
...
```

<div v-click>

💡 Tipp: `if` + Modulo (`%`)<br>
→ Wie prüft man "ist durch 3 teilbar"?

</div>

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun main() {
    for (i in 1..100) {
        if (i % 3 == 0) {
            println("Fizz")
        } else {
            println(i)
        }
    }
}
```

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Aufgabe 3 — Buzz!

Zusätzlich: `"Buzz"` bei **Vielfachen von 5**.

**Erwartete Ausgabe:**

```text
1
2
Fizz
4
Buzz
Fizz
7
...
```

<div v-click>

💡 Tipp: `else if` hinzufügen

</div>

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun main() {
    for (i in 1..100) {
        if (i % 3 == 0) {
            println("Fizz")
        } else if (i % 5 == 0) {
            println("Buzz")
        } else {
            println(i)
        }
    }
}
```

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Aufgabe 4 — FizzBuzz!

Zusätzlich: `"FizzBuzz"` bei Zahlen, die **sowohl durch 3 als auch durch 5** teilbar sind.

**Erwartete Ausgabe:**

```text
...
13
14
FizzBuzz
16
...
```

⚠️ Die **Reihenfolge** der `if`-Bedingungen ist entscheidend!<br>
Welche muss **zuerst** geprüft werden?

::right::

<div v-click>

## ✅ Lösung

```kotlin
fun main() {
    for (i in 1..100) {
        if (i % 15 == 0) {            // zuerst!
            println("FizzBuzz")
        } else if (i % 3 == 0) {
            println("Fizz")
        } else if (i % 5 == 0) {
            println("Buzz")
        } else {
            println(i)
        }
    }
}
```

<div class="pt-2 opacity-75 text-sm">
Eine Zahl die durch 3 <b>und</b> 5 teilbar ist, ist auch durch 15 teilbar.
</div>

</div>

---
layout: section
class: text-center
---

# 📘 Teil 3
## Objektorientierte Programmierung

---

# Warum Objektorientierung?

Bisher: Variablen und Funktionen — alles einzeln.

<v-click>

**Problem:** Was wenn wir mehrere Haustiere beschreiben wollen?

```kotlin
// So? Wird schnell unübersichtlich...
var pet1Name = "Fluffy"
var pet1Hunger = 5
var pet1Happiness = 5

var pet2Name = "Rex"
var pet2Hunger = 3
var pet2Happiness = 8
```

</v-click>

<v-click>

<div class="mt-4 p-3 rounded border border-emerald-400/40 bg-emerald-400/10">
<b>Besser:</b> Alles was zusammengehört in einen <b>Bauplan</b> packen → <b>Klasse</b>!
</div>

</v-click>

---

# Klassen = Baupläne

Eine **Klasse** beschreibt, wie ein Ding aufgebaut ist.<br>
Ein **Objekt** ist ein konkretes Exemplar nach diesem Bauplan.

```text
   Klasse "Hund"              Objekte
   ┌──────────────┐
   │ name         │    →    Rex,  Bella,  Lucky
   │ alter        │    →    3,    7,      1
   │ hunger       │    →    5,    2,      8
   │              │
   │ bellen()     │    →    "Wuff!", "Wuff!", "Wuff!"
   │ füttern()    │
   └──────────────┘
```

<div class="pt-4 text-center opacity-80">
Ein Bauplan, <b>beliebig viele</b> Objekte.
</div>

---
layout: two-cols
layoutClass: gap-10
---

# Was steckt in einer Klasse?

Eine Klasse hat zwei Arten von „Inhalt":

<div class="pt-2">

<v-click>

**1. Eigenschaften (Properties)**<br>
→ Wie das Ding **ist** (Zustand)

```text
name, alter, hunger
```

</v-click>

<v-click>

<div class="pt-4">

**2. Methoden**<br>
→ Was das Ding **tun kann** (Verhalten)

```text
bellen(), füttern()
```

</div>

</v-click>

</div>

::right::

<div class="pt-2">

<v-click>

**Im echten Leben** 🐕

| Hund Rex      | In der Klasse        |
| ------------- | -------------------- |
| heißt Rex     | `name = "Rex"`       |
| ist 3 Jahre   | `alter = 3`          |
| kann bellen   | `bellen()`           |
| kann gefüttert werden | `füttern()`  |

</v-click>

<div v-click class="pt-4 opacity-75 text-sm">
👉 Daten und Funktionen, die zusammengehören, leben <b>im selben Objekt</b>.
</div>

</div>

---
layout: two-cols
layoutClass: gap-10
---

# Klasse in Kotlin

```kotlin
class Hund(val name: String) {
    var alter: Int = 3
    var hunger: Int = 5

    fun bellen() {
        println("$name sagt: Wuff!")
    }
}
```

::right::

<div class="pt-2">

| Bestandteil          | Was ist das?              |
| -------------------- | ------------------------- |
| `class Hund`         | Name des Bauplans         |
| `(val name: String)` | Parameter beim Erstellen  |
| `var alter: Int = 3` | Eigenschaft (Property)    |
| `fun bellen()`       | Methode (Funktion drin)   |

</div>

---

# Objekte erstellen & verwenden

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

<v-click>

Der **Punkt `.`** ist der Zugang:

```text
objekt.eigenschaft     → Wert lesen/ändern
objekt.methode()       → Funktion ausführen
```

</v-click>

---

# Die vier Schritte mit Klassen

<div class="grid grid-cols-2 gap-x-10 gap-y-4 pt-2 text-sm">

<div v-click>

**1️⃣ Definieren** — den Bauplan schreiben

```kotlin
class Hund(val name: String) {
    var hunger: Int = 5
}
```

</div>

<div v-click>

**2️⃣ Erstellen** — ein Objekt nach dem Bauplan

```kotlin
val rex = Hund("Rex")
```

</div>

<div v-click>

**3️⃣ Lesen / Ändern** — Properties über `.`

```kotlin
println(rex.hunger)   // lesen
rex.hunger = 3        // ändern
```

</div>

<div v-click>

**4️⃣ Aufrufen** — Methoden ausführen

```kotlin
rex.bellen()
```

</div>

</div>

<div v-click class="pt-6 text-center opacity-80">
👉 Mehr braucht es <b>nicht</b>, um ein digitales Haustier zu bauen.
</div>

---
layout: section
class: text-center
---

# 📋 Cheat Sheet
## Grundlagen + OOP — bleibt offen!

---

# Cheat Sheet — Grundlagen + OOP

<div class="grid grid-cols-2 gap-6 text-sm">

<div>

**Basics**
```kotlin
println("Text")
var x = 5   // änderbar
val y = "Hi" // fest
"Hallo $name"
+  -  *  /  %
==  !=  >  <  >=  <=
```

**Kontrollfluss**
```kotlin
for (i in 1..10) { ... }
if (b) { } else if (b) { } else { }
```

</div>

<div>

**Klassen**
```kotlin
class MeineKlasse(val name: String) {
    var wert: Int = 0
    fun methode() {
        ...
    }
}

val obj = MeineKlasse("Test")
obj.methode()
obj.wert
```

</div>

</div>

<div class="pt-2 text-center opacity-80">
👉 Bleibt offen für die Steckbrief-Aufgabe
</div>

---
layout: section
class: text-center
---

# 🎯 Aufgabe: Steckbrief
## Erstellt euren eigenen digitalen Steckbrief!

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Steckbrief — Aufgabe

Baut eure **eigene Klasse `Steckbrief`** im Playground.

Sie soll **euch beschreiben**:

- Name
- Alter
- Hobby
- … mindestens **2 weitere** Eigenschaften, die zu euch passen

Außerdem soll der Steckbrief sich selbst **vorstellen können** — z.B. mit einer Methode `print()`, die alle Daten auf der Konsole ausgibt.

**Testet** eure Klasse, indem ihr ein Objekt mit euren Daten erstellt und `print()` aufruft.

::right::

<div class="pt-2">

**Ziel-Ausgabe (Beispiel)**

```text
Hallo, ich heiße Alex.
Ich bin 16 Jahre alt.
Mein Hobby ist Zocken.
Mein Lieblingsessen ist Pizza.
Mein Lieblingsfach ist Informatik.
```

<div v-click class="pt-6 p-3 rounded border border-amber-400/40 bg-amber-400/10 text-sm">
🌟 <b>Bonus:</b> Erstellt ein <b>zweites Objekt</b> für euren Sitznachbarn — dieselbe Klasse, andere Daten.
</div>

</div>

---
layout: two-cols
layoutClass: gap-8
---

# 🎯 Steckbrief — Beispiel-Lösung

```kotlin
class Steckbrief(val name: String) {
    var alter: Int = 0
    var hobby: String = ""
    var lieblingsessen: String = ""
    var lieblingsfach: String = ""

    fun print() {
        println("Hallo, ich heiße $name.")
        println("Ich bin $alter Jahre alt.")
        println("Mein Hobby ist $hobby.")
        println("Mein Lieblingsessen ist $lieblingsessen.")
        println("Mein Lieblingsfach ist $lieblingsfach.")
    }
}
```

::right::

<div v-click>

```kotlin
fun main() {
    val ich = Steckbrief("Alex")
    ich.alter = 16
    ich.hobby = "Zocken"
    ich.lieblingsessen = "Pizza"
    ich.lieblingsfach = "Informatik"
    ich.print()

    println("---")

    val nachbar = Steckbrief("Sam")
    nachbar.alter = 15
    nachbar.hobby = "Fußball"
    nachbar.lieblingsessen = "Sushi"
    nachbar.lieblingsfach = "Sport"
    nachbar.print()
}
```

</div>

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

# 🎯 Pet — Aufgabe 2 _(30 min)_
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
layout: two-cols
layoutClass: gap-8
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
layout: section
class: text-center
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

---
layout: section
class: text-center
---

# 📋 Cheat Sheet
## Alles auf einen Blick

---

# Cheat Sheet — Alles auf einen Blick

<div class="grid grid-cols-2 gap-6 text-xs">

<div>

**Ein- & Ausgabe**
```kotlin
println("Text")     // Zeile
print("Text")       // ohne Umbruch
val x = readln()    // Eingabe → String
```

**Variablen & Typen**
```kotlin
var x = 5      // änderbar
val y = "Hi"   // fest
// Int  String  Boolean  Double
"Hallo $name"  "${a + b}"
```

**Operatoren**
```kotlin
+  -  *  /  %         // % = Rest
==  !=  >  <  >=  <=  // → Boolean
```

**Kontrollstrukturen**
```kotlin
for (i in 1..10) { }
while (b) { }
if (b) { } else if (b) { } else { }
when { b -> ... else -> ... }
```

</div>

<div>

**Klassen**
```kotlin
class Name(val p: Typ) {
    var x: Int = 0
    fun m() { }
}

val obj = Name("X")
obj.x
obj.m()
```

**Helfer**
```kotlin
x.coerceIn(0, 10)   // begrenzen
"42".toInt()        // String → Int
```

</div>

</div>

---
layout: center
class: text-center
---

# 🎉 Geschafft!

Ihr habt heute gelernt:

<div class="pt-4 grid grid-cols-2 gap-x-12 gap-y-2 text-left max-w-2xl mx-auto opacity-90">

- ✅ Variablen, Typen, Templates
- ✅ Schleifen & Bedingungen
- ✅ Klassen & Objekte
- ✅ FizzBuzz gelöst
- ✅ Eigenen Steckbrief gebaut
- ✅ Digitales Haustier programmiert

</div>

<div class="pt-10 text-2xl">
Wer weiterprogrammieren will → <a href="https://play.kotlinlang.org">play.kotlinlang.org</a>
</div>

<div class="pt-6 opacity-60 text-sm">
Danke fürs Mitmachen! 🚀
</div>
