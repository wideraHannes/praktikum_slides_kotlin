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
