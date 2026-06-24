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

| Teil         | Bedeutung                  |
| ------------ | -------------------------- |
| `fun`        | „Hier kommt eine Funktion" |
| `begruessen` | **Name** der Funktion      |
| `()`         | (Eingaben — später)        |
| `{ … }`      | **Was sie tut**            |

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

# Wozu überhaupt Typen?

Ein Typ sagt: **„In dieser Box darf nur DAS rein."**

```kotlin
val alter: Int = 16
alter = "sechzehn"   // ❌ Fehler schon beim Tippen!
```

<v-clicks>

- 🛡️ **Sicherheit** — viele Fehler werden gefunden, **bevor** das Programm läuft
- 🤖 **Autovervollständigung** — die IDE weiß, was du mit dem Wert machen kannst
- 📖 **Lesbarkeit** — man sieht sofort, was eine Variable bedeutet
- ⚡ **Geschwindigkeit** — der Computer weiß genau, wie viel Platz er braucht

</v-clicks>

<v-click>

<div class="pt-4 opacity-80 text-sm">
Sprachen <b>ohne</b> Typen (z.B. Python, JavaScript) sind flexibler — finden Fehler aber oft erst beim Ausführen.
</div>

</v-click>

---
layout: two-cols
layoutClass: gap-10
---

# Typ-Inferenz — Kotlin denkt mit

In **Java** musst du den Typ immer hinschreiben:

```java
int alter = 16;
String name = "Alex";
double pi = 3.14;
boolean cool = true;
```

<div class="pt-3 opacity-75 text-sm">
Doppelt gemoppelt: <code>int</code> steht da, obwohl <code>16</code> offensichtlich eine Ganzzahl ist.
</div>

::right::

<div class="pt-8">

In **Kotlin** reicht der Wert — der Typ wird **erkannt**:

```kotlin
val alter = 16        // → Int
val name = "Alex"     // → String
val pi = 3.14         // → Double
val cool = true       // → Boolean
```

</div>

<div class="pt-4 opacity-80 text-sm">
Der Compiler schaut sich den Wert rechts an und leitet den Typ <b>automatisch</b> ab — <b>Typ-Inferenz</b>.<br>
Weniger tippen, gleiche Sicherheit.
</div>

---

# Wann doch explizit?

Auch in Kotlin schreibst du den Typ manchmal **bewusst** hin:

<v-clicks>

**1. Wenn der Typ nicht aus dem Wert hervorgeht**

```kotlin
val temperatur: Double = 20    // sonst wäre es Int
```

**2. Wenn du den Typ allgemeiner halten willst**

```kotlin
val zahlen: List<Int> = listOf(1, 2, 3)
```

**3. Bei Funktions-Parametern und Rückgaben** — Pflicht!

```kotlin
fun begruessung(name: String): String {
    return "Hallo $name"
}
```

**4. Wenn es die Lesbarkeit verbessert** — z.B. bei langen Ausdrücken

</v-clicks>

<v-click>

<div class="pt-3 text-center opacity-80">
Faustregel: <b>Variablen</b> meistens ohne Typ, <b>Funktionen</b> immer mit.
</div>

</v-click>

---

# 🧠 Quiz — `var` oder `val`? Welcher Typ?

<div class="grid grid-cols-2 gap-x-10 gap-y-8 text-xl pt-6 font-mono">

<div>
  <div>
    <span class="relative inline-block align-baseline" style="min-width: 3.2em">
      <span v-click.hide="1" class="text-gray-400">???</span>
      <span v-click="1" class="absolute left-0 top-0 text-green-400 font-bold">val</span>
    </span>
    name = <span class="text-orange-300">"Lena"</span>
  </div>
  <v-click at="1">
    <div class="opacity-75 text-sm pl-4 pt-1" style="font-family: sans-serif">→ <code>String</code></div>
  </v-click>
</div>

<div>
  <div>
    <span class="relative inline-block align-baseline" style="min-width: 3.2em">
      <span v-click.hide="2" class="text-gray-400">???</span>
      <span v-click="2" class="absolute left-0 top-0 text-green-400 font-bold">var</span>
    </span>
    punkte = <span class="text-blue-300">0</span>
  </div>
  <v-click at="2">
    <div class="opacity-75 text-sm pl-4 pt-1" style="font-family: sans-serif">→ <code>Int</code> (zählt hoch)</div>
  </v-click>
</div>

<div>
  <div>
    <span class="relative inline-block align-baseline" style="min-width: 3.2em">
      <span v-click.hide="3" class="text-gray-400">???</span>
      <span v-click="3" class="absolute left-0 top-0 text-green-400 font-bold">val</span>
    </span>
    pi = <span class="text-blue-300">3.14</span>
  </div>
  <v-click at="3">
    <div class="opacity-75 text-sm pl-4 pt-1" style="font-family: sans-serif">→ <code>Double</code></div>
  </v-click>
</div>

<div>
  <div>
    <span class="relative inline-block align-baseline" style="min-width: 3.2em">
      <span v-click.hide="4" class="text-gray-400">???</span>
      <span v-click="4" class="absolute left-0 top-0 text-green-400 font-bold">var</span>
    </span>
    eingeloggt = <span class="text-purple-300">false</span>
  </div>
  <v-click at="4">
    <div class="opacity-75 text-sm pl-4 pt-1" style="font-family: sans-serif">→ <code>Boolean</code></div>
  </v-click>
</div>

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

| Syntax         | Ergebnis            |
| -------------- | ------------------- |
| `1..5`         | 1, 2, 3, 4, 5       |
| `1 until 5`    | 1, 2, 3, 4 (ohne 5) |
| `5 downTo 1`   | 5, 4, 3, 2, 1       |
| `1..10 step 2` | 1, 3, 5, 7, 9       |

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
