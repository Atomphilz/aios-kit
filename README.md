# aiOS Kit

Ein Startpaket, das Claude Code in dein persönliches **AI Operating System** verwandelt: ein Ordner, der weiß, wer du bist, was du tust, was gerade zählt, und der jeden Tag mit einem Plan beginnt.

Das Kit ist für Solo-Selbstständige und kleine Betriebe gebaut. Es braucht keine Programmierkenntnisse. Du beantwortest Fragen, das AIOS schreibt die Dateien.

## Was drin ist

| Skill | Wann |
|---|---|
| `/onboard` | Tag 1, direkt nach dem Herunterladen. Sieben Fragen. |
| `/einstufung` | Tag 1, direkt nach `/onboard`. Vier Fragen, zwei Minuten: wie viel das AIOS erklärt. |
| `/day-setup` | Einmal, nach `/onboard`. Richtet das Tagesritual ein. |
| `/day-close` | Jeden Abend, etwa fünf Minuten. Schließt den Tag, plant morgen. |
| `/day-open` | Jeden Morgen, eine Minute. Liest den Plan vor. |
| `/grill-me` | Wenn das AIOS mehr über dich wissen soll. |
| `/link` | Wenn ein neuer Ordner oder eine Quelle dazukommt. |
| `/audit` | Tag 7, dann wöchentlich. Zeigt, was fehlt. |
| `/level-up` | Wöchentlich. Eine Automatisierung pro Woche. |

## Erste Schritte

1. Claude Code installieren (Anleitung: https://docs.claude.com/claude-code).
2. Dieses Kit herunterladen (grüner Knopf „Code“ → „Download ZIP“) und in einen Ordner entpacken, zum Beispiel `Dokumente/aiOS`. Oder klonen, falls Git da ist.
3. Ein Terminal in diesem Ordner öffnen und `claude` starten.
4. `/onboard` eingeben. Sieben Fragen, dann steht die Grundlage.
5. `/einstufung` eingeben. Vier Fragen, dann weiß das AIOS, wie viel es erklärt.
6. `/day-setup` eingeben. Höchstens sieben Fragen, dann steht das Tagesritual.
7. Heute Abend `/day-close`, morgen früh `/day-open`.

## Wie es gedacht ist

- **Context, Connections, Capabilities, Cadence.** Erst muss das AIOS dich kennen, dann deine Systeme erreichen, dann Abläufe beherrschen, dann von allein laufen. In dieser Reihenfolge.
- **Struktur vor Automatisierung.** Was manuell nicht funktioniert, wird automatisiert nicht besser.
- **Erst zeigen, dann schreiben.** Nichts geht nach außen, ohne dass du es gesehen hast.

Die Dateien sind einfaches Markdown. Du kannst alles mit einem Texteditor ändern.

## Lizenz und Herkunft

Dieses Kit basiert auf dem [AIS-OS-Starter-Kit von Nate Herk](https://github.com/nateherkai/AIS-OS), MIT-Lizenz. Die Datei `LICENSE` ist unverändert übernommen; die Skills `/onboard`, `/grill-me`, `/link`, `/audit` und `/level-up` sowie `references/3ms-framework.md` stammen von dort. „The Three Ms of AI™“ und „The Four Cs of an AI OS™“ sind Marken von Nate Herk.

Die Skills `/einstufung`, `/day-setup`, `/day-close` und `/day-open` sowie die deutsche Fassung der Anleitungen sind eigene Ergänzungen und stehen unter derselben MIT-Lizenz.
