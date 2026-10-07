---
layout: default
title: Aurora Expert – Datenschutzerklärung
description: Datenschutzerklärung der iOS-App Aurora Expert.
lang: de
---

# Aurora Expert – Datenschutzerklärung

<p class="muted"><a href="./privacy.html" hreflang="en">English version</a></p>

<p class="muted">Stand: 7. Oktober 2026</p>

Aurora Expert („die App“) sagt Polarlichter vorher. Sie ist von Grund auf **datensparsam** gebaut: Es gibt kein Konto,
keine Analyse, keine Werbung und kein Tracking. Hier steht, welche Daten die App nutzt, wohin sie gehen und warum.

## Verantwortlicher

Der Entwickler von Aurora Expert.

E-Mail: [markey2000@googlemail.com](mailto:markey2000@googlemail.com)

## Kurzfassung

- **Wir erheben keine personenbezogenen Daten für eigene Zwecke.** Die App hat kein Konto und kein Analyse-SDK. Wir
  (der Entwickler) erhalten weder deinen Standort noch deine Suchbegriffe oder deine Käufe, und wir zeichnen nicht auf,
  wie du die App nutzt. Abgesehen vom Abruf zweier öffentlicher Datendateien, die wir bei Google Firebase Storage
  bereitstellen (die weltweite Wolkenebene und die Statusdatei der Alarme – reine Downloads, die nichts über dich
  enthalten außer dem, was jede Netzwerkanfrage zeigt, etwa deine IP-Adresse), ist die einzige Anfrage, die unseren
  eigenen Server erreicht, ein Test-Alarm, den du selbst sendest (siehe unten).
- **Wir verfolgen dich nicht** über Apps oder Websites hinweg und geben keine Daten an Datenhändler weiter.
- Daten verlassen dein Gerät nur, um eine Funktion zu erfüllen, die du nutzt:
  - **Apple WeatherKit** – Koordinaten, um die Bewölkung abzurufen;
  - **Apple-Kartendienste (MapKit bzw. Core Location)** – Koordinaten und Suchtext, um einen eingetippten Ort zu
    finden, Orte zu benennen und ihre Zeitzone zu bestimmen und um Fahrzeiten zu berechnen;
  - **Google Firebase** – eine Installationskennung und ein Push-Token für Mitteilungen, die groben Regionsthemen
    deiner Alarm-Orte und, wenn du einen Test-Alarm sendest, ein zufälliges Test-Thema mit einer App-Check-Bestätigung;
  - **Apple** – Käufe und der Bewertungsdialog des App Store.

## Welche Daten die App nutzt

### Standort
- **Vorhersage auf dem Gerät.** Dein genauer Standort wird auf deinem Gerät genutzt, um zu berechnen, ob das
  Polarlicht bei dir sichtbar ist (Sonne und Dunkelheit, deine geomagnetische Breite, Lichtverschmutzung).
- **Bewölkung (Apple WeatherKit).** Für die Bewölkung werden die Koordinaten deines Standorts – und der Orte, die du
  ansiehst oder speicherst – an Apples Dienst WeatherKit gesendet. Die Trip-Planung und „Heute Nacht ab hier“ senden
  zusätzlich die Koordinaten einiger möglicher Aussichtspunkte rund um deine Unterkunft oder deinen aktuellen Standort
  (bei „Heute Nacht ab hier“ höchstens acht je Prüfung und nur, wenn du auf „Prüfen“ tippst). Für diese Anfragen gilt
  die Datenschutzerklärung von Apple.
- **„Heute Nacht ab hier“.** Hast du den Standortzugriff erlaubt, startet die App von einer Standortbestimmung deines
  Geräts, die höchstens 30 Minuten alt ist, sonst von deinem Heimatort. Diese Funktion fragt nie selbst nach dem
  Standortzugriff.
