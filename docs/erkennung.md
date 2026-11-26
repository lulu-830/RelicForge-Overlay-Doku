# Erkennung

Das Programm erkennt alles aus dem Bild, ohne in den Spielspeicher zu schauen.

## Was gelesen wird

- **Brett:** die 23 Zellen, je eine Stufe oder leer
- **Aktuelles Teil:** Form, Stufen der Relikte, Drehung
- **Next-Teil:** kleiner dargestellt, eigene Maße (`NextTile`, `NextSpacing`)
- **Hammer-Ladungen:** über die beiden kalibrierten Hammer-Felder
- **Stern-Automatik:** eigener Schalter in der INI

## Wie ein Relikt erkannt wird

Jede Zelle wird aus dem Bild geschnitten, dunkler Hintergrund wird maskiert (`DarkMax`, `MaskDiff`), und die Pixel werden mit gespeicherten **Mustern** (Signaturen) verglichen. Der Abstand muss unter einer Schwelle liegen (`SigMaxDist`, für Teile `SigMaxDistPiece`).

Unbekannte Kacheln werden gezählt und im Log aufgeführt. Mit Strg+Alt+Zahl lernt man das Muster eines Reliktes nach.

## Bildquellen

- **Fensteraufnahme:** direkt vom Spielfenster
- **ADB-Aufnahme:** Screenshots aus einem Emulator, nötig, wenn die Fensteraufnahme schwarze Bilder liefert. Einstellungen im Abschnitt `Adb` der INI.

## Instabile Aufnahmen

Wirkt ein Bild unvollständig (zum Beispiel mitten in einer Animation), meldet das Log `UNSTABLE`, und die Analyse wird wiederholt.
