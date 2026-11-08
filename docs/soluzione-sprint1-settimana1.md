# 🏆 Guida Passo-Passo & Soluzione di Riferimento — Sprint 1 • Settimana 1 (Classe 5ITA)

**Progetto:** La Ciacola di Feltre (`makiumjs/Progetto_LaCiacola`)  
**Docente:** Prof. Cassarino | **Materia:** GPOI (Gestione Progetto e Organizzazione d'Impresa)

---

## ⚠️ Regola Tassativa della Settimana 1
È severamente **VIETATO** modificare i file `.html` o fare commit/push diretti sul branch `main`.  
La sessione odierna è dedicata a:
1. **Board Scrumban su GitHub** con apertura di **3 Issue (User Story)** per ciascun Feature Team.
2. **Ricerca dei contenuti reali** nel file locale `bozza-<tema>.txt` (zero *lorem ipsum*).
3. **Progettazione dello schema HTML5 semantico** nel file locale `albero-<tema>.md` (zero `<div>` e zero `<span>`) validato dal QA.

---

## 🛠️ 0. Configurazione e Collegamento della Board Scrumban su GitHub

### Come collegare le 3 Issue alla Board
1. Vai nella scheda **[Issues](https://github.com/makiumjs/Progetto_LaCiacola/issues)** del repository e clicca **New issue** $\rightarrow$ **Get started** su **"User Story (Feature Team)"**.
2. Compila il titolo con il formato `[Sprint 1 - Team X] Titolo della User Story` e compila tutte le sezioni del template.
3. Nella colonna destra della Issue appena creata:
   * Se utilizzate la **Board centrale del repository** ([Projects](https://github.com/makiumjs/Progetto_LaCiacola/projects)), clicca sulla rotellina di **Projects**, seleziona la Board **`Scrumban 5ITA — La Ciacola`** e imposta lo stato su **`To Do`**.
   * Se lo Scrum Master crea una **Board sul proprio profilo GitHub** (*Avatar in alto a destra $\rightarrow$ Your projects $\rightarrow$ New project $\rightarrow$ Board*), deve impostare la visibilità su **Public** (*`...` $\rightarrow$ Settings $\rightarrow$ Visibility $\rightarrow$ Public*), creare le 4 colonne (`To Do`, `In Progress`, `In Review`, `Done`), cliccare **`+ Add item`** in fondo a `To Do`, digitare `#`, scegliere `makiumjs/Progetto_LaCiacola` e selezionare le 3 Issue del proprio Team.

| Feature Team | Pagina | Scrum Master | Product Specialist | QA & Accessibilità | Core Developer |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Team 1** | [`storia.html`](../storia.html) | **Di Dato** (`lorenzodidato-a11y`) | **De Marzo** | **Cirillo** | **Pavan** |
| **Team 2** | [`musei.html`](../musei.html) | **Corso** (`orsoCorso`) | **Xing** | **Lika** (`likassss`) | **Romaniuk** |
| **Team 3** | [`eventi.html`](../eventi.html) | **Pizzolon** (`albertopizzolon-roma`) | **Pizzolon** *(con team)* | **Fongaro** (`davidefongaro`) | **Merlo** (`andreamerlo-glitch`) |
| **Team 4** | [`mobilita.html`](../mobilita.html) | **Facchin** | **Facchin** *(con team)* | **Bordin** (`Brodin67`) | **Romagna** (`francesco-roma-gna`) |

---

## 🏛️ FEATURE TEAM 1 — `storia.html` (Di Dato, De Marzo, Cirillo, Pavan)

### 1. Le 3 User Story su GitHub — **DI DATO (Scrum Master)**
* **Issue 1**: `[Sprint 1 - Team 1] Sezione Evoluzione Storica (Feltria Romana e Dedizione a Venezia)`
  * **Come** turista appassionato di storia **Voglio** leggere le tappe dalla *Feltria* romana (49 a.C.) alla dedizione a Venezia (1404) e ricostruzione del 1510 **Affinché** possa comprendere l'origine rinascimentale della Cittadella.
* **Issue 2**: `[Sprint 1 - Team 1] Schede Monumenti Simbolo (Piazza Maggiore, Castello e Porte Storiche)`
  * **Come** visitatore del centro storico **Voglio** consultare 4 schede `<article>` dedicate a Piazza Maggiore, Castello di Alboino, Porte urbane (Imperiale, Oria, Pusterla) e Palazzi affrescati **Affinché** possa seguire un itinerario autonomo lungo Via Mezzaterra e Via Luzzo.
* **Issue 3**: `[Sprint 1 - Team 1] Tabella Cronologica Accessibile e Glossario in Aside`
  * **Come** utente con screen reader **Voglio** una `<table>` dotata di `<caption>` e `<th scope>` con le date storiche marcate in `<time>` e un `<aside>` con `<dl>` sul glossario architettonico **Affinché** possa orientarmi rapidamente tra epoche e termini tecnici.

### 2. File `bozza-storia.txt` — **DE MARZO (Product Specialist)**
```text
BOZZA CONTENUTI REALI — TEAM 1 (storia.html)
Redattore: De Marzo (Product Specialist)

1. DALLE ORIGINI AL MUNICIPIUM ROMANO E SERENISSIMA
- 49 a.C. (datetime="-0049"): Feltria diventa municipium romano (tribù Menenia). Area archeologica ipogea sotto Piazza Duomo (oltre 1.000 mq, battistero paleocristiano).
- 15 giugno 1404 (datetime="1404-06-15"): Dedizione spontanea di Feltre alla Serenissima Repubblica di Venezia.
- Estate 1510 (datetime="1510"): Incendio del borgo medievale da parte delle truppe imperiali di Massimiliano d'Asburgo (Guerra della Lega di Cambrai) e successiva ricostruzione cinquecentesca in pietra e affreschi (1510-1530).

2. MONUMENTI SIMBOLO DELLA CITTADELLA
- Piazza Maggiore: Palazzo della Ragione (portico palladiano), Palazzo Guarnieri, Chiesa di San Rocco (1599), Fontane Lombardesche di Tullio Lombardo (1519-1522), Colonna con Leone di San Marco.
- Castello di Alboino: Torre del Campanon (altezza 34 metri) e Torre dell'Orologio.
- Le 3 Porte Urbane:
  * Porta Imperiale (ovest, edificata 1489, restaurata 1545): inizio di Via Mezzaterra.
  * Porta Oria (est): accesso orientale verso Belluno.
  * Porta Pusterla (sud, 1493): collegata al Duomo tramite le Scale Coperte.
- Palazzi Affrescati (Via Mezzaterra e Via Luzzo): Palazzo Muffoni, Palazzo Cumano, Casa Crico-Tauro, Palazzo Salce (cicli pittorici di Lorenzo Luzzo detto il Morto da Feltre).

3. GLOSSARIO ARCHITETTONICO (per <aside> + <dl>)
- Sentiero di Ronda: camminamento di guardia sulle Mura Veneziane meridionali.
- Fontane Lombardesche: vasche monumentali in pietra d'Istria (Tullio Lombardo) per riserva idrica.
- Graffito e Affresco: decorazioni parietali cinquecentesche sulle facciate ricostruite post-1510.

4. RECAPITI (<address> nel footer)
- Percorso storico: da Porta Imperiale a Porta Oria passando per Piazza Maggiore — 32032 Feltre (BL)
- Email visite guidate: musei@comune.feltre.bl.it
```

### 3. File `albero-storia.md` + Checklist QA — **PAVAN (Core Dev) & CIRILLO (QA)**
```markdown
# Albero Semantico HTML5 — `storia.html` (Zero `<div>` / Zero `<span>`)
Progettazione: Pavan (Core Dev) | Validazione WCAG 2.1 AA+: Cirillo (QA)

- `body`
  - `a.salto-contenuto[href="#contenuto-principale"]` ("Salta al contenuto principale")
  - `header`
    - `p` (Sottotitolo redazione Team 1)
    - `h1` (**UNICO H1**: "Storia, Borgo Medievale e Mura Antiche di Feltre")
    - `p` (Lead introduttivo)
    - `nav[aria-label="Navigazione principale"]` > `ul` > 5 `li` (`a[aria-current="page"]` su `storia.html`)
  - `main#contenuto-principale`
    - `section[aria-labelledby="titolo-evoluzione-storica"]`
      - `h2#titolo-evoluzione-storica` ("Oltre Due Millenni di Storia tra Alpi e Serenissima")
      - `figure` > `img[src="img/mura-veneziane-feltre.jpg"][alt="..."][width="800"][height="450"]` + `figcaption`
      - `article` > `h3` ("Dalla Feltria Retica al Municipium Romano") + `p` con `<time datetime="-0049">`
      - `article` > `h3` ("La Dedizione a Venezia e la Ricostruzione del Cinquecento") + `p` con `<time datetime="1404-06-15">` e `<time datetime="1510">`
    - `section[aria-labelledby="titolo-monumenti-cittadella"]`
      - `h2#titolo-monumenti-cittadella` ("I Luoghi Simbolo della Cittadella e delle Mura")
      - `article` > `h3` ("Piazza Maggiore e le Fontane Lombardesche")
      - `article` > `h3` ("Il Castello di Alboino e la Torre dell'Orologio") con `<data value="34">`
      - `article` > `h3` ("Porta Imperiale, Porta Oria e Porta Pusterla")
      - `article` > `h3` ("I Palazzi Affrescati di Via Mezzaterra e Via Luzzo")
    - `section[aria-labelledby="titolo-cronologia-tabella"]`
      - `h2#titolo-cronologia-tabella` ("Cronologia Storica e Caratteristiche delle Fortificazioni")
      - `table`
        - `caption`
        - `thead` > `tr` > 4 `th[scope="col"]` (Epoca/Anno, Opera/Evento, Collocazione, Visitabilità)
        - `tbody` > 5 `tr` (ciascuna con `th[scope="row"]` contenente `<time>` + 3 `td`)
    - `aside[aria-labelledby="titolo-glossario-storico"]`
      - `h2#titolo-glossario-storico` ("Glossario Architettonico della Cittadella")
      - `dl` > 3 coppie `dt` + `dd`
  - `footer`
    - `address` (Recapiti e `mailto:musei@comune.feltre.bl.it`)
    - `p` (Copyright con `<time datetime="2026">`–`<time datetime="2027">`)
```

---

## 🎨 FEATURE TEAM 2 — `musei.html` (Corso, Xing, Lika, Romaniuk)

### 1. Le 3 User Story su GitHub — **CORSO (Scrum Master)**
* **Issue 1**: `[Sprint 1 - Team 2] Schede dei 4 Poli Culturali con Indirizzi Semantici`
  * **Come** visitatore culturale **Voglio** 4 `<article>` dedicati a Museo Civico, Galleria Rizzarda, Museo Diocesano e Teatro de la Sena corredati da `<address>` **Affinché** possa conoscere le collezioni e raggiungere ogni sede.
* **Issue 2**: `[Sprint 1 - Team 2] Tabella Accessibile Orari, Biglietti e Feltre Musei Card`
  * **Come** turista ipovedente che usa uno screen reader **Voglio** una tabella comparativa di orari, prezzi intero/ridotto e servizi di accessibilità con `<caption>`, `<th scope="col">` e `<th scope="row">` **Affinché** possa pianificare la visita in autonomia.
* **Issue 3**: `[Sprint 1 - Team 2] Riquadro Aside Agevolazioni Scuole e Gratuità di Legge`
  * **Come** docente accompagnatore **Voglio** un `<aside>` con lista di definizione `<dl>` sui contatti della Segreteria Didattica e sulle gratuità **Affinché** possa prenotare i laboratori per le scolaresche.

### 2. File `bozza-musei.txt` — **XING (Product Specialist)**
```text
BOZZA CONTENUTI REALI — TEAM 2 (musei.html)
Redattore: Xing (Product Specialist)

1. I 4 POLI CULTURALI FELTRINI (4 <article> con <address>)
- Museo Civico di Feltre (Palazzo Villabruna, istituito 1903):
  * Indirizzo: Via Lorenzo Luzzo, 23 — 32032 Feltre (BL)
  * Collezioni: statua marmorea di Esculapio (II sec. d.C.), Pinacoteca (Gentile Bellini, Cima da Conegliano, Lorenzo Luzzo, Pietro Marescalchi, Sebastiano Ricci).
- Galleria d'Arte Moderna "Carlo Rizzarda":
  * Indirizzo: Palazzo Cumano, Via Paradiso, 8 — 32032 Feltre (BL)
  * Collezioni: capolavori in ferro battuto Liberty/Art Déco di Carlo Rizzarda (1883-1931), dipinti di Felice Casorati, Egon Schiele, Pompeo Mariani, vetri di Murano.
- Museo Diocesano d'Arte Sacra Belluno-Feltre:
  * Indirizzo: Ex Vescovado Vecchio, Via Paradiso, 19 — 32032 Feltre (BL)
  * Collezioni: Calice del diacono Orso (VI sec. d.C.), croci gotiche, paramenti veneziani, sculture lignee di Andrea Brustolon.
- Teatro de la Sena ("La Piccola Fenice"):
  * Indirizzo: Piazza Maggiore, 1 (Palazzo della Ragione) — 32032 Feltre (BL)
  * Storia: ridisegnato nel 1813 da Giannantonio Selva, decorazioni e sipario di Tranquillo Orsi (1814), teatro degli esordi di Carlo Goldoni.

2. TABELLA ORARI, TARIFFE E ACCESSIBILITÀ (Lunedì chiuso)
- Museo Civico: Mar-Dom 10:00-13:00 / 15:00-18:00 | Intero € 5,00 | Ridotto € 3,00 | Schede tattili e alta leggibilità.
- Galleria Rizzarda: Mar-Dom 10:00-13:00 / 15:00-18:00 | Intero € 5,00 | Ridotto € 3,00 | Ascensore ai piani e bagni attrezzati.
- Museo Diocesano: Ven-Dom 09:30-13:00 / 14:30-18:00 | Intero € 7,00 | Ridotto € 5,00 | Senza barriere, audioguide IT/EN.
- Teatro de la Sena: Sab-Dom visite guidate ore 11:00 e 16:00 | Intero € 4,00 | Ridotto € 2,50 | Accesso platea accompagnato.
- Feltre Musei Card (Cumulativo 30 giorni): Intero € 14,00 | Ridotto € 9,00 | Gratuito disabili + accompagnatore.

3. DIDATTICA E CONTATTI (<aside>)
- Tariffa scuole: € 2,00 ad alunno (prenotazione almeno 7 giorni prima).
- Segreteria Didattica: Tel. +39 0439 885242 — Email: musei@comune.feltre.bl.it
- Gratuità: under 14 con familiari, persone con disabilità + 1 accompagnatore, giornalisti, membri ICOM.
```

### 3. File `albero-musei.md` + Specifica Tabelle — **ROMANIUK (Core Dev) & LIKA (QA)**
```markdown
# Albero Semantico HTML5 — `musei.html` (Zero `<div>` / Zero `<span>`)
Progettazione: Romaniuk (Core Dev) | Specifica Tabelle WCAG: Lika (QA)

- `body`
  - `a.salto-contenuto[href="#contenuto-principale"]`
  - `header` > `p` + `h1` (**UNICO H1**: "Musei, Gallerie d'Arte e Teatro a Feltre") + `p` + `nav[aria-label="Navigazione principale"]`
  - `main#contenuto-principale`
    - `section[aria-labelledby="titolo-polo-museale"]`
      - `h2#titolo-polo-museale` ("Le Istituzioni Culturali del Polo Feltrino")
      - `figure` > `img[src="img/museo-civico-facciata.jpg"][alt="..."]` + `figcaption`
      - `article` > `h3` ("Museo Civico di Feltre") + `p` (`<time datetime="1903">`) + `address`
      - `article` > `h3` ("Galleria d'Arte Moderna Carlo Rizzarda") + `p` + `address`
      - `article` > `h3` ("Museo Diocesano d'Arte Sacra Belluno-Feltre") + `p` + `address`
      - `article` > `h3` ("Teatro de la Sena (La Piccola Fenice)") + `p` + `address`
    - `section[aria-labelledby="titolo-orari-tariffe"]`
      - `h2#titolo-orari-tariffe` ("Orari di Apertura e Biglietteria Unificata")
      - `table`
        - `caption` ("Prospetto ufficiale degli orari, delle tariffe e dei servizi di accessibilità dei musei di Feltre")
        - `thead` > `tr` > 5 `th[scope="col"]` (Sede Museale, Giorni e Orari, Biglietto Intero, Biglietto Ridotto, Accessibilità)
        - `tbody` > 5 `tr` > `th[scope="row"]` (nome museo) + 4 `td` (orari con `<time datetime="HH:MM">`, prezzi in `&euro;`, note accessibilità)
    - `aside[aria-labelledby="titolo-agevolazioni-scuole"]`
      - `h2#titolo-agevolazioni-scuole` ("Visite Didattiche per Scuole e Gruppi")
      - `p` (con `<data value="7">7 giorni</data>`)
      - `dl` > 2 coppie `dt` + `dd` (link `tel:+390439885242` e `mailto:musei@comune.feltre.bl.it`)
  - `footer` > `address` + `p`
```

---

## 🎪 FEATURE TEAM 3 — `eventi.html` (Pizzolon, Fongaro, Merlo)

### 1. Le 3 User Story su GitHub — **PIZZOLON (Scrum Master & Product Sp.)**
* **Issue 1**: `[Sprint 1 - Team 3] Sezione Palio di Feltre e Schede dei 4 Quartieri Storici`
  * **Come** visitatore estivo **Voglio** conoscere la storia del Palio dei Quindici Ducati d'Oro (1404) e i 4 Quartieri (Castello, Duomo, Port'Oria, Santo Stefano) in `<article>` dedicati **Affinché** possa seguire le 4 gare e i cortei storici.
* **Issue 2**: `[Sprint 1 - Team 3] Rassegna Grandi Manifestazioni (Artigianato, Giro delle Mura, San Matteo, Sportful)`
  * **Come** cittadino o turista **Voglio** leggere le schede delle 4 grandi manifestazioni annuali con dati tecnici marcati in `<data>` **Affinché** possa scoprire l'offerta culturale e sportiva di Feltre durante tutto l'anno.
* **Issue 3**: `[Sprint 1 - Team 3] Tabella Calendario 2026-2027 con Tag Time ISO e Aside Logistica Spettatori`
  * **Come** utente che consulta il calendario eventi **Voglio** una `<table>` accessibile con tutte le date in formato `<time datetime="AAAA-MM-GG">` e un `<aside>` con i recapiti dell'Associazione Palio **Affinché** possa organizzare la trasferta e trovare i posti riservati per disabili.

### 2. File `bozza-eventi.txt` — **PIZZOLON (Product Specialist)**
```text
BOZZA CONTENUTI REALI — TEAM 3 (eventi.html)
Redattore: Pizzolon (Product Specialist)

1. PALIO DI FELTRE (Rievocazione dedizione 1404 — Quindici Ducati d'Oro)
- 4 Gare ufficiali: Tiro con l'arco, Staffetta, Tiro alla fune, Corsa dei cavalli a Pra' del Moro.
- I 4 Quartieri:
  * Quartiere Castello: Colori Verde e Nero | Simbolo: Leone | Zona: Cittadella alta e Piazza Maggiore.
  * Quartiere Duomo: Colori Giallo e Blu | Simbolo: Aquila | Zona: Concattedrale San Pietro e Borgo Ruga.
  * Quartiere Port'Oria: Colori Rosso e Blu | Simbolo: Grifone | Zona: Porta orientale e frazioni est.
  * Quartiere Santo Stefano: Colori Giallo e Rosso | Simbolo: Cavallo | Zona: Porta Imperiale e versante ovest.

2. GRANDI MANIFESTAZIONI ANNUALI
- Mostra dell'Artigianato Artistico e Tradizionale (fine giugno): forgiatura ferro battuto nei palazzi della Cittadella.
- Giro delle Mura Città di Feltre (fine agosto): corsa in notturna di 9,5 km, Seven Laps e Campionato Europeo Vigili del Fuoco.
- Antica Fiera di San Matteo e Festa della Noce Feltrina (terza domenica di ottobre): oltre 200 banchi in centro e valorizzazione Morone di Feltre.
- Granfondo Sportful Dolomiti Race (metà giugno): 204 km e 5.000 m di dislivello con partenza da Largo Castaldi.

3. CALENDARIO DATE ISO (<time datetime="...">)
- Antica Fiera di San Matteo: 2026-10-18 (Largo Castaldi e Via Roma, ingresso gratuito).
- Mercatino di Natale in Cittadella: 2026-12-08 (Piazza Maggiore e Via Mezzaterra, ingresso libero).
- Sportful Dolomiti Race: 2027-06-20 (Largo Castaldi).
- Mostra dell'Artigianato Artistico: dal 2027-06-24 al 2027-06-27 (Cittadella, biglietto unico).
- Palio di Feltre (XLVI Edizione): dal 2027-08-06 al 2027-08-08 (Piazza Maggiore e Pra' del Moro).
- Giro delle Mura in Notturna: 2027-08-28 ore 19:00–23:30 (Mura Veneziane, visione libera).

4. CONTATTI E ACCESSIBILITÀ (<aside> e <footer>)
- Segreteria Associazione Palio Città di Feltre: Piazzale Parmeggiani, 1 — 32032 Feltre (BL) — Tel. +39 0439 840216
- Pedane riservate disabili in Piazza Maggiore e Arena Pra' del Moro.
- Email redazione eventi: cultura@comune.feltre.bl.it
```

### 3. File `albero-eventi.md` + Guida `<time>` — **MERLO (Core Dev) & FONGARO (QA)**
```markdown
# Albero Semantico HTML5 — `eventi.html` (Zero `<div>` / Zero `<span>`)
Progettazione: Merlo (Core Dev) | Guida `<time>` e Gerarchia Titoli: Fongaro (QA)

- `body`
  - `a.salto-contenuto[href="#contenuto-principale"]`
  - `header` > `p` + `h1` (**UNICO H1**: "Eventi, Palio di Feltre e Tradizioni Popolari") + `p` + `nav[aria-label="Navigazione principale"]`
  - `main#contenuto-principale`
    - `section[aria-labelledby="titolo-palio-feltre"]`
      - `h2#titolo-palio-feltre` ("Il Palio di Feltre: La Sfida per i Quindici Ducati d'Oro")
      - `figure` > `img[src="img/palio-di-feltre-piazza.jpg"][alt="..."]` + `figcaption`
      - 4 `article` (uno per Quartiere) > ciascuno con `h3` + `p`
    - `section[aria-labelledby="titolo-grandi-rassegne"]`
      - `h2#titolo-grandi-rassegne` ("Le Grandi Manifestazioni Annuali della Città")
      - 4 `article` (Mostra Artigianato, Giro delle Mura con `<data value="9.5">`, Fiera di San Matteo, Sportful con `<data value="204">` e `<data value="5000">`) > ciascuno con `h3` + `p`
    - `section[aria-labelledby="titolo-calendario-tabella"]`
      - `h2#titolo-calendario-tabella` ("Calendario Ufficiale degli Eventi 2026–2027")
      - `table`
        - `caption`
        - `thead` > `tr` > 4 `th[scope="col"]` (Manifestazione, Periodo, Luogo, Modalità di Accesso)
        - `tbody` > 6 `tr` > `th[scope="row"]` + 3 `td` (tutte le date avvolte in `<time datetime="AAAA-MM-GG">` e orari in `<time datetime="HH:MM">`)
    - `aside[aria-labelledby="titolo-consigli-palio"]`
      - `h2#titolo-consigli-palio` ("Informazioni Pratiche per gli Spettatori del Palio")
      - `p` (con link contestuale a `mobilita.html`) + `dl` > 2 coppie `dt` + `dd`
  - `footer` > `address` + `p`
```

---

## 🚌 FEATURE TEAM 4 — `mobilita.html` (Facchin, Bordin, Romagna)

### 1. Le 3 User Story su GitHub — **FACCHIN (Scrum Master & Product Sp.)**
* **Issue 1**: `[Sprint 1 - Team 4] Sezione Nodo Intermodale (Stazione FS, Dolomiti Bus, Ascensori e Ciclovie)`
  * **Come** viaggiatore senz'auto o persona a mobilità ridotta **Voglio** 4 `<article>` dedicati a Stazione FS, Autolinee Dolomiti Bus, Ascensori pubblici gratuiti e Ciclovie **Affinché** possa salire in Cittadella evitando barriere architettoniche.
* **Issue 2**: `[Sprint 1 - Team 4] Tabella Accessibile Parcheggi di Attestamento e Stalli Disabili CUDE`
  * **Come** automobilista o camperista **Voglio** una `<table>` con `<caption>` e `<th scope>` che elenchi capienza, stalli disabili, tariffe e distanza dalla ZTL per i 5 parcheggi principali **Affinché** possa sostare senza incorrere in sanzioni ZTL.
* **Issue 3**: `[Sprint 1 - Team 4] Riquadro Aside Numeri Utili, Emergenze e Presidi Sanitari`
  * **Come** cittadino o turista in emergenza **Voglio** un `<aside>` con `<dl>` e link telefonici attivi (`href="tel:..."`) per 112, Ospedale di Feltre, Polizia Locale, Radio Taxi e Dolomiti Bus **Affinché** possa chiamare soccorso o assistenza con un tocco.

### 2. File `bozza-mobilita.txt` — **FACCHIN (Product Specialist)**
```text
BOZZA CONTENUTI REALI — TEAM 4 (mobilita.html)
Redattore: Facchin (Product Specialist)

1. TRASPORTO PUBBLICO, ASCENSORI E CICLOVIE (4 <article>)
- Stazione Ferroviaria di Feltre (Viale Giuseppe Mazzini, a 600 m dalla Cittadella):
  * Linea RFI/Trenitalia Padova – Montebelluna – Belluno / Calalzo (treni cadenzati ogni ora).
  * Accessibilità: banchine rialzate a 55 cm, sottopasso, percorsi tattili Loges, assistenza Sala Blu RFI.
- Autolinee Dolomiti Bus e Trentino Trasporti (Piazzale Stazione):
  * Linee per Belluno, Sedico, Pedavena, Fonzaso, Arsiè, Lamon, Primiero / San Martino di Castrozza e Valsugana + servizio estivo Treno+Bici.
- Ascensori Pubblici Gratuiti per la Cittadella:
  * Accesso da Piazza Trento e Trieste (zona Isola / Galleria Romita) con salita diretta a Piazza Maggiore / Castello senza gradini.
- Ciclovie:
  * Tappa dell'itinerario Monaco–Venezia e Anello ciclabile della Valbelluna; rastrelliere e colonnine e-bike in Stazione e a Pra' del Moro.

2. TABELLA PARCHEGGI DI ATTESTAMENTO (ZTL Cittadella)
- Pra' del Moro: Via Pra' del Moro | 450 posti auto + 18 piazzole camper (8 stalli disabili) | Gratuito 24h (camper a pagamento) | 350 m da Porta Imperiale.
- Piazza Isola / Piazzale della Lana: Versante Sud-Ovest | 140 posti (5 stalli disabili) | Disco orario / Parcometro feriale 08:30–19:30 | Accesso diretto ascensori.
- Campo Giorgio: Via G. Marconi | 220 posti auto + bus turistici (6 stalli disabili) | Gratuito senza limiti | 450 m da Duomo e Porta Pusterla.
- Parcheggio Stazione FS: Viale G. Mazzini | 180 posti (4 stalli disabili) | Gratuito | 600 m dal centro.
- Piazza Maggiore (Solo CUDE): Cittadella Alta (da Porta Oria) | 4 stalli esclusivi CUDE | Gratuito con contrassegno | 0 m.

3. NUMERI UTILI E RECAPITI (<aside> con <dl> e <footer> con <address>)
- Emergenza Unica Europea: tel:112 (H24).
- Ospedale Civile "Santa Maria del Prato" (ULSS 1 Dolomiti): Via Bagnols sur Cèze, 3 — Tel. +39 0439 8831.
- Comando Polizia Locale Feltre (ZTL): Piazzetta delle Biade, 1 — Tel. +39 0439 885280 — Email: polizialocale@comune.feltre.bl.it.
- Radio Taxi Stazione FS: Viale Mazzini — Tel. +39 0439 2221.
- Numero Verde Dolomiti Bus: tel:800555771.
```

### 3. File `albero-mobilita.md` + Checklist QA — **ROMAGNA (Core Dev) & BORDIN (QA)**
```markdown
# Albero Semantico HTML5 — `mobilita.html` (Zero `<div>` / Zero `<span>`)
Progettazione: Romagna (Core Dev) | Checklist Tabelle e Link: Bordin (QA)

- `body`
  - `a.salto-contenuto[href="#contenuto-principale"]`
  - `header` > `p` + `h1` (**UNICO H1**: "Mobilità, Parcheggi, Accessibilità e Numeri Utili") + `p` + `nav[aria-label="Navigazione principale"]`
  - `main#contenuto-principale`
    - `section[aria-labelledby="titolo-trasporto-pubblico"]`
      - `h2#titolo-trasporto-pubblico` ("Come Raggiungere Feltre con i Mezzi Pubblici e in Bicicletta")
      - `figure` > `img[src="img/stazione-feltre-mobilita.jpg"][alt="..."]` + `figcaption`
      - `article` > `h3` ("Stazione Ferroviaria di Feltre...") + `p` (con `<data value="55">55 cm</data>`)
      - `article` > `h3` ("Autolinee Extraurbane e Urbane...") + `p`
      - `article` > `h3` ("Ascensori Pubblici Accessibili per la Cittadella Storica") + `p`
      - `article` > `h3` ("Ciclovia Lunga Via delle Dolomiti e Anello Valbelluna") + `p`
    - `section[aria-labelledby="titolo-tabella-parcheggi"]`
      - `h2#titolo-tabella-parcheggi` ("Parcheggi di Attestamento, Tariffe e Stalli Riservati")
      - `table`
        - `caption` ("Elenco dei principali parcheggi pubblici a servizio del centro storico di Feltre")
        - `thead` > `tr` > 5 `th[scope="col"]` (Nome Parcheggio, Indirizzo/Zona, Capienza e Tipologia, Regime Tariffario, Distanza dalla Cittadella)
        - `tbody` > 5 `tr` > `th[scope="row"]` (nome parcheggio) + 4 `td` (orari in `<time datetime="HH:MM">`)
    - `aside[aria-labelledby="titolo-numeri-utili"]`
      - `h2#titolo-numeri-utili` ("Numeri Utili, Emergenze e Presidi Sanitari")
      - `p` + `dl` > 5 coppie `dt` + `dd` (tutti i numeri telefonici con link descrittivi `a[href="tel:..."]`, zero "clicca qui")
  - `footer` > `address` + `p`
```
