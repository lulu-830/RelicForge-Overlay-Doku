# Bedienung

## Tasten (NumLock an)

| Taste | Funktion |
|---|---|
| Numpad 0 | Jetzt analysieren. Bestätigt auch die Kalibrierung |
| Numpad 1 | Auto-Modus an/aus (analysiert in festem Abstand, `AutoIntervalMs`) |
| Numpad 2 | Overlay an/aus |
| Numpad 3 | Kalibrierung neu starten |
| Numpad 4 | Nächste Alternative (die fünf besten Züge) |
| Numpad 5 | Debug-Anzeige |
| Numpad 6 | Hammer automatisch oder manuell |
| Numpad 7 / 8 | Hammer −1 / +1 (im manuellen Modus) |
| Numpad 9 | Hilfe |
| Numpad Punkt | Aktuellen Vorschlag als schlecht markieren (Log und Screenshot) |
| Strg+Alt+1 bis 9, 0 | Relikt unter der Maus als Stufe 1 bis 10 lernen |
| Strg+Alt+Q | Beenden |

## Einrichtung

1. AutoIt installieren, Spiel im Fenster- oder Borderless-Modus starten.
2. Das Skript starten. Beim ersten Mal führt eine Kalibrierung durch **sechs Punkte**: Feld oben links, Feld unten rechts, aktuelles Teil, Next-Feld und die beiden Hammer-Felder. Die Bestätigung erfolgt über Numpad 0.
3. Die Kalibrierung wird in der INI gespeichert (Abschnitt `Cal`).
4. Die Erkennungsmuster aller 10 Stufen sind vorbelegt. Bei Fehlern lässt sich nachlernen: Maus über das Relikt, dann Strg+Alt+Zahl.

## Typischer Ablauf im Spiel

1. Neues Spiel starten, Numpad 1 für den Auto-Modus.
2. Das Overlay zeigt, wohin das Teil gehört und wie es gedreht wird.
3. Der Spieler setzt das Teil selbst.
4. Gefällt ein Vorschlag nicht, Numpad 4 für die nächste Alternative oder Numpad Punkt zum Markieren.
5. Bei Bedarf Numpad 6 und 7/8 für den Hammer.

## Forge Toolbox

Ein kleines Fenster mit einem Schalter für das Overlay. Praktisch, wenn kein Ziffernblock zur Hand ist.

## Aufnahmemodus

`RecordingMode` legt fest, wie sich das Overlay bei Bildschirmaufnahmen verhält: Es blinkt entweder kurz, oder es bleibt ausgeblendet, damit Videos sauber sind.
