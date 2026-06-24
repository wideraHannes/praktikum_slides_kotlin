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
