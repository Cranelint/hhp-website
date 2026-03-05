# Migration Inventar – HHP Süd Altseite

## Quelldomain
- https://xn--hhp-sd-7ya.de/ (IDN: https://hhp-süd.de/)
- Technisch identisch: https://hhp-sued.de/ (SSL-Zertifikat abgelaufen)

## Seiten der Altseite

### Hauptseiten
| Alt-URL | Status | Ziel |
|---------|--------|------|
| / | Startseite | / |
| /uber-uns/ | Über uns | /unternehmen/ueber-uns/ |
| /ansprechpartner/ | Ansprechpartner | /unternehmen/ansprechpartner/ |
| /qualifikationen/ | Qualifikationen | /unternehmen/qualifikationen/ |
| /geschaftsleitung/ | Geschäftsleitung | /unternehmen/geschaeftsleitung/ |
| /brandschutzplanung/ | Brandschutzplanung | /leistungen/brandschutzplanung/ |
| /brandschutzprufung/ | Brandschutzprüfung | /leistungen/brandschutzpruefung/ |
| /karriere/ | Karriere | /karriere/ |
| /downloads/ | Downloads | /downloads/ |
| /kontakt/ | Kontakt | /kontakt/ |
| /impressum/ | Impressum | /impressum/ |
| /datenschutz/ | Datenschutz | /datenschutz/ |
| /angebotsanfrage/ | Angebotsanfrage | /kontakt/ (301) |

### Referenz-Kategorien (10 Stück)
| Alt-URL | Kategorie | Anzahl Projekte |
|---------|-----------|----------------|
| /portfolio_category/verwaltung | Büro / Verwaltung | 9 |
| /portfolio_category/denkmalschutz | Denkmalschutz | 5 (+2 Kreuz) |
| /portfolio_category/wissenschaft | Wissenschaft / Forschung | 5 (+1 Kreuz) |
| /portfolio_category/hotels | Hotels / Tagungszentren | 6 (+2 Kreuz) |
| /portfolio_category/industriebauten | Industriebauten | 5 |
| /portfolio_category/krankenhauser | Krankenhäuser / Pflegeheime | 4 (+1 Kreuz) |
| /portfolio_category/stadien | Stadien / Versammlungsstätten | 6 (+1 Kreuz) |
| /portfolio_category/verkaufsstatten | Verkaufsstätten | 4 (+1 Kreuz) |
| /portfolio_category/wohngebaude | Wohn- und Geschäftsgebäude | 4 (+1 Kreuz) |
| /portfolio_category/schulen | Schulen / Kindertagesstätten | 5 |

### Portfolio-Einträge (53 einzigartige Projekte)
Alle Projekte wurden als Markdown-Dateien unter content/referenzen/ migriert.

## Assets

### PDFs (3 Dateien)
| Datei | Quelle | Ziel |
|-------|--------|------|
| HHPS_Kalender_Original_2024.pdf | /wp-content/uploads/2024/01/... | /downloads/ |
| HHPS_Kalender_Farbe_2024.pdf | /wp-content/uploads/2024/01/... | /downloads/ |
| Stellenausschreibung-Projektingenieur-2020.pdf | /wp-content/uploads/2021/01/... | /downloads/karriere/ |

### Bilder
- Logo: 1 Datei (logo-2.png -> logo.png)
- Portfolio-Bilder: 53 Projektbilder (je 1 Hauptbild pro Projekt)
- Gesamt: 54 Bilddateien

## Entfallene Funktionen
- Kontaktformular (ersetzt durch E-Mail/Telefon-Kontaktdaten)
- Angebotsanfrage-Formular (301 Redirect auf /kontakt/)
- WordPress-Backend
- Externe Abhängigkeiten (Google Fonts, etc.)
