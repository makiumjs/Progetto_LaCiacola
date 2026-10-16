# Rubrica di Valutazione GPOI — Progetto Portale Feltre (Scala 1–10)

**Destinatari:** Classe 5ITA — Indirizzo Informatica  
**Materia:** Gestione Progetto e Organizzazione d'Impresa (GPOI)  
**Cadenza di Valutazione:** Al termine di ogni Sprint (ogni 4 settimane, per un totale di 4 valutazioni formali).

---

## 1. Pesi Percentuali dei Criteri di Valutazione

Il voto complessivo di ciascuno Sprint (espresso in decimi, da **1 a 10**) è calcolato come media ponderata di **5 dimensioni progettuali**:

| # | Dimensione Valutata | Peso (%) | Punteggio Max | Ruolo Primario Coinvolto |
| :-: | :--- | :-: | :-: | :--- |
| **1** | **Gestione Progetto, Board Scrumban & Report di Sprint** | **25%** | 2,5 punti | Scrum Master (+ tutto il Team) |
| **2** | **Architettura HTML5 Semantico Puro (Zero `div`/`span`)** | **25%** | 2,5 punti | Core Developer |
| **3** | **Accessibilità WCAG 2.1 AA+ & Validazione W3C** | **20%** | 2,0 punti | QA & Accessibilità |
| **4** | **Qualità Contenuti, Coerenza Cross-Team & Usabilità** | **15%** | 1,5 punti | Product Specialist |
| **5** | **Flusso Git, Pull Request, Commits & Collaborazione** | **15%** | 1,5 punti | Tutti i membri del Team |
| | **TOTALE** | **100%** | **10,0 punti** | |

> **Nota sulla responsabilità individuale e di gruppo:** Il voto di Sprint è composto per il **70%** dal risultato collettivo del Feature Team e per il **30%** dalla qualità dell'esecuzione del ruolo specifico ricoperto dallo studente nello Sprint corrente (verificabile tramite cronologia Git, Issue, revisioni PR e Report).

---

## 2. Griglia Descrittiva Analitica per Livelli (Scala 1–10)

| Criterio (Peso) | Insufficiente Gr. (1 – 3) | Insufficiente (4 – 5) | Sufficiente (6) | Discreto / Buono (7 – 8) | Ottimo / Eccellente (9 – 10) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Gestione Scrumban & Report (25%)** | Report non consegnato o privo di dati; Board assente o mai aggiornata. | Report incompleto o consegnato in ritardo; metriche di Sprint assenti; limiti WIP ignorati. | Report consegnato nei tempi con le sezioni minime; Board aggiornata solo a fine Sprint. | Report chiaro con metriche di avanzamento, impedimenti e retrospettiva; Board allineata alle PR. | Report di livello aziendale con analisi puntuale di velocity, rischi, metriche PR/Issue e piano di miglioramento continuo. |
| **2. HTML5 Semantico Puro (25%)** | Uso diffuso di `<div>` e `<span>`; struttura semantica inesistente. | Presenza residua di `<div>`/`<span>`; uso improprio dei tag semantici (`<section>` senza titolo). | Zero `<div>`/`<span>`; struttura base (`<header>`, `<main>`, `<footer>`) presente e corretta. | Uso appropriato di `<article>`, `<section>`, `<aside>`, `<figure>`, `<time>`, `<address>` e `<dl>`. | Semantica impeccabile; tabelle complete di `<caption>` e `<th scope="...">`; markup pulito, manutenibile e auto-documentante. |
| **3. Accessibilità WCAG 2.1 AA+ & W3C (20%)** | Pipeline CI fallita; numerosi errori W3C; assenza di `alt` e skip-link. | Errori W3C minori non corretti; salti nella gerarchia titoli (`h1` $\rightarrow$ `h3`); contrasto insufficiente. | Validazione W3C superata; un solo `<h1>`, gerarchia `h1`–`h3` rispettata e skip-link presente. | Attributi `alt` ricchi di contesto, focus da tastiera ben visibile, contrasto $\ge 4.5:1$ verificato. | Accessibilità esemplare testata da tastiera; uso accurato di `aria-label` e `aria-current="page"`; zero warning W3C. |
| **4. Contenuti & Coerenza Cross-Team (15%)** | Presenza di *lorem ipsum* o testo copiato senza struttura; `<nav>` difforme dagli altri team. | Contenuti scarni o imprecisi; asset in `img/` con nomi non conformi (spazi o maiuscole). | Contenuti reali sul tema di Feltre; `<nav>` unificata corretta; file in `img/` in `kebab-case`. | Contenuti ben organizzati, dati reali (orari, indirizzi, prezzi), ottima leggibilità mobile-first. | Ricerca storica/tecnica approfondita, perfetta integrazione con `index.html`, micro-copy chiaro e orientato al cittadino/turista. |
| **5. Flusso Git & Collaborazione (15%)** | Commit diretti su `main`; un solo studente ha effettuato tutti i commit del gruppo. | Branch disordinati; PR unite senza revisione o senza compilare il template DoD. | Uso di branch dedicati e PR verso `main`; partecipazione minima registrata da tutti i membri. | Messaggi di commit convenzionali e chiari; PR revisionate dal QA con checklist DoD spuntata. | Flusso Git rigoroso: Issue atomiche collegate alle PR, Code Review costruttive con commenti sul codice e contributi bilanciati. |

---

## 3. Penalità Automatiche (Regole di Sbarramento Architetturale)

Per simulare gli standard reali di un reparto di ingegneria del software, si applicano le seguenti decurtazioni oggettive in sede di consegna dello Sprint:

1. **Violazione Tassativa Anti-`<div>` / Anti-`<span>`:** **$-1,5$ punti** per ogni file HTML del team che contenga anche un solo tag `<div>` o `<span>` al momento della chiusura dello Sprint.
2. **Commit Diretto su `main` (Bypass PR):** **$-1,0$ punto** per modifiche spinte direttamente sul branch principale senza Pull Request e approvazione del QA.
3. **Presenza di *Lorem Ipsum*:** **$-1,0$ punto** per la presenza di testo fittizio non sostituito da contenuti reali.
4. **Consegna Tardiva del Report di Sprint:** **$-0,5$ punti** per ogni giorno scolastico di ritardo rispetto alla scadenza della 4ª settimana.

---

## 4. Scheda Sintetica di Calcolo del Voto (Ad uso del Docente)

```text
Feature Team: ___________________   Sprint N.: [ 1 | 2 | 3 | 4 ]   Data: ___/___/202_

[A] Gestione Scrumban & Report (max 2,5 pt):          _____ / 2,5
[B] HTML5 Semantico Puro (max 2,5 pt):                _____ / 2,5
[C] Accessibilità WCAG 2.1 AA+ & W3C (max 2,0 pt):    _____ / 2,0
[D] Contenuti, Coerenza & Asset (max 1,5 pt):         _____ / 1,5
[E] Flusso Git, PR & Collaborazione (max 1,5 pt):     _____ / 1,5
-----------------------------------------------------------------
SUBTOTALE TEAM (A + B + C + D + E):                   _____ / 10,0
Eventuali Penalità Automatiche:                     - _____
VOTO BASE TEAM:                                       _____ / 10,0

Valutazione Individuale (70% Base Team + 30% Esecuzione Ruolo):
- Scrum Master (______________________): Voto Finale = _____ / 10
- Product Specialist (________________): Voto Finale = _____ / 10
- QA & Accessibilità (________________): Voto Finale = _____ / 10
- Core Developer (____________________): Voto Finale = _____ / 10
```
