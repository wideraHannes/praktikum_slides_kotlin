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
  <div class="cheat-title">Kotlin · Cheat Sheet</div>
  <div class="cheat-logo" role="img" aria-label="codecentric"></div>
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
    ...
}
else if (bedingung) {
    ...
}
else {
    ...
}

if (zahl % 2 == 0) {
    println("Zahl ist gerade")
}
```

</div>

<div class="cheat-card">

**Schleifen — `for` & `while`**

```kotlin
for (i in 1..5) {
    println(i)
}

while (i < 10) {
    i++
}
```

</div>

<div class="cheat-card">

**Wert begrenzen mit `if`**

```kotlin
if (punkte > 100) {
    punkte = 100
}
if (punkte < 0) {
    punkte = 0
}
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
        eigenschaft = eigenschaft + 1
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

<div class="section-head">⑥ Datenstrukturen</div>

<div class="cheat-card">

**Liste — viele Werte in Reihenfolge**

```kotlin
val obst = mutableListOf("Apfel", "Banane")
obst.add("Kirsche")   // → [Apfel, Banane, Kirsche]
obst[0]               // → "Apfel"
obst.size             // → 3
for (o in obst) { … }
```

</div>

<div class="cheat-card">

**Map — Schlüssel → Wert**

```kotlin
val noten = mutableMapOf("Mathe" to 2)
noten["Mathe"]      = 1     // ändern
noten["Informatik"] = 1     // neu
noten["Mathe"]              // → 1
noten.size                  // → 2
```

</div>

</div>

</div>

<style>
.slidev-layout.cheatsheet {
  padding: 0.1rem 0.5rem 0.25rem;
  background: #ffffff !important;
  color: #1f2937;
  font-size: 0.42rem;
  line-height: 1.15;
  display: flex;
  flex-direction: column;
  gap: 0.05rem;
  overflow: hidden;
}
.cheatsheet .cheat-head {
  border-bottom: 1px solid #e2e8f0;
  padding-bottom: 0.02rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.cheatsheet .cheat-title {
  font-size: 0.62rem;
  font-weight: 600;
  color: #1e293b;
  letter-spacing: -0.01em;
  line-height: 1.1;
}
.cheatsheet .cheat-sub {
  font-size: 0.4rem;
  color: #64748b;
}
.cheatsheet .cheat-logo {
  height: 2.4rem;
  width: 13rem;
  background: url('/codecentric.svg') no-repeat right center;
  background-size: contain;
}
.cheatsheet .cheat-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.2rem;
  flex: 1 1 auto;
  min-height: 0;
}
.cheatsheet .cheat-col {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
  min-width: 0;
}
.cheatsheet .section-head {
  font-size: 0.42rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  padding: 0.05rem 0.24rem;
  border-radius: 2px;
  color: #475569;
  background: #f1f5f9;
  border-left: 2px solid #94a3b8;
  margin-top: 0.6rem;
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
  padding: 0.18rem 0.16rem 0.08rem;
}
.cheatsheet .cheat-card > p {
  margin: 0 !important;
  line-height: 1.15;
}
.cheatsheet .cheat-card > p:first-child,
.cheatsheet .cheat-card > p:first-child strong {
  margin: 0 !important;
  font-size: 0.4rem;
  color: #475569;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  line-height: 1.05;
}
.cheatsheet .cheat-card > p:first-child + pre,
.cheatsheet .cheat-card > p:first-child + .slidev-code {
  margin-top: 0.14rem !important;
}
.cheatsheet .cheat-card > p + pre,
.cheatsheet .cheat-card > p + .slidev-code {
  margin-top: 0.14rem !important;
}
.cheatsheet .cheat-card pre,
.cheatsheet .cheat-card .slidev-code {
  margin: 0 !important;
  padding: 0.08rem 0.18rem !important;
  font-size: 0.38rem !important;
  line-height: 1.18 !important;
  background: #f6f8fa !important;
  border: 1px solid #e2e8f0;
  border-radius: 2px;
}
.cheatsheet .cheat-card code {
  font-size: 0.38rem;
}
.cheatsheet .cheat-card ul {
  margin: 0.03rem 0 0;
  padding-left: 0.5rem;
}
.cheatsheet .cheat-card li {
  margin: 0;
}
.cheatsheet .cheat-card table {
  width: 100%;
  font-size: 0.4rem;
  border-collapse: collapse;
  margin: 0.04rem 0;
}
.cheatsheet .cheat-card table + pre,
.cheatsheet .cheat-card pre + table {
  margin-top: 0.05rem !important;
}
.cheatsheet .cheat-card th,
.cheatsheet .cheat-card td {
  padding: 0 0.14rem;
  border-bottom: 1px solid #f1f5f9;
  text-align: left;
  line-height: 1.15;
}
.cheatsheet .cheat-card th {
  color: #64748b;
  font-weight: 500;
  font-size: 0.36rem;
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.cheatsheet .cheat-card td code {
  background: #f1f5f9;
  padding: 0 0.1rem;
  border-radius: 2px;
}
.cheatsheet .hint {
  font-size: 0.38rem;
  color: #64748b;
  margin-top: 0.03rem;
}
.cheatsheet .hint code {
  background: #f1f5f9;
  padding: 0 0.08rem;
  border-radius: 2px;
}
</style>