- **Optionale Polarlicht-Alarme.** Schaltest du Alarme ein, wird der Standort deines Heimatorts – und mit Aurora Pro
  der jedes gespeicherten Orts, für den Alarme an sind – **auf deinem Gerät** in eine grobe Region umgerechnet (etwa ein
  Band von 5° Breite × 15° Länge). Nur dieser Regionscode und die gewählte Alarm-Schwelle werden genutzt, um
  Mitteilungsthemen zu abonnieren. **Deine genauen Koordinaten werden nie auf unsere Server hochgeladen.**
- **Kompass (Feld-Modus „Ich bin draußen“).** Die Kompassrichtung und, bei bereits erteiltem Standortzugriff, grobe
  Standortbestimmungen werden nur auf deinem Gerät genutzt, um den Pfeil auszurichten; sie werden nirgendwohin
  gesendet.
- Der Standortzugriff nutzt die Erlaubnis „Beim Verwenden der App“ und lässt sich jederzeit in den iOS-Einstellungen
  widerrufen.

### Ortssuche, Ortsnamen, Zeitzonen und Routen (Apple-Kartendienste)
- **Ortssuche.** Suchst du einen Ort – deinen Heimatort, einen gespeicherten Ort oder den Ort, den du ansehen willst,
  und im Trip-Setup eine Basis oder Unterkunft –, geht der eingetippte Text an Apples Ortssuche (`MKLocalSearch`, im
  Trip-Setup zusätzlich `MKLocalSearchCompleter` für Vorschläge); auch der gewählte Ort wird dort aufgelöst.
- **Namen und Zeitzonen.** Die App sendet Koordinaten an Apples Dienst zur Umkehr-Geokodierung (Core Location bzw.
  MapKit), um daraus einen Ortsnamen und die Zeitzone des Orts zu machen:
  - wenn du deinen aktuellen Standort als Ort wählst (die Koordinaten deines Geräts);
  - einmal nach einem Update für einen Ort, den du in einer früheren Version gewählt hast und zu dem noch keine Zeitzone
    gespeichert ist;
  - für empfohlene Ziele (Trip-Planung, „Heute Nacht ab hier“) und bei „Heute Nacht ab hier“ für deinen Gerätestandort,
    wenn er keiner deiner eigenen Orte ist.
  Die Namen der Ziele werden auf deinem Gerät zwischengespeichert, derselbe Punkt wird also nicht erneut abgefragt.
- **Fahrzeiten.** Die Trip-Planung und „Heute Nacht ab hier“ fragen Apples Routendienst (MapKit) nach den Fahrzeiten
  zwischen deiner Basis und möglichen Zielen.
- **„Route starten“** öffnet Apple Karten mit dem gewählten Ziel; ab dort gilt die Datenschutzerklärung von Apple Karten.
- Diese Anfragen gehen direkt von deinem Gerät an Apple. Für sie gilt die Datenschutzerklärung von Apple. Wir erhalten
  davon nichts.

### Firebase und das Push-Token
- Beim Start richtet die App Google Firebase ein (Cloud Messaging, App Check und Cloud Functions, kein Analytics).
  Firebase legt dabei eine **Installationskennung** für diese Kopie der App an.
- Sobald du Mitteilungen erlaubt hast – für Polarlicht-Alarme oder für Trip-Erinnerungen –, meldet sich die App bei
  jedem Start bei Apples Push-Dienst an und gibt das Ergebnis an Firebase Cloud Messaging weiter, das ein
  **Push-Token** ausstellt. Das kann auch geschehen, wenn kein Alarm eingeschaltet ist.
- Polarlicht-Alarme gehen an Themen. Die App abonniert nur die oben beschriebenen Regionsthemen (eine grobe Region und
  eine Schwelle, nie Koordinaten). Das Token kennzeichnet die App-Installation, nicht dich. Wir speichern es nicht auf
  eigenen Servern und verknüpfen es nicht mit deiner Person.

