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
