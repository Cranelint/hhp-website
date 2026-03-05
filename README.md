# HHP Süd – Website

Statische Website der HHP Süd Sachverständige für Brandschutz GmbH, gebaut mit [Hugo](https://gohugo.io/).

## Voraussetzungen

- [Hugo Extended](https://gohugo.io/installation/) v0.120.0 oder neuer

## Lokale Entwicklung

```bash
# Entwicklungsserver starten
hugo server

# Seite unter http://localhost:1313 aufrufen
```

## Build

```bash
# Produktions-Build
hugo --minify

# Output-Verzeichnis: public/
```

## Cloudflare Pages Deployment

| Einstellung | Wert |
|-------------|------|
| Build command | `hugo --minify` |
| Build output directory | `public` |
| Hugo version | `0.157.0` (oder neuer) |

Die Hugo-Version kann über die Umgebungsvariable `HUGO_VERSION` gesetzt werden:

```
HUGO_VERSION = "0.157.0"
```

## Projektstruktur

```
.
├── assets/css/          # CSS (wird von Hugo verarbeitet/minifiziert)
├── content/             # Markdown-Inhalte
│   ├── referenzen/      # Referenzprojekte
│   ├── unternehmen/     # Unternehmensseiten
│   ├── leistungen/      # Leistungsseiten
│   ├── kontakt/         # Kontaktseite
│   ├── karriere/        # Karriereseite
│   ├── downloads/       # Downloads-Seite
│   ├── impressum/       # Impressum
│   └── datenschutz/     # Datenschutzerklärung
├── layouts/             # Hugo-Templates
│   ├── _default/        # Standard-Layouts
│   ├── referenzen/      # Referenz-spezifische Layouts
│   ├── partials/        # Wiederverwendbare Komponenten
│   └── taxonomy/        # Kategorie-Layouts
├── static/              # Statische Dateien (1:1 kopiert)
│   ├── images/          # Bilder
│   ├── downloads/       # PDF-Downloads
│   ├── _headers         # Cloudflare Pages Security Headers
│   └── _redirects       # Cloudflare Pages Redirects
├── migration/           # Migrationsdokumentation
│   ├── inventory.md     # Inventar der Altseite
│   ├── url-map.csv      # URL-Mapping alt -> neu
│   └── qa-report.md     # Qualitätssicherungsbericht
└── hugo.toml            # Hugo-Konfiguration
```

## Besonderheiten

- **Zero JavaScript**: Die Seite funktioniert komplett ohne JavaScript
- **Keine Cookies**: Keine Cookies, kein Tracking, keine externen Requests
- **DSGVO-konform**: Keine Third-Party-Embeds, keine externen Fonts
- **Security Headers**: CSP, HSTS, X-Frame-Options etc. via `_headers`
- **Mobile Navigation**: Realisiert mit `<details>`/`<summary>` (kein JS)
