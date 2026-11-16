# Huize Zuinig

Een gratis milieuspel in pixel art, in je browser. Loop een week lang door je huis, scheid afval, bespaar energie en water en verdien een energielabel van A tot G.

Geïnspireerd op het schoolspel *Thuis in het Milieu* (Malmberg, 1990), maar volledig nieuw gemaakt. Dit project is onafhankelijk en niet gelieerd aan Malmberg, Redline Software Design of de makers van het originele spel.

Gemaakt door Harold, met hulp van Claude (Anthropic).

**Speel het:** https://haaarold.github.io/Huize-Zuinig/

## Over het spel

- 7 dagen, 21 klussen, 7 kamers (woonkamer, keuken, slaapkamer, badkamer, zolder, tuin en oprit)
- Kies per klus uit drie opties en lees waarom een keuze zuiniger is
- Blaadjes, een comfortmeter en een eindrapport met energielabel
- Geen account, geen cookies, geen statistieken, geen advertenties
- Werkt op computer, tablet, telefoon en digibord

De adviezen kloppen in grote lijnen. De getallen voor energie, water en afval zijn ruwe schattingen om keuzes te vergelijken en geen meetgegevens.

## Techniek

Gewoon HTML, CSS en JavaScript, zonder build-stap en zonder frameworks.

```
index.html      homepage met uitleg en SEO
spel/index.html het spel zelf (canvas, pixel art in code getekend)
img/            voorbeeldplaatjes, favicon en social image
sitemap.xml     voor zoekmachines
robots.txt
```

De pixel art wordt in `spel/index.html` met code getekend op een canvas van 160 x 112 pixels. De kamers zijn per pixel in perspectief berekend en worden geschaald met `image-rendering: pixelated`.

### Lokaal draaien

```
git clone https://github.com/haaarold/Huize-Zuinig.git
cd Huize-Zuinig
python3 -m http.server 8000
```

Open daarna http://localhost:8000.

### Publiceren met GitHub Pages

1. Zet de bestanden in een repository met de naam `Huize-Zuinig`.
2. Ga naar **Settings > Pages**, kies **Deploy from a branch** en dan `main` en `/ (root)`.
3. Na een minuut staat de site op `https://<gebruikersnaam>.github.io/Huize-Zuinig/`.

Gebruik je een andere naam of een eigen domein? Pas dan de URL aan in `index.html`, `spel/index.html`, `sitemap.xml` en `robots.txt` (zoek op `haaarold.github.io`).

## Meewerken

Ideeën voor nieuwe klussen, betere uitleg of vertalingen zijn welkom via een issue of pull request. Nieuwe klussen staan in de lijst `TAKEN` in `spel/index.html`. Elke klus heeft een kamer, een plek in de kamer, drie opties en een uitleg.

## Licentie

De code en teksten staan onder de [MIT-licentie](LICENSE). Je mag ze vrij gebruiken, aanpassen en delen.

De lettertypes Pixelify Sans en Figtree komen van Google Fonts en hebben een eigen open licentie (SIL Open Font License).
