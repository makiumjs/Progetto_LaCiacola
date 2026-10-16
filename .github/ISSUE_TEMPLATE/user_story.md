---
name: "User Story (Feature Team)"
about: "Template standard per l'assegnazione di attività ai Feature Team della classe 5ITA"
title: "[Sprint X - Team Y] Titolo sintetico della User Story"
labels: ["user-story", "scrumban"]
assignees: []
---

## 1. Descrizione della User Story

**Come** `[tipologia di utente: es. turista, cittadino, studente, visitatore con disabilità visiva]`
**Voglio** `[azione o contenuto desiderato all'interno della pagina]`
**Affinché** `[valore aggiunto o beneficio concreto ottenuto]`

---

## 2. Dettagli di Assegnazione (Scrumban)

- **Sprint di riferimento:** `[Sprint 1 / Sprint 2 / Sprint 3 / Sprint 4]`
- **Feature Team assegnatario:** `[Team 1 - Storia / Team 2 - Musei / Team 3 - Eventi / Team 4 - Mobilità / Cross-Team]`
- **Pagina HTML coinvolta:** `[index.html / storia.html / musei.html / eventi.html / mobilita.html]`
- **Ruoli del Team in questo Sprint:**
  - **Scrum Master:** `@username`
  - **Product Specialist:** `@username`
  - **QA & Accessibilità:** `@username`
  - **Core Developer:** `@username`

---

## 3. Criteri di Accettazione Funzionali

- [ ] Contenuto testuale reale, accurato e coerente con il territorio di Feltre e delle Dolomiti Bellunesi (zero testo segnaposto o *lorem ipsum*).
- [ ] Struttura informativa completa di dati verificabili (orari, indirizzi in `<address>`, date in `<time>`, oppure tabelle con `<caption>` e `<th scope="...">`).
- [ ] Eventuali immagini inserite nella cartella `img/` con nomenclatura rigorosamente `kebab-case` minuscola e attributo `alt` descrittivo.

---

## 4. Definition of Done (Vincoli Architetturali Obbligatori)

- [ ] **HTML5 Semantico Puro:** zero tag `<div>` e zero tag `<span>` nel file modificato.
- [ ] **Accessibilità WCAG 2.1 AA+:**
  - [ ] Presenza dello skip-link `<a href="#contenuto-principale" class="salto-contenuto">` come primo elemento di `<body>`.
  - [ ] Gerarchia dei titoli rigorosa: un solo `<h1>` per pagina, seguito da `<h2>` e `<h3>` senza salti di livello.
  - [ ] Contrasto cromatico verificato $\ge 4.5:1$ e stato `:focus-visible` ben distinguibile da tastiera.
- [ ] **Navigazione Unificata:** blocco `<nav aria-label="Navigazione principale">` identico e coerente con le altre pagine del portale.
- [ ] **Validazione Automatica:** superamento completo dei controlli nella pipeline CI (`.github/workflows/w3c-validator.yml`).
