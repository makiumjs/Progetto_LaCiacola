# 🧭 COMANDI GIT — Guida Passo-Passo per Scrum Master e Compagni di Team (5ITA)

> **💡 PERCHÉ NON VEDETE IL BRANCH DEI COMPAGNI?**  
> Quando lo **Scrum Master** crea un branch sul suo PC con `git checkout -b`, quel branch **esiste solo sul suo computer finché non fa `git push`!**  
> Seguite nell'ordine esatto: **prima la FASE 1 (solo lo Scrum Master)** e **dopo la FASE 2 (i compagni di Team)**.

---

## 📖 Mini-Dizionario: Cosa fa ogni comando? (Leggi prima di incollare)

| Comando | Cosa significa in italiano semplice |
| :--- | :--- |
| `git checkout main` | *"Spostami sul ramo principale `main`"* |
| `git pull origin main` | *"Scarica da GitHub (`origin`) le ultime novità di `main` sul mio PC"* |
| `git checkout -b nome-branch` | *"Crea un **nuovo** ramo (`-b`) chiamato `nome-branch` ed entraci dentro"* *(Lo fa SOLO chi crea il branch per primo!)* |
| `git push -u origin nome-branch` | *"Pubblica questo nuovo ramo su GitHub così anche i miei compagni possono vederlo"* |
| `git fetch --all` | *"Chiedi a GitHub quali nuovi branch sono stati creati dai miei compagni"* |
| `git checkout nome-branch` | *(Senza `-b`!)* *"Entra nel branch che il mio Scrum Master ha già creato su GitHub"* |
| `git status` | *"Dimmi su quale branch mi trovo adesso e quali file ho modificato"* |

---

# 🏛️ TEAM 1 — `storia.html` (Di Dato, De Marzo, Cirillo, Pavan)

### 👑 FASE 1 — SOLO per lo Scrum Master (**DI DATO**)
**Di Dato**, apri il terminale di VS Code e copia-incolla questi **4 comandi uno alla volta** per creare il branch del Team 1 e pubblicarlo su GitHub:

```bash
git checkout main
git pull origin main
git checkout -b sprint1/team1-storia
git push -u origin sprint1/team1-storia
```
✅ *Quando vedi scritto `new branch -> sprint1/team1-storia`, avvisa i tuoi compagni che possono fare la Fase 2!*

---

