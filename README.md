# Rechnungstool – Tischlerei Bitschnau

Einfaches Rechnungsprogramm, das komplett im Browser läuft. Es braucht keine Installation, keinen Server und keine Internetverbindung.

## Starten

`index.html` im Browser öffnen (Doppelklick). Die Ordner `vendor/` und `assets/` müssen daneben liegen. Am einfachsten lädst du das ganze Repository als ZIP herunter und entpackst es.

## Funktionen

- **Einstellungen**: eigene Firmendaten, Logo, Bankverbindung, UID, USt-Satz, Zahlungsziel, Nummernkreis, Kleinunternehmerregelung
- **Kunden**: Rechnungsadressen einmal speichern und bei jeder Rechnung auswählen
- **Rechnung**: Kunde wählen, Positionen erfassen, Live-Vorschau im A4-Format, **PDF erstellen** lädt das PDF direkt herunter
- **Rechnungen**: Archiv aller erstellten Rechnungen: erneut öffnen, als Vorlage für eine neue Rechnung verwenden oder löschen
- Rechnungsart (Rechnung, Teilrechnung I, Schlussrechnung …) und Betreff, z. B. „Teilrechnung I: Möbeltischlerarbeiten“
- Rechnungsnummern werden automatisch fortlaufend vergeben (Jahr + laufende Nummer, z. B. `202636`)
- Positionsnummer frei wählbar (leer = automatisch). Pauschalbeträge wie Anzahlungen: Menge 1 und Einheit leer, dann werden Menge und E. Preis nicht gedruckt
- Platzhalter in Texten: `{faellig}`, `{tage}`, `{nummer}`

## Erste Einrichtung

Firmendaten, Logo und Bank sind vorausgefüllt. Unter *Einstellungen* einmal **IBAN und BIC** eintragen, weil die nicht im öffentlichen Repository stehen sollen. Außerdem die **nächste laufende Rechnungsnummer** setzen.

## Daten & Backup

Alle Daten liegen im `localStorage` des Browsers, also nur auf diesem Computer und in diesem Browser.
Unter *Einstellungen → Datensicherung* kannst du ein Backup als JSON-Datei herunterladen und wieder einspielen, zum Beispiel für einen anderen Computer.

## Rechnungslayout anpassen

Das Layout folgt der bisherigen Bitschnau-Rechnung. Festgelegt ist es in `index.html`: in der Funktion `invoiceHtml()` und in den CSS-Regeln unter `.invoice`. Das Logo liegt in `assets/logo.png` und ist zusätzlich in `assets/logo.js` eingebettet. Ein anderes Logo lässt sich in den Einstellungen hochladen.

Schrift: Cambria (unter Windows vorinstalliert), sonst Caladea von Google Fonts bzw. Georgia.

PDF-Erzeugung: [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) 0.10.1 (MIT), liegt in `vendor/`.
