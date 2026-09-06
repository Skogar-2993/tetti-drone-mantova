# Tetto a posto — Ispezione tetti con drone a Mantova

Sito statico di **Tetto a posto**, servizio di ispezione tetti con drone a Mantova e
provincia. Un solo file HTML con dentro CSS e JavaScript, nessuna libreria, nessun font
scaricato, nessuna richiesta a server esterni. Percorsi relativi: funziona sia online sia
aprendo `index.html` con un doppio clic.

Pagina: **8 KB** compressa, più le fotografie.

## Da sostituire prima di pubblicare

Cerca e sostituisci in `index.html`, `report/index.html`, `privacy-policy/index.html`,
`cookie-policy/index.html`, `sitemap.xml` e `robots.txt`:

| Cerca | Sostituisci con |
|---|---|
| `nome@esempio.it` | la tua email |
| `https://www.esempio.it` | il dominio, senza `/` finale |
| `[Nome Cognome]` | il tuo nome |
| `[Partita IVA]` | la tua partita IVA |

Telefono e WhatsApp sono già impostati su **+39 334 396 7314**.

Poi completa i placeholder fra parentesi quadre nelle due pagine legali (indirizzo,
fornitore di hosting, tempi di conservazione, data).

Nelle FAQ e nel report c'è spazio per il numero di operatore UAS e la polizza
assicurativa: compilali o togli la riga. Non c'è niente di inventato sul tuo conto —
né recensioni, né anni di esperienza, né certificazioni, né prezzi.

## Il dominio

Il nome è **Tetto a posto**. Prima di comprare, verifica che `tettoaposto.it` sia libero
su un registrar (Aruba, Register, Netsons…). Se è occupato, valuta `tettoaposto.com` o
aggiungi la località: `tettoapostomantova.it`.

Quando ce l'hai, sostituisci `https://www.esempio.it` ovunque.

## Pubblicazione

Carica tutto tranne `docs/`, `report/` e questo README:

```
index.html   robots.txt   sitemap.xml   assets/img/   privacy-policy/   cookie-policy/
```

`report/` è uno strumento interno: tienilo sul tuo computer. Se decidi di caricarlo
online resta comunque escluso dai motori di ricerca (`noindex`), ma chiunque abbia
l'indirizzo può aprirlo, quindi non lasciarci dentro dati di clienti.

Sull'hosting attiva compressione gzip o brotli, se puoi.

## Il report per i clienti

`report/index.html` è un modello di report da consegnare dopo l'ispezione.

1. Aprilo nel browser (doppio clic).
2. Clicca su un campo e scrivi: tutto il testo in grigio corsivo è compilabile.
3. Carica fino a quattro foto negli spazi in fondo.
4. **Stampa / PDF** → scegli "Salva come PDF".

Le righe dei rilievi si aggiungono e si tolgono. Il livello di attenzione ha tre gradi:
*nessuna anomalia*, *da monitorare*, *da approfondire*.

**Salva bozza** conserva il testo nel browser se devi interrompere, ma **non le foto**:
sono troppo pesanti per lo spazio disponibile e vanno ricaricate. Nessun dato esce dal
tuo computer.

Il riquadro finale sui limiti è la parte più importante: dice che l'ispezione è visiva e
fotografica, che non sostituisce una perizia e che i livelli non esprimono giudizi sulla
gravità o sulla sicurezza. Serve a te quanto al cliente — non toglierlo.

## Le fotografie

Le foto in `assets/img/` sono tue, scattate col drone. Quando ne aggiungi altre:

```html
<img src="assets/img/tetto.webp" width="1200" height="900"
     alt="descrivi cosa si vede" loading="lazy" decoding="async">
```

Esportale a 1200 px di lato lungo, convertile in **WebP** su
[squoosh.app](https://squoosh.app) con qualità 80 e tieniti sotto i 150 KB per foto.
Tieni sempre `width` e `height` con le proporzioni vere: impediscono alla pagina di
"saltare" mentre carica.

> **Da sistemare:** `veduta-provincia-mantova.jpg` pesa **4 MB** — non è mai passata da
> Squoosh, è il file originale del drone a 4000×2250. È in lazy loading, quindi non
> rallenta il primo schermo, ma su rete mobile sono una quindicina di secondi. Rifalla a
> 1200 px in WebP: scenderà sotto i 200 KB.

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
