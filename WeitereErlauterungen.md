# Weiterführende Erklärungen

## Unterschied von Daten und Metadaten
Bei dem Begriff Daten denken die meisten an die Anwendungsdaten. Bei Metadaten wird durch die Vorsilbe Meta klar, dass es sich um etwas handelt, was diesen Anwendungsdaten übergeordnet ist. Metadaten bezeichnet Daten, welche die Struktur der Anwendnungsdaten beschreibt.
Der Unterschied zwischen Daten und Metadaten ist immer abhängig vom Standpunkt des Betrachters.
Im Fall BIMeta wird der Unterschied zwischen Daten und Metadaten an einem Bespiel klar. In einer Merkmalsliste einer Tür steht folgendes:
Farbe = braun
Hier ist "braun" der Datenwert und "Farbe" der Metadatenwert.

## Unterschied von Maßen und Einheiten


## Semantische Versionierung

BIMeta versioniert nach der [Semantische Versionierung](https://semver.org/).

**Version 1.2.3 (Major, Minor, Patch)**

**Major**: Inkompatible Changes, Veränderung der Bedeutung, welche sich auch auf die Benutzung auswirken
   - Bei jedem Major-Change muss das Merkmal ersetzt werden, weil das alte Merkmal in der alten Version unverändert benutzt werden können muss.
   - Nachfolgendes Merkmal

**Minor**: Anpassung der Bedeutung, welche die Benutzung aber in keiner Weise einschränkt.
   - Der Datenaustausch ist nicht beeinträchtigt

**Patch**: Beseitigung eines Tippfehlers, einer (Sprachlichen) Korrektur in der Definition oder in den Beispielen oder das Hinzufügen eins neuen Beispiels
   - Bedeutung ändert sich in keiner Weise
   - Kein Grund das Merkmal abzukündigen, Verbesserung im laufenden Betrieb
