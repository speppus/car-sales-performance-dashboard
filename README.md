# 🚗 Car Sales Performance Analysis
### Capstone Project – Data Analysis with Python & Power BI  
---

# 📌 Project Overview

Questo progetto analizza le **performance di vendita, il comportamento dei clienti e l'efficienza dello stock** di una concessionaria automobilistica.

L'obiettivo dell’analisi è trasformare dati grezzi di vendita e inventario in **insight strategici utili per supportare decisioni aziendali basate sui dati (data-driven decision making)**.

Il progetto è stato sviluppato utilizzando:

- **Python** per il data cleaning e la preparazione dei dati
- **Power BI** per la modellazione dei dati e la creazione della dashboard interattiva

La dashboard permette di monitorare:

- performance commerciali
- segmentazione dei clienti
- andamento delle vendite nel tempo
- gestione dello stock
- rischio di inventario

---

# 🎯 Business Objective

Lo scopo dell’analisi è supportare il management della concessionaria nel rispondere a domande strategiche come:

- Quali brand generano il maggior fatturato?
- Quali segmenti di clienti sono più profittevoli?
- Come si stanno evolvendo le vendite nel tempo?
- Quali modelli o brand presentano rischio di stock elevato?
- Dove è possibile migliorare l’efficienza dell’inventario?

Attraverso queste analisi è possibile individuare **opportunità di crescita e aree di inefficienza operativa**.

---

# 📂 Dataset Description

Il dataset rappresenta le operazioni di vendita di una concessionaria automobilistica e include informazioni relative a:

- Brand e modelli delle auto
- Prezzo di vendita
- Tipo di motore
- Quantità vendute
- Stock disponibile
- Informazioni sui clienti
- Data delle transazioni

I dati sono stati puliti e trasformati per essere utilizzati nell’analisi.

---

# 🧹 Data Cleaning (Python)

Prima dell’analisi è stata effettuata una fase di **data cleaning utilizzando Python e la libreria Pandas**.

Le principali operazioni effettuate includono:

- rimozione dei valori nulli
- conversione dei tipi di dato
- pulizia delle colonne di prezzo
- standardizzazione dei nomi delle colonne
- creazione di nuove variabili utili all’analisi
- verifica della presenza di duplicati
- trasformazione delle colonne temporali

Esempio di operazioni di pulizia:

```python
import pandas as pd

df = pd.read_csv("sales_data.csv")

# Rimozione valori nulli
df = df.dropna()

# Conversione prezzo
df["Price"] = df["Price"].replace(r'[$,]', '', regex=True).astype(float)

# Conversione data
df["Sale_Date"] = pd.to_datetime(df["Sale_Date"])

# Verifica duplicati
df = df.drop_duplicates()
