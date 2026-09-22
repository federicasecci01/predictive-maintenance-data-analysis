🇬🇧 [English](README.md) | 🇮🇹 Italiano

# Predictive Maintenance Data Analysis

### Analisi delle condizioni operative e dei guasti attraverso Excel, statistica descrittiva e Tableau

Questo progetto analizza il dataset **AI4I 2020 Predictive Maintenance**, composto da **10.000 osservazioni** relative a un contesto industriale di manutenzione predittiva.

L'obiettivo del progetto è studiare il comportamento operativo dei macchinari, confrontare le condizioni delle macchine che hanno registrato un guasto con quelle che hanno operato normalmente e analizzare le diverse modalità di guasto presenti nel dataset.

Il progetto combina **Microsoft Excel e Power Query** per la preparazione, trasformazione e analisi quantitativa dei dati con **Tableau**, che verrà utilizzato nella fase finale per la costruzione di una dashboard interattiva.

La mia formazione in **Matematica** ha influenzato l'approccio utilizzato, in particolare nella costruzione di nuove variabili quantitative, nell'impiego della statistica descrittiva, nell'analisi delle correlazioni e nell'interpretazione dei risultati.

> **Stato del progetto:** in corso di sviluppo.  
> L'analisi in Excel è stata completata. La dashboard Tableau è attualmente in fase di realizzazione e verrà aggiunta al repository al termine dello sviluppo.

---

## Obiettivi dell'analisi

L'analisi è stata sviluppata a partire da alcune domande principali:

* Qual è la frequenza complessiva dei guasti nel dataset?
* Quali modalità di guasto si verificano più frequentemente?
* Le condizioni operative medie differiscono tra macchine con e senza guasto?
* Quali differenze emergono in termini di coppia, potenza, usura dell'utensile, velocità di rotazione e temperatura?
* Esistono relazioni lineari tra le variabili operative e il verificarsi di un Machine Failure?
* Come varia la frequenza dei guasti tra le categorie di prodotto L, M e H?
* È possibile sintetizzare i principali risultati attraverso una dashboard interattiva?

L'obiettivo non è stato soltanto descrivere il dataset, ma costruire un processo analitico strutturato che permettesse di collegare le condizioni operative dei macchinari ai fenomeni di guasto osservati.

---

## Preparazione e trasformazione dei dati

**Microsoft Excel** e **Power Query** sono stati utilizzati per la preparazione e la trasformazione del dataset.

Il processo ha incluso:

* importazione del dataset;
* controllo e correzione dei tipi di dato;
* gestione delle variabili relative ai guasti;
* verifica della struttura del dataset;
* creazione di nuove variabili quantitative utili all'analisi.

### Velocità angolare

La velocità angolare è stata ricavata dalla velocità di rotazione espressa in rpm:

**ω = (2 × π × n) / 60**

dove:

* `ω` = velocità angolare in rad/s;
* `n` = velocità di rotazione in rpm.

### Differenza di temperatura

È stata calcolata la differenza tra la temperatura di processo e la temperatura dell'aria:

**ΔT = Temperatura di processo − Temperatura dell'aria**

Questa variabile consente di rappresentare direttamente lo scarto termico tra processo e ambiente.

### Potenza meccanica

La potenza meccanica è stata calcolata utilizzando coppia e velocità angolare:

**P = T × ω**

dove:

* `P` = potenza meccanica;
* `T` = coppia in Nm;
* `ω` = velocità angolare in rad/s.

Il risultato è stato successivamente convertito in **kW**.

L'introduzione di queste variabili ha permesso di estendere il dataset originale con grandezze direttamente interpretabili dal punto di vista fisico e meccanico.

---

## Analisi esplorativa e statistica

L'analisi quantitativa ha incluso:

* statistiche descrittive delle principali variabili operative;
* confronto tra media, mediana, deviazione standard, minimo e massimo;
* Tabelle Pivot;
* analisi delle macchine con e senza guasto;
* analisi delle modalità di guasto;
* confronto tra le categorie di prodotto L, M e H;
* matrice di correlazione;
* analisi delle relazioni tra variabili operative e Machine Failure.

Le principali variabili considerate comprendono:

* Air Temperature;
* Process Temperature;
* Rotational Speed;
* Torque;
* Tool Wear;
* Delta Temperature;
* Angular Velocity;
* Mechanical Power.

---

## Modalità di guasto

Il dataset distingue diverse tipologie di guasto:

* **TWF — Tool Wear Failure**
* **HDF — Heat Dissipation Failure**
* **PWF — Power Failure**
* **OSF — Overstrain Failure**
* **RNF — Random Failure**

L'analisi ha permesso di confrontarne la frequenza e la distribuzione all'interno del dataset.

---

## Confronto tra macchine con e senza guasto

Una delle principali Tabelle Pivot è stata utilizzata per confrontare le **condizioni operative medie** delle macchine che non hanno registrato guasti con quelle che hanno registrato un Machine Failure.

Il confronto considera variabili quali:

* Rotational Speed;
* Delta Temperature;
* Mechanical Power;
* Tool Wear;
* Torque.

I risultati evidenziano differenze nelle condizioni operative medie tra i due gruppi.

In particolare, le macchine che hanno registrato un guasto presentano:

* **Mechanical Power:** circa `+XX%`
* **Tool Wear:** circa `+XX%`
* **Torque:** circa `+XX%`
* **Rotational Speed:** circa `−XX%`
* **Delta Temperature:** circa `−XX%`

