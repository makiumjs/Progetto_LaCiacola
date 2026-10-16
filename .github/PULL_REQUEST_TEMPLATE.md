## Descrizione della Pull Request

- **Sprint:** `[Sprint 1 / Sprint 2 / Sprint 3 / Sprint 4]`
- **Feature Team:** `[Team 1 - Storia / Team 2 - Musei / Team 3 - Eventi / Team 4 - Mobilità]`
- **Issue collegata:** Closes `#numero_issue`
- **File modificati:** `[es. storia.html, css/style.css]`

### Riepilogo delle modifiche
Descrivi brevemente i contenuti inseriti o le migliorie strutturali/stilistiche apportate in questa Pull Request:
- 
- 

---

## Ruoli e Firme di Revisione (Rotazione Sprint)

- **Core Developer (Autore implementazione):** `@username`
- **Product Specialist (Verifica contenuti e coerenza editoriale):** `@username`
- **QA & Accessibilità (Revisione codice, WCAG e validazione W3C):** `@username`
- **Scrum Master (Coordinamento e verifica finale per il Report):** `@username`

---

## Checklist Definition of Done (Obbligatoria prima del Merge)

### 1. Architettura HTML5 Semantico Puro
- [ ] **Zero `<div>` e Zero `<span>`:** ho verificato che nessun file HTML contenga i tag vietati `<div>` o `<span>`.
- [ ] **Tag Semantici Appropriati:** sono stati usati esclusivamente tag dotati di valore semantico (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<time>`, `<address>`, `<table>`, `<dl>`).
- [ ] **Tabelle Accessibili (se presenti):** ogni `<table>` include obbligatoriamente `<caption>`, `<thead>`, `<tbody>` e intestazioni `<th scope="col">` o `<th scope="row">`.

### 2. Accessibilità (WCAG 2.1 Livello AA+)
- [ ] **Skip-link funzionante:** è presente `<a href="#contenuto-principale" class="salto-contenuto">` in cima al `<body>` e `<main id="contenuto-principale">`.
- [ ] **Gerarchia Titoli:** esiste un unico `<h1>` nella pagina e i sottotitoli seguono l'ordine logico `<h2>` $\rightarrow$ `<h3>` senza alcun salto di livello.
- [ ] **Immagini Accessibili:** ogni `<img>` possiede un attributo `alt` contestualizzato e descrittivo (mai vuoto per immagini informative).
- [ ] **Navigazione da Tastiera e Contrasto:** tutti gli elementi interattivi sono raggiungibili con `Tab`, mostrano il focus ad alto contrasto e rispettano il rapporto minimo $4.5:1$.

### 3. Coerenza Cross-Team e Asset
- [ ] **Navigazione Globale Unificata:** il blocco `<nav aria-label="Navigazione principale">` è allineato con tutte le 5 pagine del portale.
- [ ] **Nomenclatura Asset:** tutti i file in `img/` utilizzano solo lettere minuscole e formato `kebab-case` (es. `museo-civico-facciata.jpg`).
- [ ] **Contenuti Reali:** assenza totale di testo fittizio (*lorem ipsum*).
- [ ] **Pipeline CI Verde:** l'azione GitHub `w3c-validator.yml` è stata eseguita con esito positivo.
