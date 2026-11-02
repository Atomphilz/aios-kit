---
name: einstufung
disable-model-invocation: true
description: "Legt in vier Fragen fest, wie das AIOS mit dem Nutzer spricht: wie viel es erklärt und welche Wörter es voraussetzt. Schreibt references/sprache.md. Läuft am Tag 1 direkt nach /onboard, zwei Minuten, und erneut, wenn die Stufe nicht mehr passt. Trigger auf \"/einstufung\", \"Sprachstufe\", \"wie viel sollst du erklären\", \"zu technisch\", \"zu einfach\"."
---

## Was dieser Skill tut

Schreibt `references/sprache.md`: die Stufe (Einsteiger, Vertraut, Technisch),
welche Wörter der Nutzer kennt und welche erklärt werden, und die Antworten,
aus denen das folgt. Die CLAUDE.md liest diese Datei bei jedem Gespräch und
richtet jede Antwort danach aus. Fehlt die Datei, gilt Einsteiger.

Es ist keine Prüfung. Sag das im ersten Satz. Wer hier „Einsteiger“ wird, hat
nichts falsch gemacht; die Stufe sagt nur, wie das AIOS redet, nicht, was der
Nutzer kann. Das Wort „Test“ fällt nie.

## Die drei Stufen

| Stufe | Punkte | Was das AIOS tut |
|---|---|---|
| Einsteiger | 0 bis 2 | Erklärt jedes Fachwort im selben Satz. Ein Schritt pro Nachricht. Dateien heißen nach ihrem Sinn. |
| Vertraut | 3 bis 5 | Wörter unter „Kennt“ laufen frei, Wörter unter „Erklären“ bekommen einen Halbsatz. Mehrere Schritte pro Nachricht. |
| Technisch | 6 bis 8 | Keine Einschränkung. |

## Ablauf

### Schritt 1 — Bestand prüfen

Lies `references/sprache.md`, falls vorhanden. Gibt es sie, zeig Stufe und
Datum in einer Zeile und frag, ob die vier Fragen neu gestellt werden sollen
oder nur eine Stufe gesetzt werden soll („Stell mich auf Vertraut“ reicht; dann
Datei anpassen, Anpassung mit Datum und Grund eintragen, fertig).

### Schritt 2 — Vier Fragen, eine nach der anderen

Eröffnung, ein Satz: „Vier kurze Fragen, damit ich weiß, wie viel ich erkläre.
Keine Prüfung, zwei Minuten, jederzeit änderbar.“

Jede Frage mit drei Antworten a, b, c. Der Nutzer antwortet mit Buchstabe oder
in eigenen Worten; ordne eigene Worte selbst zu und sag kurz, wie du sie
verstanden hast.

**Frage 1 — KI-Nutzung.** Wie oft nutzt du ChatGPT, Claude oder Ähnliches?
a) Noch nie oder ein paar Mal (0)
b) Ab und zu, für Texte oder Fragen (1)
c) Fast täglich, auch für die Arbeit (2)

**Frage 2 — Ordner finden.** Wenn ich sage „die Datei liegt im Ordner daily“,
was passiert?
a) Ich würde erst mal fragen, wo das ist (0)
b) Ich finde sie, mit etwas Suchen (1)
c) Ich öffne sie direkt, auch über den Pfad (2)

**Frage 3 — Befehlsfenster.** Hast du schon einmal etwas in ein schwarzes
Befehlsfenster getippt?
a) Nein, noch nie (0)
b) Ein- oder zweimal, nach Anleitung (1)
c) Ja, regelmäßig (2)

**Frage 4 — Wörter.** Welche dieser Wörter könntest du jemandem in einem Satz
erklären? Nur nennen, was wirklich sitzt.
Prompt · Cloud · Browser · Download · Datei und Ordner · Terminal · Pfad ·
Markdown · Skill · Token · Commit · Repository
Bis 4 Wörter: 0 Punkte. 5 bis 8: 1 Punkt. 9 und mehr: 2 Punkte.

Zusätzlich beobachtest du die Sprache der Antworten selbst. Schreibt der Nutzer
„im Terminal“ oder „den Pfad“ von sich aus richtig, ist das ein Signal, das
du in Schritt 3 nennen darfst, aber nicht zählst. Gezählt werden nur die vier
Antworten.

### Schritt 3 — Auswerten

Summe 0 bis 8, Stufe nach Tabelle oben. Liegt die Summe genau auf einer Grenze
(2 oder 5) und die Antworten der Fragen 1 bis 3 widersprechen sich (etwa 0,
0, 2), nenn beide Stufen und lass den Nutzer wählen. Sonst entscheidest du.

### Schritt 4 — Datei schreiben

Schreib `references/sprache.md` in genau dieser Form. Keine andere Datei wird
angefasst.

```markdown
# Sprachstufe

Stufe: Vertraut
Punkte: 5 von 8
Eingestuft: 2026-11-04 (/einstufung)

## Kennt
Prompt, Cloud, Browser, Download, Datei und Ordner

## Erklären
Terminal, Pfad, Markdown, Skill, Token, Commit, Repository

## Antworten
- KI-Nutzung: ab und zu, für Texte oder Fragen
- Ordner finden: mit etwas Suchen
- Befehlsfenster: noch nie

## Anpassungen
(Datum: Stufe oder Wort geändert, Grund. Trägt das AIOS im Alltag ein.)
```

Bei Stufe Technisch bleiben „Kennt“ und „Erklären“ trotzdem gefüllt; die
Listen gelten dann nur als Notiz.

### Schritt 5 — Zeigen und schließen

Zwei bis drei Sätze, bereits im Ton der neuen Stufe: die Stufe, was das im
Alltag heißt, und dass ein Satz wie „zu technisch“ oder „du erklärst zu viel“
jederzeit reicht, um nachzujustieren. Bei Einsteiger und Vertraut ein Hinweis
auf `references/begriffe.md`, zum Lesen oder Ausdrucken. Kein Bericht, keine
Punkte vorlesen, außer der Nutzer fragt.

## Regeln

1. Vier Fragen, nicht mehr. Keine Rückfragen, die nach Prüfung klingen.
2. Nie bewerten. „Einsteiger“ ist eine Einstellung, keine Note.
3. Die Stufe ist eine Arbeitsannahme. Das AIOS darf sie im Alltag nach den
   Regeln in CLAUDE.md anpassen, nur über diese Datei, und sagt es jedes Mal
   in einem Satz.
4. Nur `references/sprache.md` wird geschrieben. Kein Eintrag in `context/`,
   kein Log.
5. Läuft erneut ohne Widerstand: Wer zum zweiten Mal startet, will etwas
   ändern, nicht noch einmal alles beantworten. Schritt 1 fängt das ab.
