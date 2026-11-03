# Laboratorio di Machine Learning - Food Delivery Time Prediction

Questo repository contiene il codice e la relazione per il laboratorio del corso di Machine Learning. Il progetto consiste nella riproduzione e nell'analisi critica dell'articolo scientifico: "Food Delivery Time Prediction Using Machine Learning Algorithms: A Comparative Study with Hybrid XGBoost-LSTM Architecture".

## Obiettivo del Progetto
1. Riproduzione: Implementazione dei modelli di Machine Learning proposti nel paper originale (Linear Regression, Decision Tree, Random Forest, XGBoost, LSTM).
2. Ricostruzione dell'Ibrido: Sviluppo dell'architettura ibrida XGBoost-LSTM che unisce l'embedding temporale delle consegne passate con le feature statiche correnti.
3. Analisi Critica: Validazione indipendente dei risultati dichiarati dagli autori e analisi diagnostica del reale apporto della rete ricorrente (LSTM) sulle performance predittive.

## Risultati Principali
La riproduzione ha evidenziato che l'architettura ibrida (MAE 3.07, R² 0.834) offre prestazioni pressoché identiche all'XGBoost standalone (MAE 3.10, R² 0.832), smentendo il netto miglioramento rivendicato nel paper originale (R² 0.912). L'analisi diagnostica ha inoltre dimostrato che il segnale temporale storico (catturato dalla LSTM) risulta debole se decontestualizzato dalle feature statiche della consegna corrente.

## Istruzioni per l'Uso

### 1. Dataset
Il dataset originale utilizzato per l'analisi è già incluso all'interno di questo repository. Si trova nel percorso `data/train.csv`. 

### 2. Esecuzione su Google Colab
Se si desidera riprodurre l'analisi utilizzando Google Colab, seguire questi passaggi:
1. Aprire il file `Food_Delivery_LAB_ML.ipynb` (presente nella cartella `notebooks/`) in Google Colab.
2. Individuare e avviare la prima cella di codice, responsabile del caricamento dei dati.
3. Quando richiesto dall'interfaccia, caricare il file `train.csv` prelevandolo dalla cartella `data/` del repository locale.
4. Una volta caricato il file con successo, eseguire le celle del notebook in sequenza dall'inizio alla fine.

### 3. Requisiti Consigliati
Per un'esecuzione più rapida, si raccomanda di impostare un runtime GPU in Google Colab (NVIDIA T4 o superiore). Questo permetterà di velocizzare sensibilmente l'addestramento dei modelli più complessi.