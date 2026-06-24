---
layout: section
class: text-center
---

# 📋 Cheat Sheet

## Grundlagen — bleibt offen!

---
class: cheatsheet
---

<div class="cheat-head">
  <div class="cheat-title">Kotlin · Cheat Sheet — Grundlagen</div>
  <div class="cheat-sub">Kurzreferenz zu allen Konzepten aus Teil 2</div>
</div>

<div class="cheat-grid">

<!-- Spalte 1 -->
<div class="cheat-col">

<div class="cheat-card">

**Funktion — Bestandteile**

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

**Funktion aufrufen**

```kotlin
fun main() {
    val text = gruss("Tom") // Rückgabe speichern
    println(text)
}
```

</div>

<div class="cheat-card">

**Ausgabe**

```kotlin
println("Text")   // mit Umbruch
print("…")        // ohne
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

</div>

<!-- Spalte 2 -->
<div class="cheat-col">

<div class="cheat-card">

**Datentypen**

| Typ       | Beispiel  |
| --------- | --------- |
| `Int`     | `42`      |
| `Double`  | `3.14`    |
| `String`  | `"Hallo"` |
| `Boolean` | `true`    |

</div>

<div class="cheat-card">

**Typ-Inferenz · Typ explizit**

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

</div>

<!-- Spalte 3 -->
<div class="cheat-col">

<div class="cheat-card">

**Vergleiche → Boolean**

```kotlin
==  !=                // gleich / ungleich
<   <=   >   >=       // kleiner / größer
```

</div>

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

</div>

</div>

<style>
.slidev-layout.cheatsheet {
  padding: 0.7rem 1rem 0.6rem;
  background: #ffffff !important;
  color: #1f2937;
  font-size: 0.6rem;
  line-height: 1.25;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  overflow: hidden;
}
.cheatsheet .cheat-head {
  border-bottom: 1px solid #e2e8f0;
  padding-bottom: 0.25rem;
}
.cheatsheet .cheat-title {
  font-size: 0.9rem;
  font-weight: 600;
  color: #1e293b;
  letter-spacing: -0.01em;
}
.cheatsheet .cheat-sub {
  font-size: 0.58rem;
  color: #64748b;
  margin-top: 0.05rem;
}
.cheatsheet .cheat-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.4rem;
  flex: 1 1 auto;
  min-height: 0;
}
.cheatsheet .cheat-col {
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  min-width: 0;
}
.cheatsheet .cheat-card {
  background: #ffffff;
  border: 1px solid #e2e8f0;
  border-radius: 4px;
  padding: 0.28rem 0.45rem 0.35rem;
}
.cheatsheet .cheat-card > p:first-child,
.cheatsheet .cheat-card > p:first-child strong {
  margin: 0 0 0.2rem 0;
  font-size: 0.58rem;
  color: #475569;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.cheatsheet .cheat-card pre,
.cheatsheet .cheat-card .slidev-code {
  margin: 0 !important;
  padding: 0.3rem 0.45rem !important;
  font-size: 0.56rem !important;
  line-height: 1.3 !important;
  background: #f6f8fa !important;
  border: 1px solid #e2e8f0;
  border-radius: 3px;
}
.cheatsheet .cheat-card code {
  font-size: 0.56rem;
}
.cheatsheet .cheat-card table {
  width: 100%;
  font-size: 0.58rem;
  border-collapse: collapse;
  margin-top: 0.25rem;
}
.cheatsheet .cheat-card th,
.cheatsheet .cheat-card td {
  padding: 0.06rem 0.3rem;
  border-bottom: 1px solid #f1f5f9;
  text-align: left;
}
.cheatsheet .cheat-card th {
  color: #64748b;
  font-weight: 500;
  font-size: 0.54rem;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.cheatsheet .cheat-card td code {
  background: #f1f5f9;
  padding: 0 0.2rem;
  border-radius: 2px;
}
.cheatsheet .hint {
  font-size: 0.55rem;
  color: #64748b;
  margin-top: 0.2rem;
}
.cheatsheet .hint code {
  background: #f1f5f9;
  padding: 0 0.15rem;
  border-radius: 2px;
}
</style>
