# QA-Report – HHP Süd Website Migration

## Zusammenfassung

| Metrik | Wert |
|--------|------|
| Seiten Altseite (Hauptseiten) | 13 |
| Seiten Altseite (Portfolio) | 53 |
| Seiten Altseite (Kategorien) | 10 |
| **Seiten Altseite Gesamt** | **76** |
| Seiten Neuseite (Hugo) | 89 |
| davon Referenzen | 63 (+1 Index) |
| davon Kategorien | 10 (+1 Index) |
| davon Unternehmen | 4 (+1 Index) |
| davon Leistungen | 2 (+1 Index) |
| davon Sonstige (Kontakt, Karriere, Downloads, Impressum, Datenschutz, Startseite) | 6 |
| PDFs migriert | 3/3 |
| Bilder migriert | 54 (Logo + 53 Projekte) |
| Redirects definiert | ~70 Regeln |

## Inhalts-Migration

### Vollständig migriert
- [x] Startseite (Projekt-Grid, Leistungen, Download-Hinweis)
- [x] Über uns (Firmengeschichte, Beschreibung)
- [x] Ansprechpartner (alle 5 Personen)
- [x] Qualifikationen (alle 8 Qualifikationen)
- [x] Geschäftsleitung (Dammköhler + Budwill)
- [x] Brandschutzplanung (alle 5 Leistungsphasen)
- [x] Brandschutzprüfung (inkl. Standort Saarbrücken)
- [x] Alle 53 Referenzprojekte mit Frontmatter
- [x] Alle 10 Referenz-Kategorien als Taxonomie
- [x] Downloads (2 Kalender-PDFs)
- [x] Karriere (Stellenausschreibung + PDF)
- [x] Kontakt (ohne Formular, nur Kontaktdaten)
- [x] Impressum (vollständig)
- [x] Datenschutz (vollständig, Cookies-Abschnitt angepasst: „keine Cookies")

### Entfernte Funktionen
- Kontaktformular → Ersetzt durch E-Mail/Telefon
- Angebotsanfrage → 301 auf /kontakt/
- WordPress-Backend → Entfallen
- Externe Abhängigkeiten → Entfallen

## Assets

### PDFs
| Datei | Größe | Status |
|-------|-------|--------|
| HHPS_Kalender_Original_2024.pdf | 287 KB | OK |
| HHPS_Kalender_Farbe_2024.pdf | 615 KB | OK |
| Stellenausschreibung-Projektingenieur-2020.pdf | 213 KB | OK |

### Bilder
- 53 Projektbilder heruntergeladen
- 53 davon > 1 KB (gültige Bilder)
- Logo (logo.png) heruntergeladen und referenziert

## Redirects

- Alle alten WordPress-URLs haben 301-Redirects auf neue Hugo-URLs
- Portfolio-Einzelseiten: 53 Redirects
- Portfolio-Kategorien: 10 Redirects
- Hauptseiten: ~10 Redirects
- Download-Pfade: 3 Redirects
- Entfallene Seiten: 1 Redirect (Angebotsanfrage → Kontakt)

## Security Headers

Konfiguriert in `_headers`:
- [x] Content-Security-Policy (script-src 'none', keine externen Ressourcen)
- [x] Strict-Transport-Security
- [x] X-Content-Type-Options: nosniff
- [x] Referrer-Policy: strict-origin-when-cross-origin
- [x] Permissions-Policy (alle Features deaktiviert)
- [x] X-Frame-Options: DENY

## DSGVO-Konformität

- [x] Keine Cookies
- [x] Keine externen Requests (keine Google Fonts, kein CDN, kein Tracking)
- [x] Keine Formulare
- [x] Keine Third-Party-Embeds
- [x] Kein JavaScript
- [x] Datenschutzerklärung aktualisiert (Cookies-Abschnitt: „keine Cookies")

## Bekannte Einschränkungen / Annahmen

1. **Bilder**: Nur je 1 Hauptbild pro Referenzprojekt migriert. Die Altseite hatte teilweise mehrere Bilder pro Projekt (z.B. Stadthalle Braunschweig: 7 Bilder). Bei Bedarf können weitere Bilder nachträglich ergänzt werden.

2. **Detailinfos Referenzen**: Für ca. 40 der 53 Projekte liegen nur Titel, Standort und Kategorie vor. Detailinfos (Auftraggeber, Architekt, Bauzeit, Leistungen) wurden nur für die Featured-Projekte (12 Stück) vollständig migriert, da diese Informationen auf den Kategorieübersichtsseiten der Altseite nicht verfügbar waren.

3. **Stellenausschreibung**: Die Stellenausschreibung stammt aus 2020 und ist möglicherweise nicht mehr aktuell. Die Datei wurde dennoch migriert.

4. **Datenschutz Cookies-Abschnitt**: Der Original-Text erwähnte Cookies. Da die neue Seite keine Cookies verwendet, wurde der Abschnitt angepasst zu „Diese Website verwendet keine Cookies."

5. **Kontaktformular**: Durch E-Mail/Telefon-Kontaktdaten ersetzt. Hinweis auf der Seite ergänzt.

## Build-Verifizierung

- Hugo Build: Erfolgreich (90 Seiten, 69 statische Dateien)
- Keine Build-Warnungen oder -Fehler
- _headers und _redirects im Build-Output vorhanden
