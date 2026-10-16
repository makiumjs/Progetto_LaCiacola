# Report Formale di Fine Sprint — GPOI (Classe 5ITA)

**Testata / Progetto:** La Ciacola di Feltre — Giornale e Portale Turistico-Culturale Cittadino  
**Sprint N.:** `[1 / 2 / 3 / 4]`  
**Periodo di riferimento:** Dal `[GG/MM/AAAA]` al `[GG/MM/AAAA]` (4 settimane — 8 ore di laboratorio)  
**Feature Team:**
- [ ] **Team 1 (`storia.html`):** Di Dato, De Marzo, Cirillo, Pavan
- [ ] **Team 2 (`musei.html`):** Corso, Xing, Lika, Romaniuk
- [ ] **Team 3 (`eventi.html`):** Pizzolon, Fongaro, Merlo
- [ ] **Team 4 (`mobilita.html`):** Facchin, Bordin, Romagna

**Data di consegna:** `[GG/MM/AAAA]`

---

## 1. Ruoli Ricoperti dal Team nello Sprint Corrente

*(Compilare con i cognomi dei membri del proprio Feature Team secondo la rotazione prevista in `docs/pianificazione-sprint.md`. Per i Team 3 e 4 da 3 componenti, indicare il membro che ricopre il doppio ruolo Scrum Master + Product Specialist).*

| Ruolo Aziendale nello Sprint | Cognome Studente | Username GitHub | Ore Presenza Lab (su 8h) |
| :--- | :--- | :--- | :-: |
| **Scrum Master** (Coordinatore e Redattore Report) | `[Cognome]` | `@username` | `[8/8]` |
| **Product Specialist** (Contenuti e Coerenza) | `[Cognome]` | `@username` | `[8/8]` |
| **QA & Accessibilità** (Revisione Codice e WCAG) | `[Cognome]` | `@username` | `[8/8]` |
| **Core Developer** (Implementazione HTML5 e CSS3) | `[Cognome]` | `@username` | `[8/8]` |

---

## 2. Sprint Goal e Riepilogo Esecutivo

- **Obiettivo dello Sprint (Sprint Goal):**  
  `[Descrivere in 2-3 righe l'obiettivo principale prefissato all'inizio delle 4 settimane per La Ciacola di Feltre]`
- **Stato di Raggiungimento dello Sprint Goal:** `[Raggiunto al 100% / Parzialmente raggiunto / Non raggiunto]`
- **Sintesi del valore rilasciato:**  
  `[Riassumere gli articoli, le tabelle, i dati o i miglioramenti CSS/WCAG effettivamente pubblicati sul branch main]`

---

## 3. Metriche Scrumban & Tracciamento Attività (Issue & Pull Request)

### 3.1 Stato delle User Story pianificate nello Sprint

| ID Issue | Titolo della User Story / Attività Redazionale | Stato Finale (`Done` / `Carry-over`) | PR Collegata | Responsabile Principale |
| :-: | :--- | :-: | :-: | :--- |
| `#01` | `[Es. Articolo Mura Veneziane e Porte storiche]` | `Done` | `PR #10` | `[Cognome]` |
| `#02` | `[Es. Tabella accessibile cronologia / orari / parcheggi]` | `Done` | `PR #12` | `[Cognome]` |
| `#03` | `[Es. Audit WCAG contrasto e focus tastiera]` | `Done` | `PR #14` | `[Cognome]` |

### 3.2 Indicatori Quantitativi dello Sprint
- **User Story pianificate:** `[N]`
- **User Story completate (`Done`):** `[N]`
- **Tasso di completamento:** `[XX %]`
- **Pull Request aperte e revisionate:** `[N]`
- **Rotture della pipeline CI (`w3c-validator.yml`) riscontrate e risolte:** `[N]`

---

## 4. Verifica di Conformità alla Definition of Done (Audit QA)

*Sezione compilata in sinergia tra **QA & Accessibilità** e **Scrum Master**.*

| Controllo Architetturale e Qualitativo | Esito (`OK` / `KO`) | Note Tecniche o Evidenze |
| :--- | :-: | :--- |
| **Zero `<div>` e Zero `<span>` nel file HTML** | `[OK]` | Verificato tramite `grep` locale e GitHub Actions. |
| **Validazione W3C Nu Html Checker** | `[OK]` | Zero errori e zero warning sul markup HTML5. |
| **Skip-link presente e funzionante con `Tab`** | `[OK]` | `<a href="#contenuto-principale" class="salto-contenuto">` testato. |
| **Gerarchia titoli `<h1>` $\rightarrow$ `<h2>` $\rightarrow$ `<h3>`** | `[OK]` | Un solo `<h1>`, nessun salto di livello rilevato. |
| **Tabelle con `<caption>` e `<th scope="...">`** | `[OK]` | Tutte le tabelle dati rispettano lo standard di accessibilità. |
| **Immagini in `img/` in `kebab-case` con `alt`** | `[OK]` | Tutti i file grafici sono minuscoli con descrizione contestuale. |
| **Blocco `<nav>` unificato con gli altri 3 Team** | `[OK]` | Navigazione principale identica su tutte le 5 pagine. |
| **Assenza totale di testo *lorem ipsum*** | `[OK]` | Tutti i testi riguardano dati reali della Città di Feltre. |

---

## 5. Contributi Individuali per Ruolo

- **Scrum Master (`[Cognome]`):**  
  `[Descrivere le attività di coordinamento, gestione Board, risoluzione blocchi e stesura del presente report]`
- **Product Specialist (`[Cognome]`):**  
  `[Elencare le fonti consultate, gli articoli redatti, i dati inseriti nelle tabelle e il coordinamento cross-team su index.html]`
- **QA & Accessibilità (`[Cognome]`):**  
  `[Elencare le PR revisionate, gli errori intercettati prima del merge e i test di accessibilità effettuati]`
- **Core Developer (`[Cognome]`):**  
  `[Elencare le sezioni HTML5 e le regole CSS3 implementate, specificando i commit principali]`

---

## 6. Retrospettiva di Sprint (Sprint Retrospective)

### Cosa ha funzionato bene (Keep Doing)
- `[Punto di forza 1 emerso durante le 8 ore di laboratorio]`
- `[Punto di forza 2]`

### Impedimenti e Criticità Riscontrate (Problems / Blockers)
- `[Difficoltà tecnica, organizzativa o di coordinamento con gli altri team e come è stata affrontata]`

### Azioni di Miglioramento per il Prossimo Sprint (Action Items)
1. `[Azione concreta e verificabile da applicare nel prossimo Sprint]`
2. `[Passaggio di consegne per la rotazione dei ruoli del prossimo Sprint]`

---

**Firma dello Scrum Master:** `___________________________`  
**Visto di convalida del Team:** `___________________________`
