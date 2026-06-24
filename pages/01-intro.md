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
layout: center
class: text-center
---

<div class="flex flex-col items-center justify-center" style="height: 100%;">

<div class="flex items-center justify-center" style="height: 520px;">

<div
  v-motion
  :initial="{ scale: 3 }"
  :click-1="{ scale: 2 }"
  :click-2="{ scale: 1.45 }"
  :click-3="{ scale: 1 }"
  :transition="{ duration: 750, ease: [0.22, 1, 0.36, 1] }"
  class="relative w-[540px] h-[540px] origin-center"
  style="will-change: transform;"
>

  <div
    v-click="3"
    class="absolute inset-0 rounded-full border-2 border-slate-400/40 bg-slate-400/5 transition-opacity duration-500"
  >
    <div class="absolute top-3 left-1/2 -translate-x-1/2 text-center">
      <div class="text-[13px] uppercase tracking-wider opacity-70">🌍 Software-Entwicklung</div>
      <div class="text-[10px] opacity-75 mt-1 leading-relaxed">
        Android · Spring Boot · Cloud<br>
        Datenbanken · APIs · DevOps
      </div>
    </div>
  </div>

  <div
    v-click="2"
    class="absolute inset-[72px] rounded-full border-2 border-purple-400/50 bg-purple-400/10 transition-opacity duration-500"
  >
    <div class="absolute top-3 left-1/2 -translate-x-1/2 text-center">
      <div class="text-[7px] uppercase tracking-wider opacity-75">🗣️ Programmiersprachen</div>
      <div class="text-[6px] opacity-85 mt-1 leading-relaxed">
        Python · Java · JavaScript<br>
        Swift · C# · Go · Rust
      </div>
    </div>
  </div>

  <div
    v-click="1"
    class="absolute inset-[148px] rounded-full border-2 border-indigo-400/60 bg-indigo-400/15 transition-opacity duration-500"
  >
    <div class="absolute top-2.5 left-1/2 -translate-x-1/2 text-center">
      <div class="text-[5px] uppercase tracking-wider opacity-80">🧩 Kotlin</div>
      <div class="text-[4.5px] opacity-90 mt-1 leading-relaxed">
        Lambdas · Collections<br>
        Null-Safety · Coroutines
      </div>
    </div>
  </div>

  <div class="absolute inset-[220px] rounded-full border-2 border-teal-400/80 bg-teal-400/15 flex items-center justify-center text-center px-2">
    <div>
      <div class="text-[3.5px] uppercase tracking-wider opacity-80">🧱 Fundamentals</div>
      <div class="text-[3.5px] font-medium mt-1.5 leading-snug">
        Variablen · `if`<br>
        Schleifen · Funktionen<br>
        Klassen
      </div>
      <div class="text-[3px] mt-1.5 opacity-70">← unsere 2 Tage</div>
    </div>
  </div>

</div>

</div>

</div>

---
layout: two-cols
layoutClass: gap-6
---

# So sieht Kotlin aus

Ein kleines Programm — wir lesen es **zusammen**.

```kotlin {none|1,20|2|3-4|6-8|10-11|13-19|all}{lines:true}
fun main() {
    val spieler: String = "Mia"
    var punkte: Int = 4
    var bonus: Int = 3

    punkte = punkte * 2
    bonus = bonus + punkte
    punkte = bonus - 5

    println("Hallo $spieler!")
    println("Punkte: $punkte · Bonus: $bonus")

    if (punkte >= 20) {
        println("Legendär! 👑")
    } else if (punkte >= 10) {
        println("Stark! 💪")
    } else {
        println("Übung macht den Meister.")
    }
}
```

::right::

<div class="pt-10 space-y-3 text-sm">

<v-click at="1">

🔧 **`fun main() { ... }`** — eine **Funktion**: Name, runde Klammern für Argumente, geschweifte für den Code.

</v-click>

<v-click at="2">

📦 **`val`** = fest · **Typ** `String` (Text).

</v-click>

<v-click at="3">

📦 **`var`** = änderbar · **Typ** `Int` (Zahl).

</v-click>

<v-click at="4">

➕ **Zuweisungs-Kette** — jede Zeile rechnet mit den **neuen** Werten.

</v-click>

<v-click at="5">

🖨️ **`println(...)`** — Ausgabe; `$spieler` setzt den Wert ein.

</v-click>

<v-click at="6">

🔀 **`if / else if / else`** — wählt **einen** der Zweige.

</v-click>

</div>

<div v-click class="pt-4 text-center text-base">
🧩 <b>Mini-Rätsel:</b> Was steht am Ende auf dem Bildschirm?
</div>
