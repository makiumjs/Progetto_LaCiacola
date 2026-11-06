# 🚀 Guida Operativa Settimana 2 & Consegna Finale Sprint 1 (Voto 1–10)

**Progetto:** La Ciacola di Feltre (`makiumjs/Progetto_LaCiacola`)  
**Classe:** 5ITA — **Materia:** GPOI  
**Docente:** Prof. Cassarino  
**Scadenza Consegna Sprint 1 (a casa):** Entro l'inizio della prossima lezione di laboratorio

---

## 🛠️ Parte 1 — Attività di Oggi in Laboratorio (Sprint 1 • Settimana 2)

Oggi si passa dalla progettazione su carta/file di testo alla **codifica vera e propria su branch Git dedicati**.

> **REGOLA TASSATIVA:** È vietato fare commit o push sul branch `main`. Chi lavora su `main` riceverà un errore di blocco da GitHub e una penalità di **$-1,0$ punto** sul voto di Sprint.

### Passo 1 — Sincronizzazione e Creazione del Branch del Team *(Core Developer)*
Il **Core Developer** (e poi i compagni di team) apre il terminale in VS Code ed esegue:

```bash
# 1. Posizionarsi su main e scaricare gli ultimi aggiornamenti del docente
git checkout main
git pull origin main

# 2. Creare e spostarsi sul branch del proprio Feature Team (SCEGLIERE IL PROPRIO):
git checkout -b sprint1/team1-storia     # Solo Team 1 (Di Dato, De Marzo, Cirillo, Pavan)
git checkout -b sprint1/team2-musei      # Solo Team 2 (Corso, Xing, Lika, Romaniuk)
git checkout -b sprint1/team3-eventi     # Solo Team 3 (Pizzolon, Fongaro, Merlo)
git checkout -b sprint1/team4-mobilita   # Solo Team 4 (Facchin, Bordin, Romagna)
```

*(Quando il primo membro ha fatto `git push -u origin sprint1/teamX-...`, gli altri compagni dello stesso gruppo possono scaricare il branch con `git fetch --all` seguito da `git checkout sprint1/teamX-...`).*

### Passo 2 — Implementazione HTML5 Semantico Puro *(Core Developer + Product Specialist)*
Trasformate i contenuti preparati in `bozza-<tema>.txt` e la struttura di `albero-<tema>.md` dentro il file `.html` del vostro Team (`storia.html`, `musei.html`, `eventi.html`, `mobilita.html`):
- Usate **esclusivamente** tag semantici: `<header>`, `<nav>`, `<main id="contenuto-principale">`, `<section>`, `<article>`, `<aside>`, `<figure>`, `<figcaption>`, `<table>`, `<dl>`, `<dt>`, `<dd>`, `<time datetime="...">`, `<address>`, `<footer>`.
- **ZERO `<div>` e ZERO `<span>`**.
- **ZERO *lorem ipsum***: solo dati reali, verificati e completi sulla Città di Feltre.

### Passo 3 — Collaudo Locale in Terminale *(QA & Accessibilità)*
Prima di fare commit e push, il responsabile **QA & Accessibilità** esegue nel terminale:

```bash
# 1. Verifica assenza di <div> e <span> (NON deve stampare nessuna riga!)
grep -rn -i -E "<(div|span)([[:space:]>]|$)" . --include="*.html"

# 2. Avvia il server web locale per testare la pagina su http://localhost:8000
python3 -m http.server 8000
```

---

## 🏠 Parte 2 — Compiti per Casa (Completamento e Chiusura dello Sprint 1)

Entro la prossima settimana, ogni Feature Team deve completare a casa i **4 passaggi seguenti** per chiudere ufficialmente lo **Sprint 1** ed essere valutato (voto da 1 a 10).

### 1. Rifinitura Accessibilità WCAG 2.1 AA+ e Commit di Tutti i Membri
1. **Skip-link funzionante:** verificare che il primo elemento dentro `<body>` sia:
   ```html
   <a href="#contenuto-principale" class="salto-contenuto">Salta al contenuto principale</a>
   ```
   e che il tag `<main>` abbia `id="contenuto-principale"`.
2. **Barra di navigazione `<nav>` identica su tutte le pagine:** verificare che il blocco `<nav aria-label="Navigazione principale">` sia allineato a `index.html` e abbia `aria-current="page"` sul link della propria pagina.
3. **Gerarchia dei titoli senza salti:** un solo `<h1>` per pagina, seguito da `<h2>` per le `<section>` e `<aside>`, e `<h3>` per gli `<article>`.
4. **Tabella accessibile:** verificare che la `<table>` contenga `<caption>`, `<thead>`, `<tbody>`, `<th scope="col">` e `<th scope="row">`.
5. **Partecipazione su Git:** sia il **Core Developer** sia il **Product Specialist** (e il resto del team) devono aver effettuato **almeno un commit a proprio nome** sul branch del team usando il formato *Conventional Commits* (es. `feat(storia): ...`, `a11y(storia): ...`, `docs(storia): ...`).

---

### 2. Redazione del Report Ufficiale di Fine Sprint 1 (`docs/report-sprint1-teamX.md`)
Lo **Scrum Master**, insieme a tutto il gruppo, deve copiare il modello [`docs/templates/template-report-sprint.md`](templates/template-report-sprint.md) e creare nella cartella `docs/` il file del proprio Team:
- **Team 1 (Di Dato):** `docs/report-sprint1-team1.md`
- **Team 2 (Corso):** `docs/report-sprint1-team2.md`
- **Team 3 (Pizzolon):** `docs/report-sprint1-team3.md`
- **Team 4 (Facchin):** `docs/report-sprint1-team4.md`

