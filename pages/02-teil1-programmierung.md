---
layout: section
class: text-center
---

# 📘 Teil 1

## Was ist Programmierung?

---

# Was ist Programmierung?

Computer sind **dumm** — sie können nur genau das tun, was man ihnen<br>**Schritt für Schritt** sagt.

<v-click>

Programmieren = dem Computer **Anweisungen** geben, in einer Sprache die er versteht.

</v-click>

<v-click>

```text
1. Nimm eine Zahl
2. Wenn sie durch 3 teilbar ist → sag "Fizz"
3. Sonst → sag die Zahl
```

</v-click>

<v-click>

<div class="mt-6 text-center opacity-80">
Das ist im Prinzip schon ein Programm.
</div>

</v-click>

---

# Wo steckt überall Programmierung drin?

| Bereich     | Beispiele                                 |
| ----------- | ----------------------------------------- |
| 📱 Apps     | Instagram, WhatsApp, TikTok               |
| 🌐 Websites | YouTube, Google, Wikipedia                |
| 🎮 Spiele   | Minecraft, Fortnite, FIFA                 |
| 🤖 Geräte   | Roboter, Drohnen, Smartwatches            |
| 🚗 Autos    | Autopilot, Einparkhilfe                   |
| 🧠 KI       | ChatGPT, Bilderkennung, Sprachassistenten |

<div class="pt-6 text-center opacity-75">
Praktisch alles, was einen Bildschirm hat (und vieles ohne) wird programmiert.
</div>

---

# Welche Programmiersprachen gibt es?

Hunderte — jede hat ihren Einsatzbereich:

| Sprache    | Typischer Einsatz                       |
| ---------- | --------------------------------------- |
| Python     | KI, Data Science, Automatisierung       |
| JavaScript | Websites, Web-Apps                      |
| Java       | Große Unternehmenssoftware, Android     |
| **Kotlin** | **Android-Apps, Server, Multiplatform** |
| Swift      | iPhone-Apps                             |
| C / C++    | Betriebssysteme, Spiele-Engines         |
| C#         | Spiele (Unity), Windows-Software        |

<div class="pt-4 opacity-75">
Keine Sprache ist <i>"die beste"</i> — es kommt darauf an, <b>was</b> man bauen will.
</div>

---
layout: two-cols
layoutClass: gap-12
---

# Was ist Kotlin?

<v-clicks>

- Moderne Sprache von **JetBrains** (seit 2016 stabil)
- Von **Google** als bevorzugte Sprache für Android empfohlen
- Läuft auf der **JVM** (Java Virtual Machine)
- Klare, lesbare Syntax — weniger Code, gleiches Ergebnis
- Name kommt von der **Insel Kotlin** bei St. Petersburg 🏝️

</v-clicks>

::right::

<div class="pt-8">

**Java**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hallo Welt!");
    }
}
```

**Kotlin**

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

</div>

<div class="pt-4 opacity-70 text-sm">
Kein Semikolon, keine Klassen-Hülle nötig —<br>einfach loslegen.
</div>

---
layout: two-cols
layoutClass: gap-8
---

# Warum Kotlin für uns?

**Zum Lernen**

- Einfach zu lesen und schreiben
- Sofort im Browser testbar → kein Setup
- Fehler werden früh erkannt

**In der echten Welt**

- Offizielle Sprache für Android
- Google, Netflix, Amazon, Uber nutzen Kotlin
- Wächst stark — gute Jobchancen

<div class="pt-3 text-sm opacity-80">
👉 Echte Case Studies: <a href="https://kotlinlang.org/case-studies/" target="_blank">kotlinlang.org/case-studies</a>
</div>

::right::

<div class="pt-8">

**Wann eher etwas Anderes?**

| Aufgabe     | Sprache    |
| ----------- | ---------- |
| Websites    | JavaScript |
| KI          | Python     |
| iPhone-Apps | Swift      |
| 3D-Spiele   | C# / C++   |

</div>

---
layout: center
class: text-center
---

# Unser Werkzeug: Kotlin Playground

Direkt im Browser — kein Setup nötig:

## 👉 [play.kotlinlang.org](https://play.kotlinlang.org)

<div class="pt-8 text-left max-w-md mx-auto">

```kotlin
fun main() {
    println("Hallo Welt!")
}
```

</div>

<div class="pt-6 opacity-75 text-sm">
Jedes Kotlin-Programm startet in der <code>main()</code>-Funktion.<br>
Alles zwischen <code>{</code> und <code>}</code> wird ausgeführt.
</div>
