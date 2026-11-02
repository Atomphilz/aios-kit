# EXPANSIONS — was dazukommt, wenn du wächst

Das Kit ist absichtlich schlank: acht Skills, ein paar Kontext- und Referenzdateien. Wenn etwas Neues dazukommt, nutze `/link`, damit das AIOS es findet, und `/audit`, um zu prüfen, dass alles noch auffindbar und aktuell ist.

Das AIOS soll aussehen wie ein kleiner, gut geführter Betrieb. Nicht wie ein Keller voller Kisten.

---

## Was im Kit steckt (nicht entfernen)

| Ordner / Datei | Zweck |
|---|---|
| `context/` | Über dich, dein Geschäft, deine Prioritäten. Füllt `/onboard`. |
| `references/` | Frameworks, Tonfall-Proben, Anleitungen zu Werkzeugen, Abläufe. |
| `references/tagesritual.md` | Konfiguration des Tagesrituals. Schreibt `/day-setup`. |
| `daily/` | Eine Datei pro Tag. Schreiben `/day-close` und `/day-open`. |
| `decisions/log.md` | Fortlaufendes Protokoll: was entschieden wurde und warum. |
| `brainstorms/` | Gespeicherte `/grill-me`-Interviews. Entsteht beim ersten Lauf. |
| `audits/` | Datierte Prüfberichte. Entsteht beim ersten `/audit`. |
| `archives/` | Altes. Nicht löschen, hierher verschieben. |
| `connections.md` | Verzeichnis aller Systeme, die das AIOS erreicht. |
| `.claude/skills/` | Die Skills. Neue nur, wenn sie ein echtes Problem lösen. |
| `aios-intake.md` | Quelldatei für `/onboard`. Ändern und erneut laufen lassen. |
| `CLAUDE.md` | Das Betriebshandbuch. Füllt `/onboard`. Ändern, wenn sich Rolle oder Tonfall ändern. |

---

## Was dazukommt, wenn du wächst

| Ordner / Datei | Wann | Warum |
|---|---|---|
| `projekte/` | Zwei oder mehr laufende Vorhaben mit eigenem Kontext | Aktive Projekte brauchen ihren eigenen Platz, getrennt von den Dauerdateien in `context/` |
| `vorlagen/` | Du kopierst dieselben Texte oder Prompts zum dritten Mal | Wiederverwendbare Ausgangspunkte, weniger Abweichung |
| `references/ablaeufe/` | Du beschreibst, wie ein wiederkehrender Vorgang läuft | Das AIOS liest den Ablauf und hält sich daran |
| `references/<werkzeug>-api.md` | Du schließt ein neues Werkzeug an | Einmal recherchiert, für immer gespeichert; `/audit` rechnet es an |
| `scripts/` | Du brauchst ein kleines Skript für ein System ohne fertige Anbindung | Die zweite Verbindung ist bei den meisten ein Skript |
| `.claude/agents/` | Du brauchst einen Hilfsagenten für wiederkehrende Recherche oder Texte | Agenten laufen in eigenem Kontext; die Hauptsitzung bleibt schlank |

---

## Empfohlener Rhythmus

| Wann | Was |
|---|---|
| Täglich | `/day-close` abends, `/day-open` morgens |
| Tag 7 | `/audit` |
| Wöchentlich | `/level-up`, danach `/audit` |
| Bei Bedarf | `/grill-me`, `/link` |

Baue nichts, was manuell noch nicht funktioniert.