Il Report va compilato in **tutte le 6 sezioni** (tabella ruoli con `@username`, Sprint Goal, tabella delle 3 Issue con link alle PR, tabella Audit QA con gli `[OK]`, contributi individuali e retrospettiva) e **aggiunto al branch prima di chiudere la Pull Request**:

```bash
git add docs/report-sprint1-teamX.md
git commit -m "docs(docs): consegna report finale Sprint 1 Team X"
git push
```

---

### 3. Apertura della Pull Request e Revisione del QA
1. Andate su **[Pull requests](https://github.com/makiumjs/Progetto_LaCiacola/pulls)** $\rightarrow$ cliccate **Compare & pull request** sul branch `sprint1/teamX-...` verso `main`.
2. Compilate integralmente il template della Pull Request spuntando le caselle `[x]` e indicando i numeri delle 3 Issue del vostro Team (es. `Closes #6, Closes #7, Closes #8`).
3. Controllate che il controllo automatico **W3C & Semantic HTML5 Validator** diventi **Verde ✅** (se diventa rosso ❌, cliccate su *Details*, leggete l'errore W3C o il `<div>` trovato, correggetelo in VS Code e rifate `git commit` + `git push`).
4. Il compagno **QA & Accessibilità** (**Cirillo, Lika, Fongaro, Bordin**) entra nella Pull Request e scrive un commento formale di revisione certificando il superamento dei controlli WCAG 2.1 AA+.

---

### 4. Approvazione dello Scrum Master (`CODEOWNERS`), Merge e Chiusura Board
Grazie al file `.github/CODEOWNERS`, **nessuna Pull Request può essere unita su `main` senza il permesso dello Scrum Master del Team**:
1. Lo **Scrum Master** (**Di Dato, Corso, Pizzolon, Facchin**) apre la Pull Request del proprio Team $\rightarrow$ clicca sulla scheda **`Files changed`** $\rightarrow$ clicca il pulsante verde **`Review changes`** $\rightarrow$ seleziona **`Approve`** $\rightarrow$ **`Submit review`**.
2. Una volta sbloccato il pulsante, clicca **`Merge pull request`** $\rightarrow$ **`Confirm merge`**.
3. Infine apre la **[Board Scrumban 5ITA](https://github.com/users/makiumjs/projects/3/views/1)** e verifica che tutte le **3 Issue del proprio Team** siano nella colonna **`Done`**.

---

## 🎯 Parte 3 — Come Verrete Valutati Settimana Prossima (Voto 1–10)

La prossima settimana in laboratorio il docente valuterà il lavoro di ciascun Feature Team e di ogni singolo studente applicando la **[Rubrica di Valutazione GPOI](rubrica-valutazione-gpoi.md)**:

| # | Criterio di Valutazione | Peso | Punti Max | Cosa Viene Controllato dal Docente | Ruolo Valutato (30% Individuale) |
| :-: | :--- | :-: | :-: | :--- | :--- |
| **1** | **Board Scrumban & Report Sprint 1** | **25%** | **2,5 pt** | 3 Issue ben scritte e spostate in `Done` sulla Board + file `docs/report-sprint1-teamX.md` completo in ogni sezione. | **Scrum Master** *(Di Dato, Corso, Pizzolon, Facchin)* |
| **2** | **HTML5 Semantico Puro** | **25%** | **2,5 pt** | Struttura impeccabile con `<section>`, `<article>`, `<aside>`, `<table>`, `<dl>`, `<time>`, `<address>` e zero `<div>`/`<span>`. | **Core Developer** *(Pavan, Romaniuk, Merlo, Romagna)* |
| **3** | **Accessibilità WCAG 2.1 AA+ & W3C** | **20%** | **2,0 pt** | Pipeline GitHub Actions verde ✅, skip-link funzionante, gerarchia `<h1>`→`<h2>`→`<h3>`, `<caption>` e `<th scope>` + commento di review QA sulla PR. | **QA & Accessibilità** *(Cirillo, Lika, Fongaro, Bordin)* |
| **4** | **Contenuti Reali & Coerenza `<nav>`** | **15%** | **1,5 pt** | Ricerca storica/informativa accurata su Feltre, zero *lorem ipsum*, `<nav>` unificata con le altre 4 pagine. | **Product Specialist** *(De Marzo, Xing, Pizzolon, Facchin)* |
| **5** | **Flusso Git, Commit & Pull Request** | **15%** | **1,5 pt** | Uso del branch `sprint1/teamX-...`, messaggi *Conventional Commits*, commit distribuiti tra i membri e PR approvata dallo Scrum Master. | **Tutto il Team** |

> **Formula del Voto Individuale:**  
> $$\text{Voto Finale Studente} = 70\% \text{ Voto Base del Feature Team} + 30\% \text{ Valutazione sul Ruolo Ricoperto}$$

### ⚠️ Penalità Automatiche di Sbarramento
- **$-1,5$ punti** se nel file HTML è presente anche un solo tag `<div>` o `<span>`.
- **$-1,0$ punto** per tentativi di commit diretti su `main` o bypass della Pull Request.
- **$-1,0$ punto** per presenza di testo fittizio (*lorem ipsum*).
- **$-0,5$ punti** per ogni giorno di ritardo nella consegna di `docs/report-sprint1-teamX.md`.
