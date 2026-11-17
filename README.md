# BRAINROT CASINO: Gamble Til You Sigma 🗿

Ein Idle-/Incremental-Gamble-Spiel im maximalen Meme-Stil – als **eine einzige Datei** (`index.html`, Vanilla JS, keine Abhängigkeiten).
Nur Spielwährung: kein echtes Geld, keine Käufe.

## Starten
- `index.html` im Browser öffnen (Doppelklick genügt), **oder**
- lokal servieren: `python3 -m http.server` → http://localhost:8000
- Debug-Modus: `index.html?debug=1` (Button „🐞 DEBUG“ unten rechts: +1M Chips, +1B, Gems, Tokens, Aura, Event, Jackpot …)

## Balancing anpassen
Alle zentralen Werte stehen im `CONFIG`-Objekt ganz oben im `<script>` (Startkapital, Max-Einsatz-Wachstum, XP-Kurve,
House-Edges, Ziel-EVs, Plinko-Testwürfe, Crash-Limits, Offline-Zeit, Pleite-Schutz, Event-Intervalle, Sigma Mode,
Prestige-Schwelle, Soft-Cap für Gewinn-Boni …).

Die Inhalts-Tabellen direkt darunter:
| Was | Konstante |
|---|---|
| Automaten & Croupiers (passiv) | `BOTS` |
| Basis-Shop (Kosten × 1.15) | `SHOP` |
| Spiel-Upgrades | `GAME_UP` |
| Premium (Gems) / VIP-Lounge | `GEM_SHOP` / `VIP` |
| Skill-Tree (54 Knoten) | `SKILLS` |
| Prestige-Baum / Freischaltungen | `PRESTIGE` / `PRESTIGE_UNLOCKS` |
| Erfolge / Quests | `ACH` / `QUEST_POOL` |
| Story, Ticker | `STORY` / `NEWS` |

## Module im Code
`CONFIG · Utils · State · SND (Audio) · FX · Data · Eco (Economy) · Games · Upgrades · Tree · GameEvents · Quests · Ach · Prestige · Mascot · Tut · UI · Stats · Settings · Save · Main`

## Steuerung
- Leertaste: nochmal spielen (Crash: auszahlen)
- 1–8: Spiel wechseln
