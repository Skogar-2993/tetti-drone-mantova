# Ispezione tetti con drone — Mantova e provincia

Landing page statica. Un file HTML con il CSS dentro, nessuna immagine da caricare,
zero JavaScript, zero font scaricati, zero richieste esterne. Percorsi relativi: funziona
sia online sia aprendo `index.html` con un doppio clic.

Peso della pagina: **4,6 KB** compressa.

## Da sostituire prima di pubblicare

Cerca e sostituisci in `index.html`, `privacy-policy/index.html`,
`cookie-policy/index.html`, `sitemap.xml` e `robots.txt`:

| Cerca | Sostituisci con |
|---|---|
| `390000000000` | il tuo numero per WhatsApp e per i link `tel:` — prefisso `39`, senza `+` e senza spazi |
| `+39 000 000 0000` | lo stesso numero, come vuoi che si legga |
| `nome@esempio.it` | la tua email |
| `https://www.esempio.it` | il dominio, senza `/` finale |
| `[Nome Cognome]` | il tuo nome |
| `[Partita IVA]` | la tua partita IVA |

Poi completa i placeholder fra parentesi quadre nelle due pagine legali (indirizzo,
fornitore di hosting, tempi di conservazione, data).

Non c'è niente di inventato sul tuo conto: né recensioni, né anni di esperienza, né
certificazioni, né prezzi.

## Pubblicazione

Carica tutto tranne `docs/` e questo README:

```
index.html   robots.txt   sitemap.xml   assets/img/   privacy-policy/   cookie-policy/
```

Sull'hosting attiva compressione gzip o brotli, se puoi.

## Se vuoi aggiungere foto

La pagina oggi non ha immagini di proposito. Quando avrai foto tue dei voli, inseriscile
dove servono con questo schema — restano leggere e non fanno "saltare" il layout:

```html
<img src="assets/img/tetto.jpg" width="1200" height="900"
     alt="descrivi cosa si vede" loading="lazy" decoding="async">
```

Esportale a 1200 px di lato lungo, convertile in WebP (su [squoosh.app](https://squoosh.app))
e tieniti sotto i 150 KB per foto.

`assets/img/og-cover.svg` è l'anteprima che si vede condividendo il link. Alcune
piattaforme non leggono gli SVG: quando puoi esporta una JPG 1200×630, chiamala
`og-cover.jpg` e aggiorna i due riferimenti in `index.html`.

## Dopo la pubblicazione

1. Aggiorna `<lastmod>` in `sitemap.xml`.
2. Invia la sitemap da [Google Search Console](https://search.google.com/search-console).
3. Apri un **profilo Google Business** con la zona di attività: per "ispezione tetti
   Mantova" conta più di qualsiasi cosa scritta nella pagina.

## Cookie

Il sito non installa nessun cookie e per questo non ha il banner di consenso. Se aggiungi
Google Analytics, una mappa incorporata o un pixel Meta, ti servono il banner e
l'aggiornamento della Cookie Policy.
