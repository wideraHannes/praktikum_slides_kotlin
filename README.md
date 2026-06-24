# Praktikums-Slides — Kotlin

Slides für das Schüler:innen-Praktikum „Einführung in die Programmierung mit Kotlin".
Gebaut mit [Slidev](https://sli.dev/) — Folien als Markdown, live editierbar, mit Hot-Reload.

## Schnellstart

Vorausgesetzt: Node.js (≥ 18) und [pnpm](https://pnpm.io/installation).

```bash
pnpm install      # einmalig: Abhängigkeiten installieren
pnpm dev          # startet den Live-Server auf http://localhost:3030
```

Der Browser öffnet sich automatisch. Änderungen an `slides.md` werden sofort übernommen.

## Während der Präsentation

| Taste            | Funktion                                                       |
| ---------------- | -------------------------------------------------------------- |
| `→` / `Leertaste`| Nächste Folie / nächster Klick-Schritt                         |
| `←`              | Vorherige Folie                                                |
| `o`              | Übersicht aller Folien                                         |
| `d`              | Dark-Mode an/aus                                               |
| `f`              | Vollbild                                                       |
| `g`              | Zu Folie springen (Nummer eingeben)                            |

Presenter-Modus mit Notizen, Timer und Vorschau der nächsten Folie:
<http://localhost:3030/presenter>

## Inhalte ändern

Die Folien liegen in **`slides.md`**. Jede Folie wird durch `---` getrennt.
Eine neue Folie sieht z. B. so aus:

```md
---
layout: default
---

# Überschrift

- Aufzählungspunkt
- Noch einer

<!-- Sprecher-Notizen hier — nur im Presenter-Modus sichtbar -->
```

Weitere nützliche Bausteine:

- **`assets/`** — Bilder (z. B. `![](/assets/kotlin_vs_java.png)`)
- **`components/`** — Vue-Komponenten zum Einbetten (`<Counter />`)
- **`snippets/`** — externer Code, per `<<< @/snippets/external.ts` einbindbar
- **`pages/`** — ausgelagerte Folien, per `src: ./pages/imported-slides.md` einbindbar

Layouts, Animationen (`v-click`, `v-clicks`), Code-Highlighting und mehr:
siehe [sli.dev/builtin/layouts](https://sli.dev/builtin/layouts) und [sli.dev/guide/syntax](https://sli.dev/guide/syntax).

## Export

```bash
pnpm build        # statische HTML-Version nach dist/  → einfach hosten oder zippen
pnpm export       # PDF-Export (braucht Playwright: pnpm dlx playwright install chromium)
```

Die `dist/`-Version reicht zum Verteilen — einfach in einem Browser öffnen, kein Server nötig.

## Tipps für die Praktikumswoche

- **Vor dem Praktikum einmal `pnpm install` laufen lassen** — offline geht's danach auch.
- **Presenter-Modus auf dem Lehrer-Laptop, Folien auf den Beamer** (zweites Browserfenster auf `/`).
- **Demos live im Editor**, nicht aus den Folien — die Folien sind nur das Skript dahinter.
- Inhalt für die Übungen liegt in [`praktikum_content.md`](./praktikum_content.md).

## Fragen?

Slidev-Doku: <https://sli.dev/> — alle Layouts, Themes, Plugins.
Bei projektspezifischen Fragen: gerne im Team kurzschließen.
