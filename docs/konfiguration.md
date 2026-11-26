# Konfiguration (RelicForge.ini)

Die Datei hat vier Abschnitte.

## [Cfg] – Erkennung und Bewertung

| Gruppe | Beispiele | Bedeutung |
|---|---|---|
| Maße | `TileSize`, `PieceSpacing`, `NextTile` | Größe von Kacheln und Teilen im Bild, relativ zum Feld |
| Zonen | `PieceZoneHalfW`, `NextZoneHalfH` | Suchbereiche für aktuelles und Next-Teil |
| Erkennung | `DarkMax`, `MaskDiff`, `SigMaxDist`, `DotWhite` | Schwellen für Maske und Mustervergleich |
| Ablauf | `AutoIntervalMs`, `UseNext`, `LookaheadK` | Takt des Auto-Modus, Vorausschau |
| Pool | `PoolShift`, `PoolShiftHigh` | Spawn-Regel |
| Hammer | `HammerMargin`, `HammerJunkMargin`, `HammerSoonRule` | Schwellen für die Hammer-Entscheidung |
| Lernmodell | `UseLearnedModel`, `LearnedHammerMargin`, `TenReward` | Zusatzmodell, Belohnung für Stufe 10 |
| Endspiel | `LateSame`, `LateUsable`, `LateDead`, `LateDanger`, `LateGain` … | Gewichte der Bewertung |
| Strafen | `Pen1` bis `Pen10` | Strafe je Stufe |
| Boni | `Brg1` bis `Brg10` | Bonus je Stufe |
| Aufnahme | `RecordingMode` | Verhalten bei Bildschirmaufnahmen |

## [Sig] – gelernte Muster

Pro Stufe gespeicherte Erkennungsmuster. Werden durch Strg+Alt+Zahl ergänzt.

## [Cal] – Kalibrierung

Die sechs kalibrierten Punkte: Feld oben links und unten rechts, aktuelles Teil, Next-Feld, beide Hammer-Felder.

## [Adb] – Emulator-Aufnahme

Schalter und Verbindungsdaten für die Bildaufnahme per ADB. Der Idle-Bot nutzt diesen Weg, um das Skript im Hintergrund laufen zu lassen.

## Hinweise

- Alle Zahlen sind aus Messungen und Tests abgeleitet. Änderungen am besten einzeln machen und im Log prüfen.
- Vor größeren Änderungen eine Sicherungskopie der INI anlegen.
