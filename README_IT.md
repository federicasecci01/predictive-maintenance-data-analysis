# Predictive Maintenance Data Analysis

## 🇮🇹 Italiano

### Descrizione del progetto

Questo progetto analizza il dataset **AI4I 2020 Predictive Maintenance**, composto da **10.000 osservazioni** relative a un contesto industriale di manutenzione predittiva.

L'obiettivo dell'analisi è esplorare le condizioni operative dei macchinari, confrontare il comportamento delle macchine che hanno registrato un guasto con quello delle macchine che hanno operato normalmente e approfondire la distribuzione delle diverse modalità di guasto presenti nel dataset.

La prima fase del progetto è stata sviluppata in **Microsoft Excel**, utilizzando Power Query, formule, statistiche descrittive, tabelle Pivot e analisi di correlazione.

> **Project status:** work in progress  
> L'analisi in Excel è stata completata. La fase successiva prevede la realizzazione di una dashboard interattiva in Tableau, che verrà aggiunta al repository al termine dello sviluppo.

---

## Obiettivi dell'analisi

- Esplorare le principali variabili operative dei macchinari.
- Confrontare le condizioni operative delle macchine con e senza guasto.
- Analizzare frequenza e distribuzione delle diverse modalità di guasto.
- Confrontare le categorie di prodotto L, M e H.
- Studiare le relazioni tra variabili operative e Machine Failure.
- Preparare i dati per la successiva visualizzazione in Tableau.

---

## Preparazione e trasformazione dei dati

I dati sono stati importati e preparati utilizzando **Power Query**.

Oltre alle variabili originali del dataset, sono state calcolate alcune grandezze aggiuntive utili all'analisi.

### Velocità angolare

La velocità angolare è stata calcolata a partire dalla velocità di rotazione espressa in rpm:

**ω = (2 × π × n) / 60**

dove:
- `ω` = velocità angolare in rad/s
- `n` = velocità di rotazione in rpm

### Differenza di temperatura

È stata calcolata la differenza tra la temperatura di processo e la temperatura dell'aria:

**ΔT = Temperatura di processo − Temperatura dell'aria**

### Potenza meccanica

La potenza meccanica è stata calcolata utilizzando la coppia e la velocità angolare:

**P = T × ω**

dove:
- `P` = potenza meccanica
- `T` = coppia in Nm
- `ω` = velocità angolare in rad/s

Il risultato è stato successivamente convertito in **kW**.

---

## Analisi effettuate

L'analisi comprende:

- statistiche descrittive delle principali variabili operative;
- analisi di correlazione;
- confronto tra macchine con e senza guasto;
- analisi mediante tabelle Pivot;
- analisi delle diverse modalità di guasto;
- confronto dei guasti tra le categorie di prodotto.

Le modalità di guasto considerate nel dataset sono:

- **TWF** — Tool Wear Failure
- **HDF** — Heat Dissipation Failure
- **PWF** — Power Failure
- **OSF** — Overstrain Failure
- **RNF** — Random Failure

---

## Confronto tra macchine con e senza guasto

Una delle analisi principali è stata effettuata confrontando i valori medi delle condizioni operative tra macchine senza guasto e macchine che hanno registrato un Machine Failure.

Per le osservazioni appartenenti alla categoria di prodotto **L**, le macchine che hanno registrato un guasto presentano, rispetto alle macchine senza guasto:

- **Mechanical Power:** circa **+17,6%**
- **Tool Wear:** circa **+39,5%**
- **Torque:** circa **+28,4%**
- **Rotational Speed:** circa **−3,9%**
- **Delta Temperature:** circa **−5,2%**

Il confronto evidenzia quindi differenze particolarmente marcate per **Tool Wear, Torque e Mechanical Power**.

Questi risultati rappresentano un'analisi descrittiva delle condizioni operative associate ai guasti e non implicano, da soli, una relazione causale tra le singole variabili e il verificarsi del Machine Failure.

---

## Primi risultati

Nel dataset sono presenti **339 Machine Failures su 10.000 osservazioni**, corrispondenti a circa il **3,39% del totale**.

Tra le modalità di guasto registrate, **Heat Dissipation Failure (HDF)** risulta la più frequente, seguita da **Overstrain Failure (OSF)** e **Power Failure (PWF)**.

È stata inoltre effettuata un'analisi di correlazione per valutare la relazione lineare tra alcune variabili operative e la variabile **Machine Failure**.

I coefficienti di correlazione ottenuti sono:

- **Mechanical Power – Machine Failure:** `r = 0.176`
- **Tool Wear – Machine Failure:** `r = 0.105`
- **Delta Temperature – Machine Failure:** `r = -0.112`

I coefficienti mostrano relazioni lineari complessivamente deboli.

Mechanical Power e Tool Wear presentano una debole associazione positiva con Machine Failure, mentre Delta Temperature mostra una debole associazione negativa.

Nel complesso, i risultati indicano che nessuna delle variabili considerate, presa singolarmente, presenta una relazione lineare sufficientemente forte da descrivere da sola il fenomeno del guasto. L'analisi congiunta di più condizioni operative può quindi offrire una rappresentazione più completa del comportamento dei macchinari.

---

## Strumenti utilizzati

### Microsoft Excel
- Power Query
- Pivot Tables
- Descriptive Statistics
- Correlation Analysis
- Data Cleaning
- Data Transformation
- Feature Engineering

### Tableau — in sviluppo
- Interactive Dashboard
- KPI Visualization
- Failure Analysis
- Operating Conditions Comparison

---

## Stato del progetto

**Data Preparation:** completata  
**Excel Analysis:** completata  
**Descriptive Statistics:** completata  
**Correlation Analysis:** completata  
**Failure Analysis:** completata  
**Tableau Dashboard:** in sviluppo

La dashboard Tableau e le relative visualizzazioni verranno aggiunte in un aggiornamento successivo.



The Tableau dashboard and related visualizations will be added in a future update.
