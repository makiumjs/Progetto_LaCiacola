# Pianificazione Didattica & Calendario Sprint (GPOI - Classe 5ITA)

**Testata / Progetto:** La Ciacola di Feltre — Giornale e Portale Turistico-Culturale Cittadino  
**Anno Scolastico:** 2026/2027 (Ottobre 2026 – Fine Marzo 2027)  
**Metodologia:** Scrumban con iterazioni fisse da 4 settimane e limiti WIP (Work In Progress) sulla Board  
**Monte Ore Laboratorio:** 2 ore/settimana (~40 ore complessive: 4 ore Onboarding/Setup + 32 ore su 4 Sprint + 4 ore Collaudo Finale & Presentazione)

---

## 1. Architettura Organizzativa: I 4 Feature Team della 5ITA

| Feature Team | Componenti (14 Studenti) | Pagina HTML | Ambito Tematico e Redazionale |
| :--- | :--- | :--- | :--- |
| **Hub Comune** | **Coordinamento dei 4 Product Specialist** | `index.html` | Prima pagina de *La Ciacola di Feltre*, panoramica territoriale, collegamenti alle 4 redazioni e quadro sinottico. |
| **Team 1** (4 membri) | **Di Dato, De Marzo, Cirillo, Pavan** | `storia.html` | Storia millenaria di Feltre, Cittadella fortificata, Mura Veneziane, Piazza Maggiore e Porte storiche. |
| **Team 2** (4 membri) | **Corso, Xing, Lika, Romaniuk** | `musei.html` | Museo Civico, Galleria d'Arte Moderna "Carlo Rizzarda", Museo Diocesano d'Arte Sacra e Teatro de la Sena. |
| **Team 3** (3 membri) | **Pizzolon, Fongaro, Merlo** | `eventi.html` | Palio di Feltre (Quindici Ducati d'Oro), Mostra dell'Artigianato, Giro delle Mura e Fiera di San Matteo. |
| **Team 4** (3 membri) | **Facchin, Bordin, Romagna** | `mobilita.html` | Stazione ferroviaria, autobus Dolomiti Bus, parcheggi scambiatori, ascensori per il centro storico e numeri utili. |

---

## 2. Matrice Nominativa di Rotazione Obbligatoria dei Ruoli (Sprint 1 – 4)

La rotazione dei 4 ruoli aziendali a ogni Sprint è **tassativa** affinché ogni studente della 5ITA maturi competenze trasversali su coordinamento, contenuti, qualità/WCAG e sviluppo.

### 2.1 Team da 4 Componenti (Team 1 e Team 2 — Rotazione 1:1)

#### Feature Team 1 — Pagina `storia.html`
| Studente | Sprint 1 (Ott - Nov) | Sprint 2 (Nov - Dic) | Sprint 3 (Gen - Feb) | Sprint 4 (Feb - Mar) |
| :--- | :--- | :--- | :--- | :--- |
| **Di Dato** | **Scrum Master** | Core Developer | QA & Accessibilità | Product Specialist |
| **De Marzo** | **Product Specialist** | Scrum Master | Core Developer | QA & Accessibilità |
| **Cirillo** | **QA & Accessibilità** | Product Specialist | Scrum Master | Core Developer |
| **Pavan** | **Core Developer** | QA & Accessibilità | Product Specialist | Scrum Master |

#### Feature Team 2 — Pagina `musei.html`
| Studente | Sprint 1 (Ott - Nov) | Sprint 2 (Nov - Dic) | Sprint 3 (Gen - Feb) | Sprint 4 (Feb - Mar) |
| :--- | :--- | :--- | :--- | :--- |
| **Corso** | **Scrum Master** | Core Developer | QA & Accessibilità | Product Specialist |
| **Xing** | **Product Specialist** | Scrum Master | Core Developer | QA & Accessibilità |
| **Lika** | **QA & Accessibilità** | Product Specialist | Scrum Master | Core Developer |
| **Romaniuk** | **Core Developer** | QA & Accessibilità | Product Specialist | Scrum Master |

---

### 2.2 Team da 3 Componenti (Team 3 e Team 4 — Rotazione Bilanciata su 4 Ruoli)

> **Regola Operativa per i Team da 3 studenti:** In ogni Sprint devono sempre essere presidiati tutti e 4 i ruoli aziendali (con separazione rigorosa tra chi scrive il codice `Core Developer` e chi lo revisiona `QA & Accessibilità`). Uno dei membri abbina quindi il ruolo di **Scrum Master** con quello di **Product Specialist** (oppure a Sprint 4 la redazione contenuti è condivisa), così che ciascuno studente ricopra tutti e 4 i ruoli nell'arco dell'anno.

#### Feature Team 3 — Pagina `eventi.html`
| Studente | Sprint 1 (Ott - Nov) | Sprint 2 (Nov - Dic) | Sprint 3 (Gen - Feb) | Sprint 4 (Feb - Mar) |
| :--- | :--- | :--- | :--- | :--- |
| **Pizzolon** | **Scrum Master** + *Product Specialist* | Core Developer | QA & Accessibilità | **Product Specialist** (Lead Hub) |
| **Fongaro** | **QA & Accessibilità** | **Scrum Master** + *Product Specialist* | Core Developer | **Scrum Master** (Report Finale) |
| **Merlo** | **Core Developer** | QA & Accessibilità | **Scrum Master** + *Product Specialist* | **Core Developer** + *QA Audit* (incrociato con Fongaro) |

#### Feature Team 4 — Pagina `mobilita.html`
| Studente | Sprint 1 (Ott - Nov) | Sprint 2 (Nov - Dic) | Sprint 3 (Gen - Feb) | Sprint 4 (Feb - Mar) |
| :--- | :--- | :--- | :--- | :--- |
| **Facchin** | **Scrum Master** + *Product Specialist* | Core Developer | QA & Accessibilità | **Product Specialist** (Lead Hub) |
| **Bordin** | **QA & Accessibilità** | **Scrum Master** + *Product Specialist* | Core Developer | **Scrum Master** (Report Finale) |
| **Romagna** | **Core Developer** | QA & Accessibilità | **Scrum Master** + *Product Specialist* | **Core Developer** + *QA Audit* (incrociato con Bordin) |

---

## 3. Calendario Dettagliato dei 4 Sprint (Ottobre 2026 – Marzo 2027)

### Fase 0: Kick-off & Onboarding Tecnico (Metà Ottobre 2026 — 4 ore)
- **Settimana 0.1 (2h):** Presentazione del giornale **"La Ciacola di Feltre"** alla LIM, insediamento dei 4 Feature Team, studio di `CONTRIBUTING.md` e `README.md`, clonazione del repository.
- **Settimana 0.2 (2h):** Esercitazione guidata su branch Git, apertura Issue, Pull Request e prima ispezione della pipeline `.github/workflows/w3c-validator.yml`.

---

### Sprint 1: Architettura Semantica & Fondamenta Redazionali (Fine Ottobre – Novembre 2026 — 8 ore)
- **Sprint Goal:** Strutturare lo scheletro HTML5 semantico completo della propria pagina e pubblicare i primi articoli informativi con dati reali verificati.
- **Scrum Master in carica (Redattori Report Sprint 1):** **Di Dato** (Team 1), **Corso** (Team 2), **Pizzolon** (Team 3), **Facchin** (Team 4).
- **Scansione settimanale (8 ore):**
  - *Settimana 1 (2h):* Sprint Planning (30 min), apertura Issue su GitHub Board, raccolta fonti ufficiali (Comune di Feltre, Musei, Associazione Palio, Dolomiti Bus) e progettazione dell'albero semantico.
  - *Settimana 2 (2h):* Implementazione markup HTML5 puro (`<h1>`, `<h2>`, `<h3>`, `<article>`, `<aside>`) senza alcun `<div>` o `<span>`.
  - *Settimana 3 (2h):* Inserimento dello skip-link `<a href="#contenuto-principale" class="salto-contenuto">` e allineamento cross-team del blocco `<nav aria-label="Navigazione principale">`.
  - *Settimana 4 (2h):* Verifica QA, apertura Pull Request, Sprint Review e consegna **Report Sprint 1**.

---

### Sprint 2: Dati Strutturati, Tabelle Accessibili & Fotogiornalismo (Dicembre 2026 – Metà Gennaio 2027 — 8 ore)
- **Sprint Goal:** Arricchire le pagine con tabelle dati pienamente accessibili, liste di definizione (`<dl>`), marcatori temporali/geografici (`<time>`, `<address>`) e asset fotografici ottimizzati.
- **Scrum Master in carica (Redattori Report Sprint 2):** **De Marzo** (Team 1), **Xing** (Team 2), **Fongaro** (Team 3), **Bordin** (Team 4).
- **Scansione settimanale (8 ore):**
  - *Settimana 1 (2h):* Rotazione ruoli, Sprint Planning, progettazione delle tabelle informative (cronologia storica, orari musei, calendario eventi, tariffe parcheggi).
  - *Settimana 2 (2h):* Codifica di `<table>` complete di `<caption>`, `<thead>`, `<tbody>`, `<th scope="col">` e `<th scope="row">`.
  - *Settimana 3 (2h):* Ottimizzazione immagini in `img/` (formato `kebab-case` minuscolo), inserimento in `<figure>` con `<figcaption>` e attributi `alt` descrittivi.
  - *Settimana 4 (2h):* Collaudo W3C Validator, merge delle Pull Request, Sprint Retrospective e consegna **Report Sprint 2**.

---

### Sprint 3: Design System CSS Mobile-First & Impaginazione Editoriale (Metà Gennaio – Febbraio 2027 — 8 ore)
- **Sprint Goal:** Perfezionare l'impaginazione del giornale tramite `css/style.css` sfruttando selettori semantici, CSS Grid/Flexbox applicati ai contenitori semantici (`<main>`, `<section>`, `<article>`) e variabili `:root`.
- **Scrum Master in carica (Redattori Report Sprint 3):** **Cirillo** (Team 1), **Lika** (Team 2), **Merlo** (Team 3), **Romagna** (Team 4).
- **Scansione settimanale (8 ore):**
  - *Settimana 1 (2h):* Rotazione ruoli, analisi UX/UI su schermi mobile (320px+) e desktop, verifica della palette cromatica istituzionale in `:root`.
  - *Settimana 2 (2h):* Sviluppo layout responsive per griglie di `<article>`, tabelle adattive e riquadri `<aside>` senza introdurre `<div>` wrapper.
  - *Settimana 3 (2h):* Ottimizzazione tipografica, stati `:focus-visible` ad alto contrasto e stili di stampa (`@media print`).
  - *Settimana 4 (2h):* Test cross-browser, Code Review incrociata, merge PR e consegna **Report Sprint 3**.

---

### Sprint 4: Audit WCAG 2.1 AA+, Prima Pagina (`index.html`) & Rilascio Finale (Fine Febbraio – Fine Marzo 2027 — 8 ore)
- **Sprint Goal:** Completare l'integrazione editoriale di `index.html`, eseguire l'audit completo di accessibilità da tastiera e screen reader e pubblicare il numero finale de **La Ciacola di Feltre** su GitHub Pages.
- **Scrum Master in carica (Redattori Report Sprint 4):** **Pavan** (Team 1), **Romaniuk** (Team 2), **Fongaro** (Team 3), **Bordin** (Team 4).
- **Scansione settimanale (8 ore):**
  - *Settimana 1 (2h):* Ultima rotazione ruoli, revisione congiunta di `index.html` affinché valorizzi gli articoli di tutti i 4 Feature Team.
  - *Settimana 2 (2h):* Audit di accessibilità: navigazione esclusiva con tasto `Tab`/`Shift+Tab`, verifica contrasto $\ge 4.5:1$, controllo link interni/esterni.
  - *Settimana 3 (2h):* Risoluzione bug residui (Bug Bash), verifica verde su GitHub Actions e congelamento del codice (*Code Freeze*).
  - *Settimana 4 (2h):* Consegna **Report Sprint 4**, pubblicazione su GitHub Pages e presentazione finale del giornale alla classe e al docente.
