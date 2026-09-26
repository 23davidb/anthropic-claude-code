# Rechnungstool

Einfaches Rechnungsprogramm, das komplett im Browser läuft. Es braucht keine Installation, keinen Server und keine Internetverbindung.

## Starten

`index.html` im Browser öffnen (Doppelklick). Der Ordner `vendor/` muss daneben liegen.

## Funktionen

- **Einstellungen**: eigene Firmendaten, Logo, Bankverbindung, UID, USt-Satz, Zahlungsziel, Nummernkreis, Kleinunternehmerregelung
- **Kunden**: Rechnungsadressen einmal speichern und bei jeder Rechnung auswählen
- **Rechnung**: Kunde wählen, Positionen erfassen, Live-Vorschau im A4-Format, **PDF erstellen** lädt das PDF direkt herunter
- **Rechnungen**: Archiv aller erstellten Rechnungen: erneut öffnen, als Vorlage für eine neue Rechnung verwenden oder löschen
- Rechnungsnummern werden automatisch fortlaufend vergeben (`RE-2026-001`, `RE-2026-002`, …)
- Platzhalter in Texten: `{faellig}`, `{tage}`, `{nummer}`

## Daten & Backup

Alle Daten liegen im `localStorage` des Browsers, also nur auf diesem Computer und in diesem Browser.
Unter *Einstellungen → Datensicherung* kannst du ein Backup als JSON-Datei herunterladen und wieder einspielen, zum Beispiel für einen anderen Computer.

## Rechnungslayout anpassen

Das Aussehen der Rechnung ist in `index.html` festgelegt: in der Funktion `invoiceHtml()` und in den CSS-Regeln unter `.invoice`.

PDF-Erzeugung: [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) 0.10.1 (MIT), liegt in `vendor/`.
