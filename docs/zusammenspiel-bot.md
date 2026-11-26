# Zusammenspiel mit dem Idle-Bot

Der [Idle-Bot für EF2](https://github.com/lulu-830/Idle-Bot-EF2-Doku) kann das Forge-Skript im Hintergrund steuern:

1. Der Bot öffnet das Relic-Forge-Minispiel (über das Konfetti-Symbol im Seitenmenü).
2. Er startet das AutoIt-Skript mit ADB-Aufnahme.
3. Während des Laufs prüft er regelmäßig, ob das Spiel noch läuft und ob der Ergebnisbildschirm „Run Over“ erscheint.
4. Optional startet er danach ein neues Spiel („Play Again“), solange die eingestellte Minute noch nicht erreicht ist.
5. Vor dem Rebirth beendet er das Forge-Skript wieder.

Die Schalter des Skripts (Hammer automatisch, tote Relikte wegschlagen, Stern automatisch, Lernmodell) stehen im Kontrollpanel des Bots und werden in der INI gespeichert. Sie gelten nach einem Neustart des Skripts.
