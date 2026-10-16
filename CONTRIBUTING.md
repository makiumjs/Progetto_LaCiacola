# Guida di Contribuzione & Regole Architetturali (`CONTRIBUTING.md`)

Questo documento definisce il flusso di lavoro ingegneristico obbligatorio per tutti gli studenti della classe **5ITA** impegnati nello sviluppo del **Portale Turistico e Culturale della Città di Feltre ("La Ciaccola")**.

---

## 1. Flusso Git & Gestione dei Branch

> **REGOLA TASSATIVA:** È severamente **VIETATO** effettuare commit o push diretti sul branch `main`. Ogni modifica deve transitare attraverso un branch dedicato e una **Pull Request (PR)** approvata dal responsabile **QA & Accessibilità** del proprio Feature Team.

### 1.1 Convenzione di Nomenclatura dei Branch
Ogni branch deve identificare chiaramente lo Sprint, il Feature Team e lo scopo dell'attività:
- `sprint1/team1-mura-veneziane`
- `sprint2/team2-tabella-orari-musei`
- `sprint3/team3-responsive-eventi`
- `sprint4/team4-accessibilita-parcheggi`
- `fix/team1-correzione-gerarchia-h2`

### 1.2 Ciclo di Vita di una Modifica (Passo dopo Passo)
1. **Sincronizzazione con `main`:**
   ```bash
   git checkout main
   git pull origin main
   ```
2. **Creazione del branch di lavoro:**
   ```bash
   git checkout -b sprint1/team1-storia-cittadella
   ```
3. **Sviluppo e collaudo locale:** modifica i file assegnati al tuo team e verifica i vincoli della *Definition of Done*.
4. **Commit atomici e descrittivi:**
   ```bash
   git add storia.html
   git commit -m "feat(storia): aggiunta sezione mura veneziane e tabella porte storiche"
   ```
5. **Push e apertura Pull Request:**
   ```bash
   git push -u origin sprint1/team1-storia-cittadella
   ```
   Apri la Pull Request su GitHub compilando integralmente il template `.github/PULL_REQUEST_TEMPLATE.md` e assegnando la revisione al compagno con ruolo **QA & Accessibilità**.

---

## 2. Convenzioni per i Messaggi di Commit (Conventional Commits)

Tutti i messaggi di commit devono essere scritti in **italiano** (eccetto il prefisso tecnico standard) seguendo il formato:

```text
<tipo>(<ambito>): <descrizione sintetica all'infinito o sostantivata>
```

### Tipi ammessi:
- `feat`: aggiunta di una nuova sezione, tabella o contenuto informativo.
- `fix`: correzione di un errore di validazione W3C, bug visivo o problema di accessibilità WCAG.
- `style`: modifiche al foglio di stile `css/style.css` o miglioramenti di layout mobile-first.
- `docs`: aggiornamenti alla documentazione in `docs/`, ai Report di Sprint o al `README.md`.
- `a11y`: miglioramenti specifici per l'accessibilità (attributi `alt`, `aria-label`, `scope`, contrasto).

### Ambiti (`<ambito>`) ammessi:
- `index`, `storia`, `musei`, `eventi`, `mobilita`, `css`, `docs`, `ci`.

**Esempi corretti:**
- `feat(musei): inserimento tabella orari e tariffe Galleria Rizzarda`
- `a11y(mobilita): aggiunta attributi scope alle intestazioni della tabella parcheggi`
- `fix(eventi): rimozione salto di livello da h1 a h3 nella sezione Palio`

---

## 3. Definition of Done (DoD) — Vincoli Architetturali Rigorosi

Una *User Story* o una *Pull Request* può essere considerata **Done** (completata e pronta per il merge su `main`) **solo ed esclusivamente** se rispetta tutti i seguenti punti:

### 3.1 HTML5 Semantico Puro
- **Zero `<div>` e Zero `<span>`:** non è ammesso alcun tag generico privo di valore semantico.
- **Tag obbligatori per struttura logica:**
  - `<header>` per l'intestazione di pagina o di articolo.
  - `<nav aria-label="Navigazione principale">` per il menu globale unificato.
  - `<main id="contenuto-principale">` per il corpo centrale unico della pagina.
  - `<section>` per le partizioni tematiche (sempre dotate di un titolo `<h2>`).
  - `<article>` per schede autonome (monumenti, musei, singole manifestazioni, linee di trasporto).
  - `<aside>` per approfondimenti, curiosità storiche, avvisi o contatti rapidi.
  - `<figure>` e `<figcaption>` per immagini corredate da didascalia.
  - `<time datetime="...">` per date storiche, orari e periodi di svolgimento eventi.
  - `<address>` per i recapiti fisici, istituzionali e turistici.
  - `<table>` sempre corredata da `<caption>`, `<thead>`, `<tbody>` e `<th scope="col">` / `<th scope="row">`.
  - `<dl>`, `<dt>`, `<dd>` per glossari, schede tecniche o coppie chiave-valore.

### 3.2 Accessibilità (WCAG 2.1 AA+)
- **Skip-link da tastiera:** il primo elemento dentro `<body>` deve essere `<a href="#contenuto-principale" class="salto-contenuto">Salta al contenuto principale</a>`.
- **Gerarchia dei titoli:** esattamente **un solo `<h1>`** per pagina; i livelli successivi (`<h2>`, `<h3>`) devono seguire un ordine gerarchico rigoroso senza salti.
- **Testo alternativo:** ogni elemento `<img>` deve avere un attributo `alt` descrittivo e contestualizzato.
- **Contrasto e Focus:** rapporto di contrasto testo/sfondo $\ge 4.5:1$ e contorno `:focus-visible` ben visibile durante la navigazione con il tasto `Tab`.

### 3.3 Coerenza Cross-Team e Asset Grafici
- **Barra di Navigazione Unificata:** le 5 pagine (`index.html`, `storia.html`, `musei.html`, `eventi.html`, `mobilita.html`) devono condividere il medesimo blocco `<nav aria-label="Navigazione principale">`.
- **Nomenclatura file in `img/`:** sono ammessi solo nomi in `kebab-case` composti da lettere minuscole, numeri e trattini (es. `museo-civico-facciata.jpg`).
- **Contenuti verificati:** è vietato qualsiasi testo segnaposto (*lorem ipsum*).
- **Pipeline CI Verde:** tutti i controlli automatici definiti in `.github/workflows/w3c-validator.yml` devono risultare superati.
