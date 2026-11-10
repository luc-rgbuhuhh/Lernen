# Lern-Workspace

Dieses Repository ist mein Lern-Workspace für den Skill `/teach`
(`.claude/skills/teach/`, von Matt Pocock, MIT-Lizenz).
Jedes Fach hat einen eigenen Ordner unter `faecher/`.

## Aufbau

```
eingang/                  ← hier lade ich neue Unterlagen hoch
faecher/<fach>/           ← Teaching-Workspace eines Fachs (für /teach)
  unterlagen/             ← meine Kursunterlagen (Primärquellen)
  MISSION.md  RESOURCES.md  NOTES.md  GLOSSARY.md
  lessons/  reference/  learning-records/  assets/
NOTES.md                  ← meine Lernregeln, gelten für alle Fächer
```

## Regeln für Claude

- Antworte auf Deutsch, auch wenn der Skill auf Englisch geschrieben ist.
  Lektionen, Referenzen und Lernnotizen ebenfalls auf Deutsch.
- **Lies vor jeder Session die `NOTES.md` im Hauptordner.** Dort stehen meine
  Lernregeln. Sie gehen dem `/teach`-Skill vor.
- Suche zuerst in meinen Unterlagen und im Workspace des Fachs, dann nur in
  seriösen Quellen.
- Sag offen, wenn du dir bei einer Aussage nicht zu 99,99 % sicher bist.
- Gib mir nicht einfach recht, sondern antworte wahrheitsgemäß.

## Wenn ich `/teach` aufrufe

1. **Fach bestimmen.** Aus meiner Nachricht (z. B. `/teach Statistik`). Ist es
   unklar, frag nach. Ordnername: klein, ohne Umlaute und Leerzeichen
   (`Lineare Algebra` → `faecher/lineare-algebra/`).
2. **Workspace festlegen.** Alle Pfade, die der Skill relativ zum
   aktuellen Ordner nennt (`MISSION.md`, `lessons/` usw.), beziehen sich auf
   `faecher/<fach>/`, nicht auf den Hauptordner. Gibt es den Ordner noch
   nicht, leg ihn an.
3. **Eingang sortieren.** Liegen Dateien in `eingang/`, frag, zu welchem Fach
   sie gehören (wenn es nicht eindeutig ist), und verschieb sie nach
   `faecher/<fach>/unterlagen/`. Die `README.md` in `eingang/` bleibt liegen.
4. Dann weiter nach `NOTES.md` und dem Skill.

## Lernstand sichern

Die Sitzungen laufen meist in der Cloud und sind flüchtig.
Am Ende jeder Lerneinheit (neue Lektion, Learning Record, geänderte Mission,
sortierte Unterlagen): alle Änderungen committen und auf den aktuellen Branch
pushen, damit der Lernstand beim nächsten Mal da ist.
