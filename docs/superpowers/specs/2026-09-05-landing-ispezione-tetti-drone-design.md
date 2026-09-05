# Landing page — Ispezione tetti con drone (Mantova)

Data: 2026-09-05

## Obiettivo

Landing page singola per un professionista indipendente che offre ispezioni
visive di tetti tramite drone a Mantova e provincia. Priorità in ordine:
contatto (WhatsApp/telefono/email) > chiarezza > velocità > estetica.

Non deve comunicare "grande azienda": tono diretto, niente linguaggio
corporate, niente dati inventati (recensioni, anni di esperienza, numeri,
certificazioni, prezzi).

## Target

Proprietari di case/capannoni, amministratori di condominio, imprese edili,
tecnici, e in particolare persone che vogliono un controllo dopo una
grandinata. Zona: Mantova e provincia (Castiglione delle Stiviere, Suzzara,
Viadana, Porto Mantovano, San Giorgio Bigarello, Curtatone, Borgo Virgilio,
Asola, Goito e comuni limitrofi).

## Stack tecnico

HTML statico + CSS scritto a mano + JS vanilla minimo. Nessun framework,
nessuna build, nessuna libreria esterna pesante. Una sola Google Font (o
font di sistema) con preconnect. Motivazione: priorità assoluta è la
velocità (Lighthouse alto, pochissimo JS, ottimo su mobile) e il sito è una
singola pagina — un framework/bundler aggiungerebbe complessità senza
benefici.

## Struttura file

```
index.html
privacy.html
cookie.html
assets/css/style.css
assets/js/main.js        (menu mobile, eventuale sticky WhatsApp)
assets/img/*.svg         (illustrazioni originali: drone, tetto, coppi, grandine)
robots.txt
sitemap.xml
```

## Sezioni pagina (in ordine, con ancore)

1. **Hero** (`#hero`) — H1 "Ispezione tetti con drone a Mantova", sottotitolo,
   testo breve, CTA primaria "Richiedi un sopralluogo" (→ #contatti), CTA
   secondaria "Scrivimi su WhatsApp" (link `wa.me`). Illustrazione SVG
   drone/tetto al posto di foto/video hero pesante.
2. **Perché controllare il tetto** (`#perche`) — testo breve + 4 punti
   (tegole/coppi danneggiati, elementi spostati, punti critici, controllo
   dopo grandine).
3. **Come funziona** (`#come-funziona`) — 4 step numerati (contatto →
   valutazione → ispezione drone → foto/materiale) + nota che l'ispezione è
   visiva/fotografica e non sostituisce una perizia tecnica.
4. **Dopo la grandine** (`#grandine`) — sezione evidenziata visivamente
   (sfondo leggermente diverso, non un colore acceso), CTA "Richiedi un
   controllo". Nessun prezzo.
5. **Galleria "cosa posso controllare"** (`#galleria`) — illustrazioni SVG
   leggere (tetto in coppi, tegola danneggiata, grandine, drone sopra
   abitazione, vista ravvicinata tetto), lazy-loading nativo per eventuali
   foto reali future.
6. **Zona servita** (`#zona`) — testo + rappresentazione grafica leggera
   della provincia di Mantova (SVG, non mappa embed pesante) con i comuni
   citati nel testo (non come lista SEO forzata).
7. **Contatti** (`#contatti`) — testo breve, pulsanti grandi WhatsApp /
   Telefono / Email. WhatsApp sempre visibile/raggiungibile su mobile
   (bottone sticky in basso).
8. **Footer** — nome professionista (placeholder), tagline, link Privacy
   Policy / Cookie Policy, contatti ripetuti.

## Visual system

- Colori: bianco, grigio molto chiaro, nero/antracite per testo, accento
  terracotta/ruggine discreto (solo su CTA, dettagli piccoli, mai su sfondi
  grandi).
- Niente gradienti vistosi, niente animazioni/scroll-effects superflui,
  niente elementi 3D.
- Molto spazio bianco, tipografia grande e leggibile, bottoni grandi
  (mobile-first, target touch ≥44px).
- Immagini/illustrazioni: SVG inline ottimizzati (nessun file esterno
  pesante per la grafica di base). Se in futuro verranno aggiunte foto
  reali: WebP, `loading="lazy"`, dimensioni esplicite per evitare CLS.

## SEO tecnico

- Title, meta description, H1 unico, H2/H3 gerarchici, URL puliti (pagina
  singola con ancore semantiche).
- JSON-LD `LocalBusiness`/`Service` con area servita = Mantova e provincia
  (comuni citati), senza inventare dati (no recensioni/rating fittizi).
- Open Graph (og:title, og:description, og:image, og:locale it_IT).
- `sitemap.xml`, `robots.txt`.
- Keyword naturali nel testo (ispezione tetti Mantova, controllo tetto
  drone Mantova, danni grandine tetto Mantova, ecc.) — nessun keyword
  stuffing.

## Privacy/Cookie

Nessun tracking di terze parti (no Google Analytics/Meta Pixel) di default
→ sito più veloce e Cookie Policy minima ("nessun cookie di profilazione,
solo eventuali cookie tecnici"). Privacy Policy con placeholder per dati
del titolare (nome, email, indirizzo) da completare.

## Placeholder da sostituire (elenco unico, commentato nel codice)

- Nome/attività del professionista
- Numero di telefono
- Numero WhatsApp (per link `wa.me`)
- Email
- Dominio del sito (per canonical, OG, sitemap, JSON-LD)
- Eventuale indirizzo/zona base esatta

## Fuori scope

- Multi-pagina, blog, CMS, form con backend (i "pulsanti" contatto
  puntano a WhatsApp/tel/mailto — nessun invio dati a server proprio).
- Prezzi, recensioni, certificazioni, numeri di interventi: non vengono
  inventati né inclusi.
- Mappa embed (Google Maps) pesante: sostituita da rappresentazione SVG
  leggera della provincia.
