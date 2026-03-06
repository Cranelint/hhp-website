# HHP Süd – Website

Statische Website der HHP Süd Sachverständige für Brandschutz GmbH, gebaut mit [Jekyll](https://jekyllrb.com/) und gehostet auf [GitHub Pages](https://pages.github.com/).

## Voraussetzungen

- [Ruby](https://www.ruby-lang.org/) 3.0 oder neuer
- [Bundler](https://bundler.io/)

## Lokale Entwicklung

```bash
# Abhängigkeiten installieren
bundle install

# Entwicklungsserver starten
bundle exec jekyll serve

# Seite unter http://localhost:4000/hhp-website/ aufrufen
```

## Build

```bash
# Produktions-Build
bundle exec jekyll build

# Output-Verzeichnis: _site/
```

## GitHub Pages Deployment

Die Seite wird automatisch über GitHub Pages deployt. Bei jedem Push auf `main` baut GitHub Pages die Seite neu.

**Einstellungen:**
- Repository Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`

## Projektstruktur

```
.
├── _config.yml          # Jekyll-Konfiguration
├── _layouts/            # HTML-Layouts
├── _includes/           # Wiederverwendbare Komponenten (Header, Footer, Icons)
├── _referenzen/         # Referenzprojekte (Jekyll Collection)
├── _karriere/           # Stellenangebote (Jekyll Collection)
├── css/                 # Stylesheets
├── images/              # Bilder
│   └── referenzen/      # Projektbilder
├── downloads/           # PDF-Downloads
├── unternehmen/         # Unternehmensseiten
├── leistungen/          # Leistungsseiten
├── kontakt/             # Kontaktseite
├── karriere/            # Karriereseite
├── kategorie/           # Referenz-Kategorieseiten
├── impressum/           # Impressum
├── datenschutz/         # Datenschutzerklärung
├── Gemfile              # Ruby-Abhängigkeiten
└── MIGRATION.md         # Hinweise für den Umzug POC → Live
```

## Besonderheiten

- **Zero JavaScript**: Die Seite funktioniert komplett ohne JavaScript
- **Keine Cookies**: Keine Cookies, kein Tracking, keine externen Requests
- **DSGVO-konform**: Keine Third-Party-Embeds, keine externen Fonts
- **Mobile Navigation**: Realisiert mit `<details>`/`<summary>` (kein JS)
- **Redirects**: Alte WordPress-URLs werden über `jekyll-redirect-from` Plugin umgeleitet