### 🤝 FASE 2 — Per i Compagni del Team 1 (**DE MARZO, CIRILLO, PAVAN**)
**Aspettate che Di Dato abbia finito la Fase 1!** Poi aprite il terminale di VS Code e incollate questi **3 comandi** per collegarvi al suo branch *(NOTATE CHE NON C'È `-b`!)*:

```bash
git fetch --all
git checkout sprint1/team1-storia
git pull origin sprint1/team1-storia
```
✅ *Controllo: scrivete `git status`. Deve comparire: `On branch sprint1/team1-storia`.*

---

### 💾 FASE 3 — Come Salvare e Inviare le Modifiche (Tutti i membri del Team 1)
Ogni volta che avete modificato `storia.html` (o il report) e volete mandarlo su GitHub:

```bash
# 1. Scarica prima eventuali modifiche appena inviate dai tuoi compagni di team
git pull origin sprint1/team1-storia

# 2. Prepara il file modificato
git add storia.html

# 3. Salva con un messaggio chiaro
git commit -m "feat(storia): aggiunta contenuti e struttura semantica"

# 4. Invia sul branch del Team 1 su GitHub
git push origin sprint1/team1-storia
```

---
---

# 🎨 TEAM 2 — `musei.html` (Corso, Xing, Lika, Romaniuk)

### 👑 FASE 1 — SOLO per lo Scrum Master (**CORSO**)
**Corso**, apri il terminale di VS Code e copia-incolla questi **4 comandi uno alla volta** per creare il branch del Team 2 e pubblicarlo su GitHub:

```bash
git checkout main
git pull origin main
git checkout -b sprint1/team2-musei
git push -u origin sprint1/team2-musei
```
✅ *Quando vedi scritto `new branch -> sprint1/team2-musei`, avvisa i tuoi compagni che possono fare la Fase 2!*

---

### 🤝 FASE 2 — Per i Compagni del Team 2 (**XING, LIKA, ROMANIUK**)
**Aspettate che Corso abbia finito la Fase 1!** Poi aprite il terminale di VS Code e incollate questi **3 comandi** per collegarvi al suo branch *(SENZA `-b`!)*:

```bash
git fetch --all
git checkout sprint1/team2-musei
git pull origin sprint1/team2-musei
```
✅ *Controllo: scrivete `git status`. Deve comparire: `On branch sprint1/team2-musei`.*

---

### 💾 FASE 3 — Come Salvare e Inviare le Modifiche (Tutti i membri del Team 2)
Ogni volta che avete modificato `musei.html` e volete mandarlo su GitHub:

```bash
# 1. Scarica prima eventuali modifiche appena inviate dai tuoi compagni di team
git pull origin sprint1/team2-musei

# 2. Prepara il file modificato
git add musei.html

# 3. Salva con un messaggio chiaro
git commit -m "feat(musei): aggiunta contenuti e struttura semantica"

# 4. Invia sul branch del Team 2 su GitHub
git push origin sprint1/team2-musei
```

---
---

# 🎪 TEAM 3 — `eventi.html` (Pizzolon, Fongaro, Merlo)

### 👑 FASE 1 — SOLO per lo Scrum Master (**PIZZOLON**)
**Pizzolon**, apri il terminale di VS Code e copia-incolla questi **4 comandi uno alla volta** per creare il branch del Team 3 e pubblicarlo su GitHub:

```bash
git checkout main
git pull origin main
git checkout -b sprint1/team3-eventi
git push -u origin sprint1/team3-eventi
```
✅ *Quando vedi scritto `new branch -> sprint1/team3-eventi`, avvisa Fongaro e Merlo che possono fare la Fase 2!*

---

### 🤝 FASE 2 — Per i Compagni del Team 3 (**FONGARO, MERLO**)
**Aspettate che Pizzolon abbia finito la Fase 1!** Poi aprite il terminale di VS Code e incollate questi **3 comandi** per collegarvi al suo branch *(SENZA `-b`!)*:

```bash
git fetch --all
git checkout sprint1/team3-eventi
git pull origin sprint1/team3-eventi
```
✅ *Controllo: scrivete `git status`. Deve comparire: `On branch sprint1/team3-eventi`.*

---

### 💾 FASE 3 — Come Salvare e Inviare le Modifiche (Tutti i membri del Team 3)
Ogni volta che avete modificato `eventi.html` e volete mandarlo su GitHub:

```bash
# 1. Scarica prima eventuali modifiche appena inviate dai tuoi compagni di team
git pull origin sprint1/team3-eventi

# 2. Prepara il file modificato
git add eventi.html

# 3. Salva con un messaggio chiaro
git commit -m "feat(eventi): aggiunta contenuti e struttura semantica"

# 4. Invia sul branch del Team 3 su GitHub
git push origin sprint1/team3-eventi
```

---
---

# 🚌 TEAM 4 — `mobilita.html` (Facchin, Bordin, Romagna)

### 👑 FASE 1 — SOLO per lo Scrum Master (**FACCHIN**)
**Facchin**, apri il terminale di VS Code e copia-incolla questi **4 comandi uno alla volta** per creare il branch del Team 4 e pubblicarlo su GitHub:

```bash
git checkout main
git pull origin main
git checkout -b sprint1/team4-mobilita
git push -u origin sprint1/team4-mobilita
```
✅ *Quando vedi scritto `new branch -> sprint1/team4-mobilita`, avvisa Bordin e Romagna che possono fare la Fase 2!*

---

### 🤝 FASE 2 — Per i Compagni del Team 4 (**BORDIN, ROMAGNA**)
**Aspettate che Facchin abbia finito la Fase 1!** Poi aprite il terminale di VS Code e incollate questi **3 comandi** per collegarvi al suo branch *(SENZA `-b`!)*:

```bash
git fetch --all
git checkout sprint1/team4-mobilita
git pull origin sprint1/team4-mobilita
```
✅ *Controllo: scrivete `git status`. Deve comparire: `On branch sprint1/team4-mobilita`.*

---

### 💾 FASE 3 — Come Salvare e Inviare le Modifiche (Tutti i membri del Team 4)
Ogni volta che avete modificato `mobilita.html` e volete mandarlo su GitHub:

```bash
# 1. Scarica prima eventuali modifiche appena inviate dai tuoi compagni di team
git pull origin sprint1/team4-mobilita

# 2. Prepara il file modificato
git add mobilita.html

# 3. Salva con un messaggio chiaro
git commit -m "feat(mobilita): aggiunta contenuti e struttura semantica"

# 4. Invia sul branch del Team 4 su GitHub
git push origin sprint1/team4-mobilita
```

---

## 🆘 SOS Errori Comuni (Se il Terminale diventa Rosso)

1. **Errore: `fatal: a branch named 'sprint1/teamX-...' already exists`**
   * **Perché succede:** Hai scritto `-b` ma il branch esiste già sul tuo PC!
   * **Come si risolve:** Togli `-b` e scrivi solo:
     ```bash
     git checkout sprint1/team1-storia
     ```
     *(Sostituisci con il nome del tuo team).*

2. **Errore: `error: pathspec 'sprint1/teamX-...' did not match any file(s) known to git`**
   * **Perché succede:** Il tuo Scrum Master non ha ancora fatto il comando `git push -u origin ...` (oppure tu non hai fatto `git fetch --all`).
   * **Come si risolve:** Assicurati che lo Scrum Master abbia eseguito il 4° comando della Fase 1, poi scrivi `git fetch --all` e riprova.

3. **Errore: `Please commit your changes or stash them before you switch branches`**
   * **Perché succede:** Hai modificato un file mentre eri ancora su `main` prima di cambiare branch.
   * **Come si risolve:** Scrivi:
     ```bash
     git stash
     git fetch --all
     git checkout sprint1/team1-storia
     git stash pop
     ```
