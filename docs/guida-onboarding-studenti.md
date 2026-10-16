# Guida di Onboarding Studenti (Da Proiettare alla LIM — Lezione 1)

**Benvenuti nella Redazione Tecnica della classe 5ITA!**  
Da oggi fino a **fine marzo 2027** lavoreremo come una vera redazione digitale e *Software House* organizzata in **4 Feature Team** per realizzare **"La Ciacola di Feltre"** — il giornale e portale turistico-culturale della Città di Feltre.

---

## 1. Le 4 Redazioni (Feature Team) e le Pagine Assegnate

| Feature Team | Componenti del Team | Pagina di Responsabilità | Tema della Sezione |
| :--- | :--- | :--- | :--- |
| **Team 1** | **Di Dato, De Marzo, Cirillo, Pavan** | [`storia.html`](../storia.html) | Storia, borgo medievale, Cittadella e Mura Veneziane |
| **Team 2** | **Corso, Xing, Lika, Romaniuk** | [`musei.html`](../musei.html) | Musei civici, Galleria Rizzarda, Diocesano e Teatro de la Sena |
| **Team 3** | **Pizzolon, Fongaro, Merlo** | [`eventi.html`](../eventi.html) | Palio di Feltre, Mostra dell'Artigianato, Giro delle Mura e Fiere |
| **Team 4** | **Facchin, Bordin, Romagna** | [`mobilita.html`](../mobilita.html) | Trasporti, parcheggi, ascensori accessibili e numeri utili |
| **Hub Comune** | **Tutti i Team (Product Specialist)** | [`index.html`](../index.html) | Prima pagina del giornale e raccordo di navigazione |

---

## 2. Chi fa cosa nello Sprint 1 (Ottobre – Novembre 2026)?

Ecco i ruoli ufficiali per le prime **4 settimane (8 ore di laboratorio)**:

| Feature Team | Scrum Master (Coordina + Report) | Product Specialist (Contenuti) | QA & Accessibilità (W3C + WCAG) | Core Developer (HTML5 + CSS3) |
| :--- | :--- | :--- | :--- | :--- |
| **Team 1 (`storia.html`)** | **Di Dato** | **De Marzo** | **Cirillo** | **Pavan** |
| **Team 2 (`musei.html`)** | **Corso** | **Xing** | **Lika** | **Romaniuk** |
| **Team 3 (`eventi.html`)** | **Pizzolon** | **Pizzolon** *(con supporto team)* | **Fongaro** | **Merlo** |
| **Team 4 (`mobilita.html`)** | **Facchin** | **Facchin** *(con supporto team)* | **Bordin** | **Romagna** |

*(Al termine della 4ª settimana si consegna il Report valutato da 1 a 10 e i ruoli ruotano secondo la tabella in `docs/pianificazione-sprint.md`)*.

---

## 3. I 4 Comandamenti Architetturali (Definition of Done)

> **ATTENZIONE:** La pipeline automatica di GitHub bloccherà qualsiasi Pull Request che violi anche una sola di queste regole!

1. **ZERO `<div>` e ZERO `<span>`:**
   - È tassativamente vietato usare `<div>` e `<span>`.
   - Usate esclusivamente i tag HTML5 semantici: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<time>`, `<address>`, `<table>`, `<dl>`.
2. **Accessibilità WCAG 2.1 AA+ Obbligatoria:**
   - Ogni pagina inizia con lo skip-link: `<a href="#contenuto-principale" class="salto-contenuto">Salta al contenuto principale</a>`.
   - Esattamente **un solo `<h1>`** per pagina, seguito da `<h2>` e `<h3>` **senza salti** (mai passare da `<h1>` a `<h3>`!).
   - Ogni immagine deve avere un attributo `alt="..."` chiaro e descrittivo.
   - Ogni tabella (`<table>`) deve avere `<caption>`, `<thead>`, `<tbody>` e `<th scope="col">` (o `scope="row"`).
3. **Barra di Navigazione Unificata:**
   - Tutte le 5 pagine devono condividere il medesimo blocco `<nav aria-label="Navigazione principale">`.
4. **Nomi Immagini e Contenuti Reali:**
   - Nella cartella `img/` solo file con lettere minuscole e trattini (`kebab-case`), es. `museo-civico-facciata.jpg`.
   - **Vietato il *lorem ipsum*:** scriviamo solo articoli e dati reali sulla città di Feltre.

---

## 4. Operatività Pratica: Cosa Fare nei Primi 30 Minuti Oggi

### Passo 1 — Clonare il Repository e Creare il Branch del Team
Il **Core Developer** di ciascun team (nello Sprint 1: **Pavan, Romaniuk, Merlo, Romagna**) apre il terminale ed esegue:

```bash
git clone <URL_DEL_REPOSITORY>
cd Progetto_LaCiaccola
git checkout -b sprint1/team1-storia
```
*(Sostituite `team1-storia` con la sigla del vostro team: `team2-musei`, `team3-eventi`, `team4-mobilita`)*.

### Passo 2 — Controllare la propria Pagina nel Terminale
Il responsabile **QA & Accessibilità** (nello Sprint 1: **Cirillo, Lika, Fongaro, Bordin**) verifica che i controlli locali passino senza errori:

```bash
# Verifica assenza di <div> o <span> nei file HTML (non deve stampare nulla)
grep -rn -i -E "<(div|span)([[:space:]>]|$)" . --include="*.html"
```

### Passo 3 — Compilare le prime Issue sulla Board Scrumban
1. Lo **Scrum Master** e il **Product Specialist** aprono la scheda **Issues** su GitHub.
2. Cliccano su **New Issue** $\rightarrow$ **User Story (Feature Team)**.
3. Creano le prime 3–4 attività dello Sprint 1 e le spostano nella colonna **To Do / Ready** della Board.
