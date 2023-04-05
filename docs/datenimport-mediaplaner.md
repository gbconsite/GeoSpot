---
description: Die verschiedenen Möglichkeiten des Datenimports beim Mediaplaner
---

## Datenimport

Es gibt drei Möglichkeiten des Datenimports:

1.	Import eigener Sachdaten (z.B. Abonnenten-Zahlen) mit Referenz zu den Grundlage-Gebieten (in diesem Beispiel Touren), siehe dazu auch Kapitel 2.1
2.	Import von Belegungen
3.	Import von Filialstandorten als eigene Karten-Layer

### Import eigener Sachdaten

Diese Funktion ist den Mitarbeitern der gb consite vorbehalten und wird als Dienstleistung durchgeführt. Es können alle numerischen Daten, die auf eine der verfügbaren Grundlagen refe-renzieren (z.B. Touren, Belegungseinheiten, Verteilbezirke, Ausgaben, etc.) hochgeladen werden.
Diese Daten sind anschließend für alle Analysearten verfügbar.

### Import von Belegungen

Über *Administration -> Upload* können Sie bestehende Belegungen selbst hochladen, um diese beispielsweise anschließend zahlenmäßig auszuwerten oder einfach anzupassen.

![grafik](https://user-images.githubusercontent.com/99329016/230027882-c3c65518-87a1-4e31-b0a4-31b3b75e35ab.png)

Wählen Sie entweder eine bestehende Planung aus oder legen Sie vorher eine neue Planung an und wählen diese dann aus (siehe hierzu auch Kapitel 2.2).
Anschließend wählen Sie eine hochzuladende Excel-Datei über Datei auswählen und klicken dann *Upload analysieren*:

![grafik](https://user-images.githubusercontent.com/99329016/230027997-17d4762a-a033-4072-be97-53337f489b02.png)

Nun müssen Sie die Felder zuordnen. Wählen Sie für die Ebene Ihrer Grundlagen-Gebiete *Gebiet Nr.* und für die Bezeichnung Ihrer Belegung *Bezirk Nr* und klicken unten rechts auf Upload. Diese Belegung können Sie dann analysieren und bearbeiten, wie in den vorangegangenen Kapi-teln beschrieben.


### Import von eigenen Karten-Layern

Über das Symbol :material-folder-open: oben links in der Karte gelangen Sie zu einer Dateiauswahl, mit der Sie z.B. Filialstandorte eines Kunden als zusätzliche Punkt-Layer einbinden können. Dies können Sie temporär für sich oder auch dauerhaft für alle anderen Nutzer Ihres Unternehmens tun.
Es werden die Geodatenformate geojson und kml unterstützt. Diese Formate können Sie z.B. mit dem kostenlosen Programm „Google Earth Professional“ erzeugen, indem Sie dort Adresslisten kochladen, diese geokodieren und anschließend als kml-Datei abspeichern.

![grafik](https://user-images.githubusercontent.com/99329016/230028371-c7c9469b-7d5f-45f6-a9ce-f9719e5605f1.png)
![grafik](https://user-images.githubusercontent.com/99329016/230028389-45fe3520-10d7-4a3e-a2c1-ad2eba76f70a.png)


Nach dem Hochladen (in diesem Beispiel einer kml-Datei) sehen Sie die Standorte auf der Karte und klicken einen beliebigen davon an.
Es öffnet sich ein Menü, mit dem Sie die Symbole und die Farben der Icons verändern und den Layer entweder wieder löschen (Klick auf Mülltonne) oder speichern können.

Nach der Bearbeitung und dem Klick auf Layer Speichern ist dieser Layer für Sie und andere Nutzer auch in der Layersteuerung (siehe Kapitel 1.2) auswählbar.
Über das Menü *Administration -> Eigene Layer* können Sie diesen und weitere selbst hoch geladene Layer dann auch in Zukunft verwalten:

 ![grafik](https://user-images.githubusercontent.com/99329016/230028520-52213041-6ed2-4876-b8d6-68f21706809c.png)