### Test-Alarm und Firebase App Check
- Sendest du im Alarme-Tab einen **Test-Alarm**, weist die App unserem Server über **Firebase App Check** (mit Apples
  App Attest bzw. DeviceCheck) nach, dass die Anfrage von einer echten Kopie der App kommt. Das geschieht nur beim
  Senden eines Test-Alarms, nicht beim Start.
- Die Anfrage geht an unseren Server (eine Firebase Cloud Function, betrieben von Google Cloud) und enthält nur das
  zufällige, einmal genutzte Test-Thema und das App-Check-Token. Wie jede Netzwerkanfrage zeigt sie dem Server deine
  IP-Adresse; die üblichen Anfrage-Protokolle von Google Cloud für unser Projekt können sie festhalten. Gegen Missbrauch
  speichert unser Server etwa einen Tag lang einen Einweg-Hash dieses zufälligen Themas und den Zeitpunkt der Anfrage;
  darin steht nichts, was dich oder dein Gerät erkennbar macht.

### Mitteilungen, die auf deinem Gerät entstehen
- Aufbruch-Erinnerungen für Trips, ihre Absagen und die morgendliche Frage nach einer Sichtung sind **lokale
  Mitteilungen**, die die App auf deinem Gerät plant. Kein Server ist beteiligt.

### Fotos im Journal, Export und Bilder sichern
- **Fotos hinzufügen** (Aurora Pro, „Meine Nächte“): Du wählst Fotos in der Fotoauswahl von iOS. iOS gibt der App nur
  die Fotos, die du auswählst; die App bekommt keinen Zugriff auf deine Mediathek und fragt dafür nach keiner Erlaubnis.
- Die App legt von jedem gewählten Foto **eine eigene Kopie** in ihrem Speicher auf deinem Gerät ab: ein JPEG mit
  höchstens 2048 Pixeln an der langen Seite, **ohne Ortsdaten (GPS)** und ohne die Aufnahmedaten der Kamera. Die
  Aufnahmezeit wird einmal gelesen, um das Foto einer Nacht zuzuordnen, und am Journal-Eintrag gespeichert. Das
  Original in deiner Mediathek bleibt unverändert; löschst du die Kopie in der App, bleibt das Original.
- Die Kopien sind wie das übrige Journal Teil deines **Geräte-Backups** (iCloud-Backup oder Computer), wenn du eines
  nutzt. Die App selbst sendet sie nirgendwohin; wir (der Entwickler) erhalten nichts.
- **Export** (CSV oder JSON): Nur wenn du es möchtest, schreibt die App deine Journal-Einträge – ohne Fotos – in eine
  Datei an einem Ort, den du wählst (etwa die Dateien-App). Was danach mit der Datei geschieht, bestimmst du.
- **Karte teilen und „Bild sichern“.** Eine Karte, die du teilst, geht über das Teilen-Menü von iOS an die App, die du
  wählst. Wählst du „Bild sichern“, legt die App die Karte in deiner Mediathek ab; iOS fragt dafür einmal nach der
  Erlaubnis, Fotos *hinzuzufügen* (lesen kann die App deine Mediathek damit nicht).

### Käufe
- Pro-Funktionen („Aurora Pro“) werden mit einem einmaligen In-App-Kauf freigeschaltet, den **Apple** vollständig
  abwickelt. Wir sehen und speichern keine Zahlungsdaten. Der Kauf wird auf deinem Gerät über Apples StoreKit geprüft.
- Für das Abzeichen „Gründer“ liest die App das ursprüngliche Kaufdatum deines Aurora-Pro-Kaufs **auf deinem Gerät**.
  Es wird nirgendwohin gesendet.
- Ob Aurora Pro freigeschaltet ist, steht zusätzlich im gemeinsamen Speicher der App auf deinem Gerät, damit die
  Widgets Pro-Inhalte zeigen können.

