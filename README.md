# La Ciacola di Feltre — Giornale e Portale Turistico-Culturale Cittadino

**Istituto Tecnico Industriale Statale (ITIS) — Indirizzo Informatica**  
**Classe:** 5ITA (14 studenti divisi in 4 Feature Team) — **Materia:** GPOI (Gestione Progetto e Organizzazione d'Impresa)  
**Anno Scolastico:** 2026/2027 (Termine progetto: Fine Marzo 2027)  
**Repository GitHub:** [https://github.com/makiumjs/Progetto_LaCiaccola](https://github.com/makiumjs/Progetto_LaCiaccola)  
**Demo Live (GitHub Pages):** [https://makiumjs.github.io/Progetto_LaCiaccola/](https://makiumjs.github.io/Progetto_LaCiaccola/)

---

## 1. Descrizione del Progetto

**"La Ciacola di Feltre"** è il giornale civico e portale turistico-culturale della Città di Feltre e del Parco Nazionale Dolomiti Bellunesi, sviluppato in laboratorio dalla classe **5ITA** seguendo la metodologia agile **Scrumban**.

Il portale raccoglie inchieste storiche, guide museali, speciali sul Palio e informazioni logistiche sul territorio feltrino, rispettando standard ingegneristici rigorosi:
- **HTML5 Semantico Puro al 100%:** divieto assoluto di utilizzo dei tag non semantici `<div>` e `<span>`.
- **Accessibilità Universale WCAG 2.1 Livello AA+:** navigazione completa da tastiera con *skip-link*, gerarchia dei titoli rigorosa (`<h1>` $\rightarrow$ `<h2>` $\rightarrow$ `<h3>`), tabelle dati accessibili agli screen reader e contrasto cromatico verificato $\ge 4.5:1$.
- **Design Mobile-First:** foglio di stile unico basato su *CSS Custom Properties* (`:root`) e layout adattivo costruito direttamente sui contenitori semantici.

---

## 2. Organizzazione dei 4 Feature Team e Pagine Assegnate

Il monte ore complessivo (~40 ore di laboratorio, 2 ore a settimana) è articolato in **4 Sprint da 4 settimane ciascuno** (8 ore per Sprint). La classe 5ITA è suddivisa in **4 Feature Team** che collaborano sull'Hub comune (`index.html`) e sono responsabili ciascuno di una pagina tematica:

| Feature Team | Componenti (Classe 5ITA) | File HTML | Ambito Redazionale | Contenuti Principali |
| :--- | :--- | :--- | :--- | :--- |
| **Hub Comune** | **Tutti i 4 Team (Coordinamento Product Specialist)** | [`index.html`](index.html) | **Prima Pagina & Raccordo** | Editoriale sulla Città di Feltre, vetrina delle 4 redazioni, quadro sinottico e colophon IAT Feltre. |
| **Team 1** (4 studenti) | **Di Dato, De Marzo, Cirillo, Pavan** | [`storia.html`](storia.html) | **Storia & Borgo Medievale** | Origini retiche e romane (*Feltria*), Cittadella fortificata, Mura Veneziane, Piazza Maggiore, Castello di Alboino e Porte storiche. |
| **Team 2** (4 studenti) | **Corso, Xing, Lika, Romaniuk** | [`musei.html`](musei.html) | **Musei, Gallerie & Teatro** | Museo Civico, Galleria d'Arte Moderna "Carlo Rizzarda", Museo Diocesano d'Arte Sacra, Teatro de la Sena, orari e tariffe. |
| **Team 3** (3 studenti) | **Pizzolon, Fongaro, Merlo** | [`eventi.html`](eventi.html) | **Eventi, Palio & Tradizioni** | Palio di Feltre (Quindici Ducati d'Oro), Mostra dell'Artigianato Artistico, Giro delle Mura in notturna e Antica Fiera di San Matteo. |
| **Team 4** (3 studenti) | **Facchin, Bordin, Romagna** | [`mobilita.html`](mobilita.html) | **Trasporti, Parcheggi & Servizi** | Stazione FS (linea Padova-Calalzo), autolinee Dolomiti Bus, parcheggi di attestamento, ascensori accessibili e numeri utili. |

---

## 3. Rotazione Obbligatoria dei Ruoli Aziendali (Sprint 1 – Sprint 4)

A ogni Sprint (ogni 4 settimane), i componenti di ciascun Feature Team ruotano obbligatoriamente nei **4 ruoli aziendali**:
1. **Scrum Master (SM):** coordina il team, gestisce i limiti WIP sulla Board Scrumban e redige il Report di fine Sprint valutato dal docente (voto 1–10).
2. **Product Specialist (PS):** cura la ricerca storica e giornalistica, garantisce l'assenza di testo fittizio (*lorem ipsum*) e mantiene la coerenza editoriale cross-team.
3. **QA & Accessibilità (QA):** presidia la qualità tramite Code Review sulle Pull Request, verifica il rispetto delle WCAG 2.1 AA+ e accerta il superamento della pipeline W3C.
4. **Core Developer (DEV):** sviluppa il markup HTML5 semantico puro e il foglio di stile CSS3 nei branch dedicati alle singole *User Story*.

> **Nota Architetturale per i Team da 3 componenti (Team 3 e Team 4):** Poiché i ruoli aziendali sono 4 e i membri sono 3, in ogni Sprint i 3 studenti ricoprono **un ruolo primario individuale** mentre il quarto ruolo (**Product Specialist** o **Scrum Master**) viene associato a rotazione a uno dei membri, garantendo che nell'arco dei 4 Sprint tutti sperimentino tutti i profili professionali senza lasciare scoperta alcuna responsabilità.

Consultare la matrice nominativa completa Sprint per Sprint in [`docs/pianificazione-sprint.md`](docs/pianificazione-sprint.md).

---

## 4. Alberatura del Repository

```text
Progetto_LaCiaccola/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── user_story.md             # Template per l'assegnazione attività ai Feature Team
│   ├── workflows/
│   │   └── w3c-validator.yml         # Pipeline CI: validazione W3C Nu Html Checker + grep anti-div/anti-span
│   └── PULL_REQUEST_TEMPLATE.md      # Template PR con checklist Definition of Done
├── docs/                             # Documentazione didattica GPOI
│   ├── pianificazione-sprint.md      # Calendario 4 Sprint e matrice nominativa ruoli 5ITA
│   ├── rubrica-valutazione-gpoi.md   # Griglia di valutazione docente (scala 1 - 10 con pesi)
│   ├── guida-onboarding-studenti.md  # Guida prima lezione da proiettare alla LIM
│   └── templates/
│       └── template-report-sprint.md # Modello report periodico (ogni 4 settimane)
├── img/                              # Asset grafici ottimizzati in formato kebab-case minuscolo
│   ├── placeholder.jpg
│   ├── panorama-cittadella-feltre.jpg
│   ├── mura-veneziane-feltre.jpg
│   ├── museo-civico-facciata.jpg
│   ├── palio-di-feltre-piazza.jpg
│   └── stazione-feltre-mobilita.jpg
├── css/                              # Foglio di stile starter mobile-first
│   └── style.css                     # Custom properties :root, reset moderno, layout semantico
├── index.html                        # Homepage comune ("La Ciacola di Feltre")
├── storia.html                       # Team 1 (Di Dato, De Marzo, Cirillo, Pavan)
├── musei.html                        # Team 2 (Corso, Xing, Lika, Romaniuk)
├── eventi.html                       # Team 3 (Pizzolon, Fongaro, Merlo)
├── mobilita.html                     # Team 4 (Facchin, Bordin, Romagna)
├── README.md                         # Presentazione classe 5ITA, tabella team, link Pages
└── CONTRIBUTING.md                   # Flusso Git branch, convenzioni commit e Definition of Done
```

---

## 5. Collaudo Locale Rapido

Per verificare in locale il rispetto dei vincoli architetturali prima di aprire una Pull Request:

```bash
# 1. Verifica assenza di tag <div> e <span> (deve restituire 0 occorrenze)
grep -rn -i -E "<(div|span)([[:space:]>]|$)" . --include="*.html"

# 2. Avvio server statico locale per testare navigazione e accessibilità da tastiera
python3 -m http.server 8000
```
