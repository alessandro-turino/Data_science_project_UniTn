In questa repository ci sono tutti i file e i notebook per il progetto del corso di data science creati da Francesco Tanesini e Alessandro Turino.

Il progetto consiste nel creare un modello di machine learning che permetta di prevedere i consumi energetici del comune e della provincia di Trento di un dato giorno e fascia oraria avendo a disposizione una serie di dati del giorno precedente. 
I dati a disposizione sono: consumi energetici, dati meteo tra cui temperature e precipitazioni e infine dati twitter. Le fasce temporali utilizzate sono state 'giorno': 08:00 - 19:00 e 'sera': 19:00 - 24:00.
I dati coprono un intervallo temporale di due mesi, in particolare i mesi di novembre e dicembre del 2013.

La cartella 'data_trentino' contiene tutti i dati usati nel progetto, e sono stati scaricati direttamente dal sito https://dataverse.harvard.edu/dataverse/bigdatachallenge.  Il sito https://www.nature.com/articles/sdata201555#Fig2
spiega in maniera dettagliata come leggere e interpretare i vari dataset.

I file ProjectEDA.ipynb, ProjectCLASS.ipynb e ProjectREG.ipynb sono i notebook python in cui c'è l'intero progetto, rispettivamente sono la parte di EDA (Explorative Data Analysis), classificazione e regressione. Nella parte di 
EDA sono stati creati i dataset usati poi nella classificazione e nella regressione e si sono fatte alcune considerazioni iniziali a partire dai dati grezzi. In classifiazione e' stato creato un modello di machine learning che permette
di prevedere quali celle saranno ad alto consumo e quali non nella zona urbana di Trento. Le scelte della soglia per discriminare alto consumo da basso consumo e di quali zone della provincia di Trento sono state prese in considerazione
come zona urbana di Trento sono spiegate nella fase di EDA. In regressione e' stato invece creato un modello di machine learning che permette di prevedere il consumo energetico della provincia e del comune di Trento.

Il file Com01012013_g_WGS84.shp e' il file (come spiegato in ProjectEDA.ipynb) scaricato direttamente dal sito ufficiale dell'ISTAT in cui sono presenti le coordinate di tutti i confini dei comuni italiani. E' stato molto comodo in fase di EDA
per riuscire a selezionare solo le zone del comune di Trento che sono poi servite per la fase di regressione e classificazione

La foto 'Trentino_idroelettrico.jpg' e' un'immagine del Trentino in cui sono in evidenza le posizioni delle varie dighe idroelettriche, utile nella fase di EDA.

I file trentino_dataset_class.xls e trentino_dataset_reg.xls sono i dataset risultanti dal notebook ProjectEDA.ipynb, rispettivamente sono quelli usati poi per la classificazione e la regressione. Il file trentino_dataset_reg_trento.xls
e' stato ricavato dal file trentino_dataset_reg.xls prendendo pero' solo le zone del comune di Trento. Infine i file trentino_dataset_class_ristretto.xls e trentino_dataset_reg_ristretto.xls sono i file risultanti sempre dal file 
ProjectEDA.ipynb in cui pero' sono state cambiate le fasce orarie da 08:00 - 19:00 e 19:00 - 24:00 in 09:00 - 12:00 e 18:00 - 21:00. Il motivo per cui abbiamo creato anche questi file e' che tra le richieste del progetto c'era di 
provare a spiegare se fosse o meno possibile usare delle fasce orarie piu' strette: abbiamo quindi optato di effettuare la stessa analisi dati e training del modello fatti per le fasce orarie piu ampie anche su due fasce piu' piccole,
cosi' da vedere se i risultati fossero migliori, peggiori o invariati.
