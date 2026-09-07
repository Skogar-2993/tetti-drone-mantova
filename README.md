# Tetto a posto? — Ispezione tetti con drone a Mantova

Sito statico di **Tetto a posto?**, il servizio di ispezione tetti con drone a Mantova e
provincia. Un solo file HTML con dentro CSS e JavaScript, nessuna libreria, nessun font
scaricato, nessuna richiesta a server esterni. Percorsi relativi: funziona sia online sia
aprendo `index.html` con un doppio clic.

Pagina: **10 KB** compressa. Fotografie: **279 KB** al primo schermo (solo quella dell'hero),
**1216 KB** in tutto scorrendo fino in fondo.

## Da sostituire prima di pubblicare

Cerca e sostituisci in `index.html`, `report/index.html`, `privacy-policy/index.html`,
`cookie-policy/index.html`, `sitemap.xml` e `robots.txt`:

| Cerca | Sostituisci con |
|---|---|
| `nome@esempio.it` | la tua email |
| `https://www.esempio.it` | il dominio, senza `/` finale |
| `[Nome Cognome]` | il tuo nome |

Telefono e WhatsApp sono già impostati su **+39 334 396 7314**.

Nel sito non compare nessuna partita IVA: il servizio è reso come **prestazione
occasionale** da persona fisica, e i dati strutturati dichiarano una persona, non
un'impresa.

Poi completa i placeholder fra parentesi quadre nelle due pagine legali (indirizzo,
fornitore di hosting, tempi di conservazione, data).

Nel piè di pagina del resoconto c'è spazio per il numero di operatore UAS e della polizza:
compilali una volta e restano. Il sito dichiara "pilota abilitato e assicurato" perché lo
sei — non c'è niente di inventato sul tuo conto:
né recensioni, né anni di esperienza, né certificazioni, né prezzi.

## Il dominio

Il nome è **Tetto a posto?** — con il punto interrogativo. Prima di comprare, verifica che `tettoaposto.it` sia libero
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

## Il resoconto per i clienti

`report/index.html` è un modello di resoconto da consegnare dopo il controllo. È volutamente
breve: sei righe di dati, una sintesi, i punti da segnalare, quattro foto.

1. Aprilo nel browser (doppio clic).
2. Clicca su un campo e scrivi: tutto il testo in grigio corsivo è compilabile.
3. Carica fino a quattro foto negli spazi in fondo.
4. **Stampa / PDF** → scegli "Salva come PDF".

Le righe si aggiungono e si tolgono. I tre livelli sono *nulla da segnalare*, *da tenere
d'occhio*, *da far vedere a un tecnico*: dicono cosa merita attenzione senza esprimere
giudizi tecnici che non ti competono.

**Salva bozza** conserva il testo nel browser se devi interrompere, ma **non le foto**:
sono troppo pesanti per lo spazio disponibile e vanno ricaricate. Nessun dato esce dal
tuo computer.

Il riquadro finale sui limiti è la parte più importante: dice che l'ispezione è visiva e
fotografica, che non sostituisce una perizia e che i livelli non esprimono giudizi sulla
gravità o sulla sicurezza. Serve a te quanto al cliente — non toglierlo.

## Le fotografie

Le foto in `assets/img/` sono tue, scattate col drone, e sono già tutte ottimizzate per il
web. Quando ne aggiungi altre:

```html
<img src="assets/img/tetto.webp" width="1200" height="900"
     alt="descrivi cosa si vede" loading="lazy" decoding="async">
```

Esportale a 1200 px di lato lungo, convertile in **WebP** su
[squoosh.app](https://squoosh.app) con qualità 80 e tieniti sotto i 150 KB per foto.
Tieni sempre `width` e `height` con le proporzioni vere: impediscono alla pagina di
"saltare" mentre carica.

`assets/img/og-cover.svg` è l'anteprima che si vede condividendo il link. Alcune
piattaforme non leggono gli SVG: quando puoi esporta una JPG 1200×630, chiamala
`og-cover.jpg` e aggiorna i due riferimenti in `index.html`.

## Dopo la pubblicazione

1. Aggiorna `<lastmod>` in `sitemap.xml`.
2. Invia la sitemap da [Google Search Console](https://search.google.com/search-console).
3. Apri un **profilo Google Business** con la zona di attività: per "ispezione tetti
   Mantova" conta più di qualsiasi cosa scritta nella pagina.

## Prestazione occasionale: cosa ricordare

Il servizio è reso da privato con prestazione occasionale, quindi:

- si documenta con **ricevuta per prestazione occasionale** con ritenuta d'acconto del
  20%, non con fattura;
- oltre **5.000 € lordi all'anno** di compensi scatta l'obbligo di iscrizione alla
  gestione separata INPS;
- se l'attività diventa continuativa e organizzata non è più occasionale e serve la
  partita IVA.

Per i numeri esatti e la tua situazione, sentì un commercialista: qui non c'è nulla di
personalizzato.

## Cookie

Il sito non installa nessun cookie e per questo non ha il banner di consenso. Se aggiungi
Google Analytics, una mappa incorporata o un pixel Meta, ti servono il banner e
l'aggiornamento della Cookie Policy.
