# Hinweise zum Umzug von POC zu Live

## DNS-Umschreibung

- Die Domain `hhp-sued.de` (bzw. IDN `hhp-süd.de`) muss per CNAME oder A-Record auf GitHub Pages zeigen
- GitHub Pages Custom Domain konfigurieren: Repository Settings → Pages → Custom domain → `hhp-sued.de`
- HTTPS wird automatisch über Let's Encrypt bereitgestellt
- Nach DNS-Umstellung: `url` in `_config.yml` auf `https://hhp-sued.de` ändern
- Nach DNS-Umstellung: `baseurl` in `_config.yml` auf `""` (leer) ändern

## Aktuell: POC-Modus

- Die Seite läuft unter `https://cranelint.github.io/hhp-website/`
- Alle internen Links verwenden `relative_url` und funktionieren mit dem `baseurl: /hhp-website` Prefix
- Downloads-Links in der Downloads-Seite verwenden absolute Pfade – diese müssen ggf. mit `relative_url` ergänzt werden, wenn sie nicht funktionieren

## Sicherheitsheader

- GitHub Pages unterstützt keine benutzerdefinierten HTTP-Header (kein `_headers` wie bei Cloudflare Pages)
- Content-Security-Policy, HSTS, X-Frame-Options etc. können nur über einen vorgeschalteten Proxy (z.B. Cloudflare) gesetzt werden
- Empfehlung für Live: Cloudflare als DNS/Proxy vor GitHub Pages schalten und dort die Header setzen
- Alternative: Meta-Tags im HTML-Head für CSP (eingeschränkt)

## Weitere Punkte für den Live-Betrieb

- [ ] `_config.yml`: `url` und `baseurl` anpassen
- [ ] Custom Domain in GitHub Pages Repository Settings konfigurieren
- [ ] DNS-Einträge setzen (CNAME `cranelint.github.io` oder A-Records)
- [ ] HTTPS-Zertifikat abwarten (automatisch über GitHub Pages)
- [ ] `CNAME`-Datei im Repository Root erstellen: `hhp-sued.de`
- [ ] Sicherheitsheader über Cloudflare oder ähnlichen Dienst setzen
- [ ] Impressum-URLs prüfen und ggf. aktualisieren
- [ ] Google Search Console: Sitemap einreichen und alte URLs überwachen
- [ ] 301-Redirects von alten WordPress-URLs werden über `jekyll-redirect-from` Plugin gehandhabt
- [ ] Stellenausschreibungen in `_karriere/` bei Bedarf aktualisieren
- [ ] Torsten Budwill: Prokurist-Status prüfen (ggf. Creditreform-Auszug Feb 2026)
