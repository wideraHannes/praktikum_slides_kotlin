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
