# Report Formale di Fine Sprint — GPOI (Classe 5ITA)

**Testata / Progetto:** La Ciacola di Feltre — Giornale e Portale Turistico-Culturale Cittadino  
**Sprint N.:*1* `\[1 / 2 / 3 / 4]`  
**Periodo di riferimento:** Dal `\[17/10/2026]` al `\[13/11/2026]` (4 settimane — 8 ore di laboratorio)  
**Feature Team:*STORIA*

* \[ ] **Team 1 (`storia.html`):** Di Dato, De Marzo, Cirillo, Pavan
* \[ ] **Team 2 (`musei.html`):** Corso, Xing, Lika, Romaniuk
* \[ ] **Team 3 (`eventi.html`):** Pizzolon, Fongaro, Merlo
* \[ ] **Team 4 (`mobilita.html`):** Facchin, Bordin, Romagna

**Data di consegna:** `\[12/11/2026]`

\---

## 1\. Ruoli Ricoperti dal Team nello Sprint Corrente

*(Compilare con i cognomi dei membri del proprio Feature Team secondo la rotazione prevista in `docs/pianificazione-sprint.md`. Per i Team 3 e 4 da 3 componenti, indicare il membro che ricopre il doppio ruolo Scrum Master + Product Specialist).*

|Ruolo Aziendale nello Sprint|Cognome Studente|Username GitHub|Ore Presenza Lab (su 8h)|
|-|-|-|:-:|
|**Scrum Master** (Coordinatore e Redattore Report)|`\[Di Dato]`|`@lorenzodidato-a11y`|`\[8/8]`|
|**Product Specialist** (Contenuti e Coerenza)|`\[De Marzo]`|`@username`|`\[8/8]`|
|**QA \& Accessibilità** (Revisione Codice e WCAG)|`\[Cirillo]`|`@ErMagoDaAMagica`|`\[8/8]`|
|**Core Developer** (Implementazione HTML5 e CSS3)|`\[Pavan]`|`@Sandrino-SixSeven67`|`\[8/8]`|

\---

## 2\. Sprint Goal e Riepilogo Esecutivo

* **Obiettivo dello Sprint (Sprint Goal):**  
Strutturare l'albero semantico della pagina "storia.html", raccogliere le prime informazioni riguardo i luoghi storici di Feltre (Es Piazza Maggiore) e controllare la gerarchia dei tag all'interno della pagina attenendosi allo standard W3C.
* **Stato di Raggiungimento dello Sprint Goal:** `Raggiunto al 100%`
* **Sintesi del valore rilasciato:**  
È stata pubblicata la pagina "storia.html" e il file "albero-storia.md", contenente sia la struttura semantica essenziale, sia le informazioni reperite da De Marzo durante queste settimane di lavoro.

\---

## 3\. Metriche Scrumban \& Tracciamento Attività (Issue \& Pull Request)

### 3.1 Stato delle User Story pianificate nello Sprint

|ID Issue|Titolo della User Story / Attività Redazionale|Stato Finale (`Done` / `Carry-over`)|PR Collegata|Responsabile Principale|
|:-:|-|:-:|:-:|-|
|`#01`|Cercare informazioni su Feltre vecchia|Done|`PR #11`|`\[De Marzo]`|
|`#02`|Struttura dello scheletro della pagina "storia.html"|Done|`PR #12`|`\[Pavan]`|
|`#03`|Ispezionare "storia.html"|Done|`PR #13`|`\[Cirillo]`|

### 3.2 Indicatori Quantitativi dello Sprint

* **User Story pianificate:** `\[3]`
* **User Story completate (`Done`):** `\[3]`
* **Tasso di completamento:** `\[100 %]`
* **Pull Request aperte e revisionate:** `\[1]`
* **Rotture della pipeline CI (`w3c-validator.yml`) riscontrate e risolte:** `\[0]`

\---

## 4\. Verifica di Conformità alla Definition of Done (Audit QA)

*Sezione compilata in sinergia tra **QA \& Accessibilità** e <b>Scrum Master</b>.*

|Controllo Architetturale e Qualitativo|Esito (`OK` / `KO`)|Note Tecniche o Evidenze|
|-|:-:|-|
|*OK*Zero `<div>` e Zero `<span>` nel file HTML**|`\[OK]`|Verificato tramite `grep` locale e GitHub Actions.|
|*OK*Validazione W3C Nu Html Checker**|`\[OK]`|Zero errori e zero warning sul markup HTML5.|
|*OK*Skip-link presente e funzionante con `Tab`**|`\[OK]`|`<a href="#contenuto-principale" class="salto-contenuto">` testato.|
|*OK*Gerarchia titoli `<h1>` $\\rightarrow$ `<h2>` $\\rightarrow$ `<h3>`**|`\[OK]`|Un solo `<h1>`, nessun salto di livello rilevato.|
|*OK*Tabelle con `<caption>` e `<th scope="...">`**|`\[OK]`|Tutte le tabelle dati rispettano lo standard di accessibilità.|
|*OK*Immagini in `img/` in `kebab-case` con `alt`**|`\[OK]`|Tutti i file grafici sono minuscoli con descrizione contestuale.|
|*OK*Blocco `<nav>` unificato con gli altri 3 Team**|`\[OK]`|Navigazione principale identica su tutte le 5 pagine.|
|*OK*Assenza totale di testo *lorem ipsum***|`\[OK]`|Tutti i testi riguardano dati reali della Città di Feltre.|

\---

## 5\. Contributi Individuali per Ruolo

* **Scrum Master (`Di Dato`):**  
Creazione delle 3 issue nella scrum board, supervisione durante le ore di lezione del lavoro del gruppo e compilazione del report basandomi sul lavoro svolto.
* **Product Specialist (`De Marzo`):**  
Redatto gli articoli su Castello Alboino, Mura Veneziane, Piazza Maggiore e Porte storiche, usando il sito del comune di Feltre, Dolomiti PreAlpi e Wikipedia
* **QA \& Accessibilità (`Cirillo`):**  
Effettuata la supervisione del lavoro di Pavan, controllando la gerarchia dei tag, l'assenza di div e span e la presenza dello skip-link, senza trovare problemi di sorta.
* **Core Developer (`Pavan`):**  
Realizzato la pagina storia.html con html5 semantico, usando i contenuti raccolti da De Marzo e preparando lo schema della pagina albero-storia.md.

\---

## 6\. Retrospettiva di Sprint (Sprint Retrospective)

### Cosa ha funzionato bene (Keep Doing)

* Il lavoro è stato strutturato bene e la divisione dei ruoli è stata efficace a portare a termine il lavoro.
* La comunicazione, per quanto presenta alcuni problemi dovuti all'inesperienza del gruppo, è stata buona ed ha agevolato lo sprint.

### Impedimenti e Criticità Riscontrate (Problems / Blockers)

* È stato complesso gestire bene i tempi di lavoro, con periodi vuoti e periodi dove si è dovuto strafare per ottenere il risultato. 

### Azioni di Miglioramento per il Prossimo Sprint (Action Items)

1. Creare una tabella di marcia specificando bene i compiti da eseguire entro quando, permettendo così di lavorare con più costanza durante le settimane.
2. `\[Passaggio di consegne per la rotazione dei ruoli del prossimo Sprint]`

\---

**Firma dello Scrum Master:** `Lorenzo Di Dato`  
**Visto di convalida del Team:** `Alessandro Pavan, Aerendil Cirillo, Franco De Marzo`

