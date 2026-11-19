# Black Chilli – koncept nového e-shopu

Statický frontend (HTML + CSS + vanilla JS, bez buildu) pro blackchilli.cz. Stejný designový jazyk jako koncepty Montana Cans, Autolaky, Grafficon a další (tmavý rám, zaoblené plochy, plovoucí pill menu, obří „ghost“ nápisy, pozadí se přebarvuje podle barvy kůže vybraného produktu).

**Jde o neoficiální návrh** – stránka má trvalý pruh „KONCEPT“, vodoznak a `noindex`.

## Co umí
- **Kompletní katalog** – 52 produktů (peněženky, opasky, doplňky, cestování, řemínky Apple Watch, dřevěná pera), 25 s výběrem barvy kůže.
- Carousel kombinuje výřezy peněženek a fotokarty per.

## Spuštění lokálně
```bash
cd blackchilli && python3 -m http.server 8000   # http://localhost:8000
```

## Nasazení
Settings → Pages → Source: **GitHub Actions**, pak Actions → Run workflow. Kořenový `index.html` přesměruje do `blackchilli/`.

## Struktura
- `index.html`, `css/style.css`, `js/app.js` – sdílená šablona; `js/shop.js` – vše specifické pro obchod
- `data/catalog.json` – katalog; `assets/img/p/` – fotky (WebP), `assets/img/hero/` – výřezy pro carousel

## Co ještě chybí do ostrého provozu
- Platby, sklad a objednávky v reálném čase – ceny jsou snímek z 19. 11. 2026, objednávka zatím odchází e-mailem (mailto).
- Konfigurátory (kůže × nitě × přezka) jsou v náhledu zjednodušené na výběr barvy kůže.
