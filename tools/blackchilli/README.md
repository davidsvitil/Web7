# Aktualizace dat

```bash
python3 tools/blackchilli/fetch_pages.py urls.txt raw/pages                     # šetrné stažení (4 paralelně, cache)
python3 tools/blackchilli/parse_shop.py shoptet raw/pages raw/parsed.json           # parsování
python3 tools/blackchilli/build_catalog.py raw/parsed-col.json blackchilli tools/blackchilli/config.json   # katalog + WebP
python3 tools/blackchilli/make_hero.py blackchilli <id produktu> ...                    # výřezy pro carousel
```
Potřeba: Python 3, Pillow, BeautifulSoup4, lxml, curl.
Před krokem 3: `resolve_colors.py raw/parsed.json raw/parsed-col.json` (vzorky barev kůže, sloučení konfigurátorů), po kroku 3: `name_colors.py blackchilli/data/catalog.json` (barva stránky podle názvu).
