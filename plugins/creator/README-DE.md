# Creator

Der Agent, der Tools für Allkin baut. Du beschreibst ihm, was du willst; er stellt seine Fragen
in einem **Formular**, schreibt das Tool, den Dienst oder die Fähigkeit nach dem Allkin-Standard,
**prüft** es und debuggt es mit dir. Creator hat keine eigene Seite: Er ist ein Agent in der
Liste der Agenten, mit dem man spricht.

## Wozu es dient

- **Ein Tool erstellen**: ein dauerhaft laufendes Programm, eine Seite, ein Teil der Oberfläche
  von Allkin, ein eigener Agent – oder mehreres zugleich.
- **Einen Dienst erstellen**: Allkin beibringen, wie eine externe API erreicht wird, damit deine
  Agenten sie mit deinem Schlüssel aufrufen.
- **Eine Fähigkeit erstellen**: ein Know-how, das ein Agent bei Bedarf lädt.

Alles, was Creator schreibt, folgt dem **Allkin-Standard**, der mit dem Tool geliefert wird
(`standard/PLUGIN-STANDARD.md`, `standard/SERVICE-STANDARD.md`, `standard/SKILL-STANDARD.md`),
und er prüft es nach jeder Änderung selbst.

## Erste Schritte

1. Installiere Creator und erteile auf seiner Seite seine drei Rechte. Der Agent **Creator** und
   dein lokales Repository werden in diesem Moment angelegt.
2. Öffne die Unterhaltung des Agenten Creator (er steht in der Liste der Agenten, in Rosa wie
   jeder Agent eines Tools) und sag ihm, was du willst.
3. Er stellt seine Fragen auf einmal, in einem Formular; antworte, er schreibt die Dateien, prüft
   sie und sagt dir zum Schluss, was zu tun ist: installieren, ein Recht erteilen, die Seite neu
   laden, den Dienst starten.
4. Um das Geschriebene zu installieren: Seite **Tools**, dein Repository „Creator“ ist eine ihrer
   Quellen; **Installieren**, dann die Rechte auf der Seite des Tools. Ein Dienst wird auf der
   Seite **Dienste** verbunden, eine Fähigkeit auf der Seite **Fähigkeiten**.

## Debuggen

Wenn ein Tool nicht tut, was es soll, sag es Creator: Er liest das Protokoll des Dienstes
(`read_tool_log`), startet die Prüfung erneut (`check_project`), korrigiert, erhöht die Version
und sagt dir, was du erneut tun sollst. Gib ihm den genauen Fehler, den du siehst: Das hilft ihm
am meisten.

## Wo deine Dateien liegen

Im Arbeitsordner des Agenten: `~/.allkin/plugin-data/creator/workspace/`, mit einem Ordner
`plugins/`, einem Ordner `services/` und einem Ordner `skills/`. Dieser Ordner ist ein **lokales
Repository**: Er erscheint im Fenster *Repositorys* der Seiten Tools, Dienste und Fähigkeiten,
und deine Werke werden dort mit dem Etikett „Creator“ aufgeführt.

Dieser Ordner wird **nicht gelöscht**, wenn du Creator deinstallierst. Um ein Werk zu
veröffentlichen, kopiere seinen Ordner in dein Tool-Repository.

## Angeforderte Rechte

| Recht | Warum |
|-------|-------|
| Eigener Agent | Der Agent Creator, der die Dateien schreibt. Er hat außerhalb seines Arbeitsordners keinen Zugriff auf die Maschine |
| Repository | Den Arbeitsordner zu einer Quelle von Tools, Diensten und Fähigkeiten für dieses Allkin machen |
| Netzwerk | Den Agenten die Online-Dokumentation von APIs lesen lassen |

## Wenn es nicht funktioniert

- **Der Agent Creator erscheint nicht**: Ein Recht ist nicht erteilt. Öffne die Seite des Tools.
- **Installieren ändert nichts**: Die Version hat sich nicht geändert. Bitte Creator, sie zu erhöhen.
- **Die Oberfläche des Tools erscheint nicht**: Erteile ihre Rechte auf ihrer Seite und lade neu.
- **Der Agent antwortet nicht**: Prüfe deinen KI-Anbieter in den Einstellungen von Allkin.
