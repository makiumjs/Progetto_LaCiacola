# Report Formale di Fine Sprint — GPOI (Classe 5ITA)

**Testata / Progetto:** La Ciacola di Feltre — Giornale e Portale Turistico-Culturale Cittadino  
**Sprint N.:** `1`  
**Periodo di riferimento:** Dal `[17/10/2026]` al `[13/11/2026]` (4 settimane — 8 ore di laboratorio)  
**Feature Team:**
- [ ] **Team 1 (`storia.html`):** Di Dato, De Marzo, Cirillo, Pavan
- [ ] **Team 2 (`musei.html`):** Corso, Xing, Lika, Romaniuk
- [ ] **Team 3 (`eventi.html`):** Pizzolon, Fongaro, Merlo
- [x] **Team 4 (`mobilita.html`):** Facchin, Bordin, Romagna

**Data di consegna:** `[12/11/2026]`

---

## 1. Ruoli Ricoperti dal Team nello Sprint Corrente

| :--- | :--- | :--- | :-: |
| **Scrum Master** (Coordinatore e Redattore Report) + **Product Specialist** (Contenuti e Coerenza) | Facchin | `@[WorseThanEpstine]` | `[6/8]` |
| **QA & Accessibilità** (Revisione Codice e WCAG) | Bordin | `@[Bordin67]` | `[8/8]` |
| **Core Developer** (Implementazione HTML5 e CSS3) | Romagna | `@[francesco-roma-gna]` | `[2/8]` |

---

## 2. Sprint Goal e Riepilogo Esecutivo

- **Obiettivo dello Sprint (Sprint Goal):**  
  Realizzare la pagina `mobilita.html` de La Ciacola di Feltre in HTML5 semantico puro, con contenuti reali e verificati sui parcheggi e trasporti, una tabella accessibile delle informazioni e la piena conformità alla Definition of Done (validazione W3C e accessibilità WCAG 2.1 AA+).
- **Stato di Raggiungimento dello Sprint Goal:** `[Raggiunto al 100%]`
- **Sintesi del valore rilasciato:**  
  Sul branch `sprint1/team4-mobilita`, sono stati pubblicati: articoli sui trasporti di Feltre, una tabella accessibile con il calendario dei parcheggi (con `<caption>`, `<thead>`, `<tbody>`, `<th scope>`), per le date, lo skip-link, la navigazione unificata con le altre pagine e le regole CSS per contrasto e focus da tastiera.

---

## 3. Metriche Scrumban & Tracciamento Attività (Issue & Pull Request)

### 3.1 Indicatori Quantitativi dello Sprint
- **User Story pianificate:** `3`
- **User Story completate (`Done`):** `[3]`
- **Tasso di completamento:** `[100 %]`
- **Pull Request aperte e revisionate:** `[1]`
- **Rotture della pipeline CI (`w3c-validator.yml`) riscontrate e risolte:** `[1]`

---

## 4. Verifica di Conformità alla Definition of Done (Audit QA)

| Controllo Architetturale e Qualitativo | Esito (`OK` / `KO`) | Note Tecniche o Evidenze |
| :--- | :-: | :--- |
| **Zero `<div>` e Zero `<span>` nel file HTML** | `[OK]` | Verificato tramite `grep` locale e GitHub Actions. |
| **Validazione W3C Nu Html Checker** | `[OK]` | Zero errori e zero warning sul markup HTML5. |
| **Skip-link presente e funzionante con `Tab`** | `[OK]` | `<a href="#contenuto-principale" class="salto-contenuto">` testato. |
| **Gerarchia titoli `<h1>` $\rightarrow$ `<h2>` $\rightarrow$ `<h3>`** | `[OK]` | Un solo `<h1>`, nessun salto di livello rilevato. |
| **Tabelle con `<caption>` e `<th scope="...">`** | `[OK]` | Tutte le tabelle dati rispettano lo standard di accessibilità. |
| **Immagini in `img/` in `kebab-case` con `alt`** | `[OK]` | Tutti i file grafici sono minuscoli con descrizione contestuale. |
| **Blocco `<nav>` unificato con gli altri 3 Team** | `[OK]` | Navigazione principale identica su tutte le 5 pagine, con `aria-current="page"` su Eventi. |
| **Assenza totale di testo *lorem ipsum*** | `[OK]` | Tutti i testi riguardano dati reali della Città di Feltre. |

---

## 5. Contributi Individuali per Ruolo

- **Scrum Master e Product Specialist ([Facchin]):**  
  Coordinamento del team e gestione della Board Scrumban, risoluzione dei blocchi e stesura del presente report. Come Product Specialist: ricerca e verifica delle fonti sui trasporti di Feltre,
- **QA & Accessibilità ([Bordin]):**  
  'Ha eseguito i controlli locali tramite il terminale di VS Code per garantire l'assenza dei tag vietati <div> e <span>. Ha intercettato e fatto correggere un errore critico di validazione W3C riguardante l'annidamento errato dei titoli (<h3>/<h4>) nei quartieri e un attributo datetime non valido nella tabella. Ha controllato che nella tabella trasporti i tag <caption> e i corretti attributi scope fossero al loro posto secondo le specifiche WCAG 2.1 AA+, verificando infine lo spostamento dell'attributo aria-current="page" sul menu di navigazione..
- **Core Developer ([Romagna]):**  
  Creazione del branch `sprint1/team4-mobilita` e implementazione di `eventi.html` con tag semantici (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<table>`, `<time>`, `<footer>`) e delle regole CSS3 relative. Commit principali: `[feat(eventi): ...]`, `[a11y(eventi): ...]`.

---

## 6. Retrospettiva di Sprint (Sprint Retrospective)

### Cosa ha funzionato bene (Keep Doing)
- `[La suddivisione dei ruoli e il lavoro su branch dedicato hanno evitato problemi.]`

### Impedimenti e Criticità Riscontrate (Problems / Blockers)
- `[Non ci cono stati problemi.]`

### Azioni di Miglioramento per il Prossimo Sprint (Action Items)
1. `[Comunicare di più tra i vari componenti]`
---

**Firma dello Scrum Master:** `_Facchin Giosue'`  
**Visto di convalida del Team:** `___________________________`
