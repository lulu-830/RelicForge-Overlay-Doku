# Bewertung und Simulator

## Prinzip

Für jede mögliche Platzierung (Position und Drehung) wird das Brett nach dem Zug simuliert, einschließlich aller Verschmelzungen und Ketten. Das Ergebnis wird mit einer Zahl bewertet. Dabei schaut das Programm mit `LookaheadK` auf das **Next-Teil** voraus, damit ein Zug nicht den nächsten verbaut.

Die fünf besten Züge stehen zur Wahl (Numpad 4).

## Bewertungsmerkmale

Die Bewertung setzt sich aus mehreren Teilen zusammen, deren Gewichte in der INI stehen. Die Liste beschreibt Aufbau und Parameter, die genauen Formeln sind hier nicht wiedergegeben:

- Punkte durch Verschmelzungen und Ketten
- Hammer-Ladungen, die ein Zug einbringt
- Freie Zellen und Gefahr, das Brett zu füllen (`LateDanger`, `LateDead`)
- Zahl nutzbarer Relikte (`LateUsable`) und toter Relikte
- Bonus je Stufe für bestimmte Konstellationen (Parameter `Brg…`)
- Strafen für hohe Stufen, die blockieren (`Pen…`)
- Ein Bonus fürs Hämmern im Endspiel (`LateHamBonus`)

Außerdem gibt es ein **Lernmodell** (`UseLearnedModel`), das Hammer-Entscheidungen aus früheren Läufen mit einfließen lässt.

## Rechenzeit

Je nach Füllung des Bretts dauert eine Berechnung ein bis drei Sekunden.

## Simulator

Zum Abstimmen der Gewichte wurde ein Simulator gebaut, der viele Läufe automatisch spielt. Mit der aktuellen Bewertung erreichte er **Stufe 9 in rund 9 von 10 Spielen** und **Stufe 10 in etwa 6 bis 8 Prozent**. Vier zusätzliche Bewertungsmerkmale brachten dort keine Verbesserung und wurden nicht übernommen.

## Hammer-Strategie

- **Automatisch:** das Programm entscheidet, wann ein Hammer lohnt (`HammerMargin`, `HammerJunkMargin`)
- **Manuell:** der Spieler zählt die Ladungen mit Numpad 7 und 8
- Toter Ballast wird bevorzugt entfernt, wenn der Schalter dafür aktiv ist
