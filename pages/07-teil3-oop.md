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

| Hund Rex              | In der Klasse  |
| --------------------- | -------------- |
| heißt Rex             | `name = "Rex"` |
| ist 3 Jahre           | `alter = 3`    |
| kann bellen           | `bellen()`     |
| kann gefüttert werden | `füttern()`    |

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

| Bestandteil          | Was ist das?             |
| -------------------- | ------------------------ |
| `class Hund`         | Name des Bauplans        |
| `(val name: String)` | Parameter beim Erstellen |
| `var alter: Int = 3` | Eigenschaft (Property)   |
| `fun bellen()`       | Methode (Funktion drin)  |

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
