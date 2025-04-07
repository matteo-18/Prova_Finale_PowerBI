📘 README – Report Power BI: Analisi Olist Store

📌 Descrizione del progetto
Questo progetto è stato realizzato come esercitazione finale per un modulo del corso da Data Analyst. L’obiettivo era quello di sviluppare un report di Business Intelligence utilizzando Power BI, basandosi sul dataset pubblico e anonimizzato di Olist Store, una piattaforma e-commerce brasiliana attiva dal 2016 al 2018.

🎯 Obiettivi di analisi
Il report consente di esplorare dinamicamente:
- L’andamento degli ordini nel tempo, con confronto anno su anno e variazioni percentuali mensili, filtrabili per stato e status ordine
- L’andamento dei ricavi nel tempo, calcolati come somma di prezzo e costo di spedizione
- La distribuzione del punteggio delle recensioni (review score)
- Ulteriori analisi su venditori, prodotti e pagamenti

🧩 Modellazione dei dati
- Ho utilizzato tutte le tabelle principali, escludendo olist_geolocation_dataset poiché le informazioni geografiche necessarie erano già presenti in altre tabelle (customers, sellers).
- Ho costruito un modello a stella:
  - Fatti: olist_orders_dataset, olist_order_items_dataset
  - Dimensioni: tutte le altre tabelle
- Le relazioni tra tabelle sono state impostate direttamente in Power BI

🧼 Pulizia e trasformazione dei dati
- Ho ridotto il volume del dataset eliminando le colonne non necessarie.
- In Power Query ho:
  - Pulito e trasformato i dati, gestendo correttamente i tipi di dato
  - Aggiunto una colonna country per distinguere correttamente gli stati brasiliani da eventuali omonimi esteri
- Ho creato una dimensione calendario con la funzione CALENDAR, arricchita con anno, mese, giorno, nome mese e altri campi utili.

📐 Misure e calcoli DAX
- Ho implementato le misure richieste, tra cui:
  - Numero ordini
  - Ricavi totali (price + freight_value)
  - Variazione percentuale mese su mese e anno su anno
- Ho utilizzato funzioni DAX come PARALLELPERIOD per abilitare confronti temporali.
- Ho anche sviluppato analisi aggiuntive non richieste, come top prodotti venduti, categorie più performanti, stato con miglior rating, ecc.

📊 Struttura del report
Il report è suddiviso in 6 pagine, ciascuna focalizzata su un’area specifica:
1. Sales – andamento ordini, distribuzione geografica, confronto annuale
2. Revenues – andamento ricavi, variazioni YoY, stai/categorie più prolifici
3. Sellers – analisi performance venditori, distribuzione geografica
4. Payments – metodi di pagamento più usati
5. Products – categorie top, prodotti più venduti
6. Reviews – distribuzione review score, media per categoria

🔁 Interattività e UX
- Ogni pagina include un pulsante filtri che apre un menu a comparsa con i filtri principali del report (es. anno, stato, categoria, status ordine…)
- Un menu di navigazione in alto consente di spostarsi facilmente tra le pagine tramite pulsanti dedicati

✅ Considerazioni finali
Il report è stato sviluppato seguendo le best practice di modellazione dati, visual design e usabilità. Il progetto rappresenta una simulazione realistica di un’attività di data analysis in contesto e-commerce, con la possibilità di estendere ulteriormente le analisi integrando nuovi dataset o KPI.