### Bitte um eine Bewertung
- Nachdem du im Journal eine Sichtung bestätigt hast, kann die App iOS bitten, Apples Standard-Bewertungsdialog zu
  zeigen. Ob er erscheint und was du dort eingibst, regelt Apple.

### Daten, die nur auf deinem Gerät liegen
Trip-Pläne samt zwischengespeicherter Vorhersagen, Ortsnamen, dein Sichtungs-Journal mit den Kopien seiner Fotos,
die auf diesem Gerät empfangenen Alarme (der Alarm-Verlauf), die letzte bekannte Vorhersage,
Einstellungen, Zähler (etwa, wie viele Prüfungen „Heute Nacht ab hier“ heute Nacht liefen), der Stand eines kostenlosen
Sturm-Cockpit-Schnupperzugangs und Leistungsberichte des Geräts (MetricKit) bleiben auf deinem Gerät.
MetricKit-Berichte erscheinen nur in dem Diagnosetext, den du selbst kopierst; sie werden nie hochgeladen.

### Daten, die wir **nicht** erheben
- Keinen Namen, keine E-Mail, keine Kontakte, kein Konto. Fotos, die du deinem Journal hinzufügst, bleiben in der App
  auf deinem Gerät (siehe „Fotos im Journal“ oben); wir erhalten sie nie.
- Keine Werbe-IDs, keine Nutzungsanalyse, keine Absturzanalyse, die mit dir verknüpft ist.

## Datenquellen Dritter (zur Information)

Aurora Expert zeigt öffentliche Weltraumwetter- und Wetterdaten von: **NOAA Space Weather Prediction Center**, **NASA
(CCMC/DONKI)**, dem **GFZ Helmholtz-Zentrum für Geoforschung** (Hp30-Index, CC BY 4.0), **Aurorasaurus** und **Apple
WeatherKit**. Die weltweite Wolkenebene und die Statusdatei der Alarme lädt die App aus unserem Speicher bei **Google
Firebase Storage**. Beim Abruf dieser Daten gehen übliche Netzwerkanfragen (etwa deine IP-Adresse) an diese Anbieter;
dafür gelten deren Datenschutzerklärungen. Außer bei den oben beschriebenen Anfragen an WeatherKit und die
Apple-Kartendienste hängt an diesen Anfragen kein Standort.

## Speicherdauer

Wir führen keine Nutzerdatenbank. Die Abos der Regionsthemen sind anonym und enthalten keine personenbezogenen Daten.
Die oben beschriebenen Hashes der Test-Alarme verfallen nach etwa einem Tag; die Anfrage-Protokolle von Google Cloud
für unser Projekt bleiben so lange, wie Google Cloud Protokolle aufbewahrt (standardmäßig 30 Tage).
Zwischengespeicherte Vorhersagen und alles unter „Daten, die nur auf deinem Gerät liegen“ bleiben auf deinem Gerät und
werden mit dem Löschen der App entfernt.

## Deine Rechte

Da wir keine personenbezogenen Daten über dich speichern, gibt es bei uns meist nichts, worüber wir Auskunft geben,
was wir berichtigen oder löschen könnten. Du kannst dich trotzdem mit jedem Anliegen nach der DSGVO (Auskunft,
Berichtigung, Löschung, Einschränkung, Widerspruch, Datenübertragbarkeit) an die oben genannte Adresse wenden und hast
das Recht, dich bei einer Datenschutz-Aufsichtsbehörde zu beschweren. Für Daten, die Apple oder Google verarbeiten,
gelten deren Datenschutzerklärungen.

## Kinder

Aurora Expert richtet sich nicht an Kinder und erhebt wissentlich keine Daten von Kindern unter 13 Jahren.

## Änderungen

Wir können diese Erklärung ändern; wesentliche Änderungen erkennst du am Datum „Stand“ oben.

## Kontakt

Fragen zu dieser Erklärung: [markey2000@googlemail.com](mailto:markey2000@googlemail.com)