Le differenze più rilevanti emergono in particolare per **Tool Wear, Torque e Mechanical Power**.

Questa analisi permette di individuare alcune caratteristiche operative associate ai casi di guasto presenti nel dataset. I risultati hanno tuttavia natura **descrittiva** e non devono essere interpretati come prova di una relazione causale tra una singola variabile e il verificarsi del guasto.

> I valori percentuali verranno aggiornati sulla base della versione definitiva della Tabella Pivot.

---

## Analisi di correlazione

È stata costruita una matrice di correlazione per analizzare le relazioni lineari tra le principali variabili operative e la variabile **Machine Failure**.

Tra i valori osservati:

* **Mechanical Power – Machine Failure:** `r = 0.176`
* **Tool Wear – Machine Failure:** `r = 0.105`
* **Delta Temperature – Machine Failure:** `r = -0.112`

I coefficienti indicano relazioni lineari complessivamente **deboli**.

Mechanical Power e Tool Wear mostrano una debole associazione positiva con Machine Failure, mentre Delta Temperature presenta una debole associazione negativa.

Questi risultati suggeriscono che nessuna delle singole variabili considerate presenta, da sola, una relazione lineare sufficientemente forte da descrivere il verificarsi di un guasto.

L'analisi congiunta di più condizioni operative può quindi fornire una rappresentazione più completa del comportamento dei macchinari.

È importante sottolineare che la correlazione misura un'associazione lineare e **non implica una relazione di causalità**.

---

## Risultati principali

Nel dataset sono presenti:

**10.000 osservazioni**

**339 Machine Failures**

**Failure Rate complessivo: circa 3,39%**

Tra le modalità di guasto registrate, **Heat Dissipation Failure (HDF)** risulta la più frequente, seguita da **Overstrain Failure (OSF)** e **Power Failure (PWF)**.

Il confronto tra macchine con e senza guasto evidenzia inoltre differenze nelle condizioni operative, in particolare per **Tool Wear, Torque e Mechanical Power**.

Nel complesso, l'analisi mostra come il fenomeno del guasto non possa essere ricondotto semplicemente al comportamento di una singola variabile, ma debba essere osservato considerando simultaneamente più caratteristiche operative.

---

## Dashboard interattiva in Tableau

La fase finale del progetto prevede la trasformazione dei risultati ottenuti in Excel in una **dashboard interattiva sviluppata in Tableau**.

La dashboard sarà progettata per sintetizzare visivamente i principali risultati dell'analisi e consentire un'esplorazione dinamica dei dati.

In particolare comprenderà:

* KPI relativi al numero complessivo di Machine Failures;
* Failure Rate;
* distribuzione delle diverse modalità di guasto;
* confronto tra macchine con e senza guasto;
* confronto tra le categorie di prodotto L, M e H;
* analisi delle principali condizioni operative;
* visualizzazione degli insight emersi durante l'analisi esplorativa.

### Dashboard interattiva

**Attualmente in fase di sviluppo.**

Al completamento del progetto verranno aggiunti:

* anteprima della dashboard;
* collegamento alla dashboard interattiva su Tableau Public.

<!--
![Predictive Maintenance Dashboard](dashboard_preview.png)

[Esplora la dashboard su Tableau Public](INSERIRE_LINK)
-->

---

## Strumenti e competenze

**Microsoft Excel**

* Power Query
* Data Cleaning
* Data Transformation
* Tabelle Pivot
* Statistica descrittiva
* Correlation Analysis
* Exploratory Data Analysis
* Feature Engineering

**Tableau**

* Dashboard interattive
* KPI
* Filtri
* Data Visualization
* Analisi comparativa

**Competenze quantitative**

* Statistica descrittiva
* Analisi di correlazione
* Ragionamento quantitativo
* Interpretazione dei dati
* Analisi comparativa
* Applicazione di grandezze fisiche e meccaniche
* Problem solving analitico

---

## Contenuto del repository

| File | Contenuto |
| --- | --- |
| `predictive-maintenance-excel-analysis.xlsx` | Workbook Excel contenente preparazione dei dati, statistiche descrittive, Tabelle Pivot e analisi di correlazione |
| `dashboard_preview.png` | Anteprima della dashboard Tableau — verrà aggiunta al completamento del progetto |
| Tableau Workbook | Verrà aggiunto al completamento della dashboard |

---

## Fonte del dataset

Il progetto utilizza il dataset **AI4I 2020 Predictive Maintenance**, sviluppato come dataset sintetico per rappresentare un contesto industriale di manutenzione predittiva.

Il dataset è stato utilizzato a scopo formativo e di portfolio.

La preparazione dei dati, la costruzione delle variabili aggiuntive, le analisi statistiche, le Tabelle Pivot, l'interpretazione dei risultati e la futura dashboard Tableau sono state sviluppate nell'ambito del mio portfolio personale di Data Analytics.

---

## Il progetto

Questo progetto rappresenta un'applicazione della mia **formazione matematica alla Data Analytics in ambito industriale**, combinando statistica descrittiva, ragionamento quantitativo e interpretazione di grandezze fisiche con strumenti utilizzati per la preparazione, l'analisi e la visualizzazione dei dati.

Fa parte di un portfolio in evoluzione orientato alla trasformazione delle competenze teoriche e analitiche in progetti pratici basati sui dati.
