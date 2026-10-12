---
name: work-item
description: Scrive epiche, user story e sub-task secondo il template comune dei team. Verifica che ci siano tutte le informazioni richieste dal template e, se mancano, le chiede prima di scrivere. Usare quando si chiede di scrivere, creare o riscrivere una epica, una user story o un sub-task.
---

# Work item

Questa skill scrive tre tipi di work item: **Epica**, **User Story**, **Sub-task**.

Ogni work item ha due parti: **Titolo** e **Descrizione**. La Descrizione contiene le sezioni del tipo.

Il template di ciascun tipo è obbligatorio: sezioni, nomi e ordine non si cambiano, non si aggiungono e non si tolgono.

## Regole comuni

- Non inventare contenuti. Quello che manca si chiede a chi scrive: ha tutte le informazioni.
- Scrivi in italiano.
- Identifica prima il tipo di work item. Se dalla richiesta non è chiaro, chiedilo.
- I work item devono essere brevi. Ogni frase deve servire a chi lo legge per capire o verificare il lavoro. Niente premesse, ripetizioni o spiegazioni generiche.

## Check di completezza

1. Confronta quanto fornito con le sezioni obbligatorie del tipo e con i loro criteri.
2. Se una sezione manca o non rispetta il criterio, non scrivere il work item. Fai tutte le domande in un unico messaggio, numerate, senza chiedere ciò che è già stato detto.
3. Scrivi il work item solo quando le sezioni obbligatorie sono complete.
4. Dopo la stesura, verifica di nuovo ogni sezione contro il suo criterio, e i titoli e la dimensione (sezioni sotto). Se qualcosa non torna, correggi o chiedi.

## Epica

L'epica descrive un obiettivo di prodotto ad alto livello. Raggruppa più user story correlate.

Tutto è obbligatorio.

**Titolo**: nome dell'epica, descrittivo e univoco.

**Descrizione**:

| Sezione | Contenuto |
|---|---|
| **Contesto e Necessità** | Perché serve questa feature, dal punto di vista business o utente |
| **Obiettivo** | Cosa vogliamo ottenere con questa epica |
| **Ambito** | Cosa include questa epica, lista di funzionalità |
| **Sistemi Coinvolti** | Microservizi o componenti impattati |
| **Vincoli** | Assunzioni tecniche o architetturali da rispettare |
| **Acceptance Criteria Epica** | Quando l'intera epica si considera completata |

## User Story

La user story descrive una funzionalità specifica, da implementare e testare.

**Titolo**: obbligatorio.

**Descrizione**:

| Sezione | Contenuto | Obbligatoria |
|---|---|---|
| **Obiettivo** | Cosa deve fare questa story e quale valore apporta, in una o due frasi | sì |
| **Implementazione** | Checklist tecnica per i dev: cosa va fatto, in quale componente, con quale logica | no alla creazione: si scrive dopo il refinement |
| **Acceptance Criteria (AC)** | Definizione di done a livello funzionale. Non è una lista di task tecnici: è la condizione osservabile che dice che la story è finita | sì |

Le AC devono essere verificabili. "Il sistema deve funzionare" non è una AC. "Quando l'utente invia X, il sistema risponde con Y entro Z secondi" lo è.

Se l'Implementazione è presente, ogni voce indica cosa va fatto, in quale componente e con quale logica.

## Sub-task

**Titolo**: obbligatorio.

**Descrizione**: breve, obbligatoria.

Si crea solo in due casi:

- il work item richiede modifiche su componenti indipendenti o su parti diverse dello stesso componente;
- più dev possono lavorare contemporaneamente su parti distinte.

Se nessuno dei due casi vale, non creare il sub-task: il lavoro resta nella story. Chiedi quale caso si applica se non è chiaro.

Non creare sub-task per fase di lavoro (Analisi, Sviluppo, Test, Review, Deploy).

## Titoli

- **Epica**: nome della capacità o del risultato. Non generico ("Miglioramenti", "Fase 2") e univoco.
- **User Story**: verbo + oggetto + contesto, comprensibile senza aprire la story.
- **Sub-task**: verbo + parte o componente su cui si lavora.

## Dimensione

- **User Story troppo grande**: se descrive più comportamenti distinti, segnalalo e proponi di dividerla. Non dividerla da solo.
- **Epica che è una story**: se contiene una sola funzionalità, segnalalo e proponi di scriverla come user story.

Il numero di AC dipende dal contesto: non c'è un minimo né un massimo.

## Output

Markdown semplice, sezioni nell'ordine del template. Il Titolo va nel campo titolo di Jira, il resto nel campo descrizione.

Epica:

```
**Titolo**: …

**Descrizione**

**Contesto e Necessità**
…

**Obiettivo**
…

**Ambito**
- …

**Sistemi Coinvolti**
- …

**Vincoli**
- …

**Acceptance Criteria Epica**
- …
```

User Story:

```
**Titolo**: …

**Descrizione**

**Obiettivo**
…

**Implementazione**
- [ ] …

**Acceptance Criteria (AC)**
- …
```

Ometti **Implementazione** se non è ancora stata scritta.

Sub-task:

```
**Titolo**: …

**Descrizione**
…
```
