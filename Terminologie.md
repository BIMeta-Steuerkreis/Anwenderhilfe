# Terminologie

* TOC
{:toc}

<br>

![Strukturen zur Verwaltung von Metadaten](https://user-images.githubusercontent.com/77831068/118447853-8afad500-b6f1-11eb-875c-bbe8e09d8058.png)


## Publisher - Herausgeber

Ein Herausgeber ist eine Organisation, welche Digitale Standards mit dem Schwerpunkt der BIM-Methodik für ihr Klientel bzw. ihre Mitglieder veröffentlichen möchte. Er kann die Inhalte selbstständig, frei und im eigenen Namen veröffentlichen. Er ist nicht gezwungen diese Standards mit anderen Herausgebern abzustimmen. Er kann die Inhalte zu anderen Herausgebern mappen.
Die Standards werden in Domänen strukturiert.
Der Content (z.B. mehrere Domänen und Klassifikationssysteme), der von einem Herausgeber erzeugt und veröffentlicht wird, muss innerhalb des Herausgebers eineindeutig und widerspruchsfrei sein.

## Domain - Domäne

Eine Domäne ist ein fachlich in sich abgeschlossener Bereich (ein Bereich für eine bestimmte Fachlichkeit), in dem der Herausgeber mehrere Klassifikationssysteme veröffentlichen kann, welche viele Klassen und Merkmale besitzt. 
Die Domäne gruppiert bzw. selektiert verschiedene thematische Aspekte, welche vom Herausgeber bestimmt werden.

Eine Domäne kann n Klassifikationssysteme haben und ein Klassifikationssystem kann n Klassen haben und eine Klasse kann n Merkmale haben.

## ClassificationSystem - Klassifikationssystem 

Ein Klassifikationssystem sammelt Klassen, welche eine gleichartige Ausrichtung haben, basierend auf dem Verfahren nach VDI 2552-9. Es klassifiziert bzw. gruppiert Dinge nach einem bestimmten vorher festzulegenden Aspekt.
Typischerweise besteht ein Klassifikationssystem aus einer Liste von Klassen und mit diesen verbundenen Merkmalen.

Für das Festlegen der Klassifikationssysteme ist wichtig: | Beispiel: Raumnutzungsarten nach DIN 277 
--------------------------------------------------------- | ----------------------------------------
das Klassifikationselement | Räume
der Klassifikationsaspekt | Nutzungsart
die Klasse | Büroräume

Ein Klassifikationssystem kann auch nur aus einer Liste von Merkmalen bestehen.
In jedem Klassifikationssystem werden die deutschen als auch die englischen Übersetzungen eingepflegt, wobei die Herausgebersprache im Feld ClassificationArea hinterlegt wird. 
Jedes Klassifikationssystem besitzt Klassen und gehört einem Klassifikationssystemtypen an.

## ClassificationSystemType - Klassifikationssystemtyp

Ein Klassifikationssystemtyp gibt vor, welchen Klassifikationsaspekt dieses Klassifikationssystem bedingt und welche Elemente in dem BIM-Modell damit klassifiziert werden können. Es klassifiziert Klassifikationssysteme.

In einem Projekt können nicht 2 verschiedene Klassifikationssystemtypen verwendet werden. Der Anwender ist verpflichtet, in einem Projekt nur ein Klassifikationssystemtyp zu verwenden.

Klassifikationssystemtypen in BIMeta: | Beispiele:
------------------------------------- | ----------
Kostengruppen (CostTypes) | DIN276
Anwendungsfälle (UseCaseTypes) | 
Bauteiltypen (ObjectTypes) | ISO 16757, uniclass, IFC, VDI 3805
Materialtypen (MaterialTypes) |
Flächentypen (BuildingTypes) | GEFMA 924-10
Raumnutzungsarten (SpaceTypes) | Din 277, ISO 81346
Dokumententypen (DocumentTypes) | 
Lebenszyklusphasen (LifeCyclePhases) | 
Produkttypen (ProductType) ??? | 

Klassifikationssysteme dürfen nur aufeinander gemappt werden, wenn diese demselben Klassifikationssystemtypen angehören.

## Class - Klasse

Klassen sind eine offene Sammelkategorie, die unterschiedliche Elemente zusammenfasst, die sich hinsichtlich des Klassifikationsaspektes gleichen (VDI 2552-9).
Sie sind Bestandteile von Klassifikationssystemen und standardisiert gemäß ISO 12006-2 und VDI 2552-9. Diese Dokumente bilden die Grundlagen bei dem Strukturieren der Klassen.
Klasse haben Properties (Merkmale).

## Merkmale -	Properties
In BIMeta werden in der Merkmalstabelle nicht die Daten, sondern die Metadaten ([Unterschied zwischen Daten und Metadaten]()) verwaltet. Diese Tabelle ist nach der DIN EN ISO 23386 strukturiert und ermöglicht dadurch den Austausch und die Kommunikation mit anderen Systemen.
In der Merkmalstabelle werden die Merkmale der Merkmale verwaltet, die in den jeweiligen Klassifikationssystemen benutzt werden sollen. 
Merkmale werden versioniert. Die Versionen der Merkmale werden nach dem Prinzip der Semantischen Versionierung nummeriert.

Pro Merkmal kann ein deutscher und ein englischer Definitionstext eingetragen werden, wobei die Heimatsprache hinterlegt wird.

## Weiterführende Erklärungen

### Unterschied von Daten und Metadaten

### Unterschied von Maßen und Einheiten

### Semantische Versionierung

BIMeta versioniert nach der[Semantische Versionierung](https://semver.org/).
**Version 1.2.3 (Major, Minor, Patch)**

**Major**: Inkompatible Changes, Veränderung der Bedeutung, welche sich auch auf die Benutzung auswirken
   - Bei jedem Major-Change muss das Merkmal ersetzt werden, weil das alte Merkmal in der alten Version unverändert benutzt werden können muss.
   - Nachfolgendes Merkmal

**Minor**: Anpassung der Bedeutung, welche die Benutzung aber in keiner Weise einschränkt.
   - Der Datenaustausch ist nicht beeinträchtigt

**Patch**: Beseitigung eines Tippfehlers, einer (Sprachlichen) Korrektur in der Definition oder in den Beispielen oder das Hinzufügen eins neuen Beispiels
   - Bedeutung ändert sich in keiner Weise
   - Kein Grund das Merkmal abzukündigen, Verbesserung im laufenden Betrieb

