---
layout: section
class: text-center
---

# 📋 Cheat Sheet

## OOP — bleibt offen!

---
class: cheatsheet
---

<div class="cheat-head">
  <div class="cheat-title">Kotlin · Cheat Sheet — OOP</div>
  <div class="cheat-sub">Zusatz zu Teil 2 — Klassen, Objekte, Methoden</div>
</div>

<div class="cheat-grid">

<!-- Spalte 1 -->
<div class="cheat-col">

<div class="cheat-card">

**Idee**

Eine **Klasse** ist ein Bauplan.<br>
Ein **Objekt** ist ein konkretes Exemplar.

| Klasse | Objekt |
| --- | --- |
| Bauplan | Exemplar |
| `Hund` | `rex`, `bella` |

</div>

<div class="cheat-card">

**Was steckt in einer Klasse?**

- **Properties** — wie das Ding **ist** (Zustand)
- **Methoden** — was es **tun kann** (Verhalten)

</div>

</div>

<!-- Spalte 2 -->
<div class="cheat-col">

<div class="cheat-card">

**Klasse — Skelett**

```kotlin
class Name(val p: Typ) {
    var eigenschaft: Typ = wert

    fun methode() {
        …
    }
}
```

| Teil | Bedeutung |
| --- | --- |
| `class Name` | Bauplan-Name |
| `(val p: Typ)` | Konstruktor-Parameter |
| `var … = …` | Property (Zustand) |
| `fun …() { … }` | Methode (Verhalten) |

</div>

</div>

<!-- Spalte 3 -->
<div class="cheat-col">

<div class="cheat-card">

**Objekt erstellen**

```kotlin
val a = Name("…")
val b = Name("…")   // beliebig viele
```

</div>

<div class="cheat-card">

**Zugriff mit `.`**

```kotlin
objekt.eigenschaft       // lesen
objekt.eigenschaft = …   // ändern
objekt.methode()         // ausführen
```

<div class="hint">Der <b>Punkt <code>.</code></b> ist der Zugang zum Objekt.</div>

</div>

<div class="cheat-card">

**Methode mit Rückgabe**

```kotlin
fun beschreibung(): String {
    return "…"
}
```

<div class="hint">Rückgabetyp hinter <code>:</code> · <code>return</code> liefert den Wert.</div>

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
  background: #0f172a !important;
  border-radius: 3px;
}
.cheatsheet .cheat-card code {
  font-size: 0.56rem;
}
.cheatsheet .cheat-card ul {
  margin: 0;
  padding-left: 0.9rem;
}
.cheatsheet .cheat-card li {
  margin: 0.05rem 0;
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
