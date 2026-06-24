---
layout: section
class: text-center
---

# 📘 Teil 1

## Was ist Programmierung?

---

# Was ist Programmierung?

Programmieren = eine **menschlich lesbare Schicht**, um dem Computer Anweisungen zu geben.

<div class="grid grid-cols-[1fr_auto_1.3fr_auto_1fr] items-center gap-3 mt-10">

<div class="rounded-xl border border-teal-400/40 bg-teal-400/5 p-5 text-center">
  <div class="text-xs uppercase tracking-wider opacity-60 mb-2">🧑 Mensch</div>
  <div class="font-medium">„Begrüße die Welt"</div>
</div>

<div class="text-3xl opacity-50 text-center">→</div>

<div class="rounded-xl border border-indigo-400/40 bg-indigo-400/5 p-4 text-center">
  <div class="text-xs uppercase tracking-wider opacity-60 mb-2">📝 Code (Kotlin)</div>

```kotlin
println("Hallo Welt!")
```

</div>

<div class="text-3xl opacity-50 text-center">→</div>

<div class="rounded-xl border border-slate-400/40 bg-slate-400/5 p-5 text-center">
  <div class="text-xs uppercase tracking-wider opacity-60 mb-2">⚙️ Maschine</div>
  <div class="font-mono text-xs leading-relaxed opacity-80">01001000 01100001<br>01101100 01101100<br>01101111 00100000...</div>
</div>

</div>

<v-click>

<div class="mt-10 text-center opacity-80">
Der Computer versteht nur <b>Nullen und Einsen</b>.<br>
Programmiersprachen sind die <b>Brücke</b> zwischen unserer Idee und der Maschine.
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
