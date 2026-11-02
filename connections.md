# Verbindungen

Verzeichnis aller Systeme, die das AIOS erreichen kann. Füllt `/onboard` aus den Antworten Q4 bis Q7; wächst, wenn du neue Werkzeuge anschließt. `/audit` prüft diese Datei auf Abdeckung und Aktualität.

| # | Bereich | Werkzeug | Zugang | Auth | Zuletzt geprüft |
|---|---|---|---|---|---|
| 1 | Umsatz / Finanzen | _füllt /onboard_ | noch nicht verbunden | — | — |
| 2 | Kundenkontakt | _füllt /onboard_ | noch nicht verbunden | — | — |
| 3 | Kalender | _füllt /onboard_ | noch nicht verbunden | — | — |
| 4 | Kommunikation | _füllt /onboard_ | noch nicht verbunden | — | — |
| 5 | Aufgaben / Projekte | _füllt /onboard_ | noch nicht verbunden | — | — |
| 6 | Besprechungen | _füllt /onboard_ | noch nicht verbunden | — | — |
| 7 | Wissen / Dateien | _füllt /onboard_ | noch nicht verbunden | — | — |

**Zugangsarten:** `lokal` (Dateien und Ordner auf diesem Rechner), `mcp` (MCP-Server), `script` (kleines Skript in `scripts/`, das eine Schnittstelle anspricht), `export` (regelmäßiger CSV- oder JSON-Export), `key+ref` (Schlüssel in `.env` plus Anleitung in `references/<werkzeug>-api.md`), `noch nicht verbunden`, `nur Mensch` (Telefon, WhatsApp, Papier: das AIOS kommt nicht heran, der Mensch trägt ein).

Wenn du ein neues Werkzeug anschließt, lege dazu `references/<werkzeug>-api.md` an: Zugang, Anmeldung, typische Abfragen. Einmal recherchiert, für immer gespeichert.
