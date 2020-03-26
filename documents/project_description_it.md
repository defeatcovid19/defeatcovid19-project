# Descrizione del progetto

*Sviluppo di un modello di analisi di immagini cliniche per finalità di supporto alla diagnosi medica*

25 marzo 2020

## Revisioni

| Versione | Data       |  Note               |
|:--------:|:----------:|:--------------------|
|      1.0 | 2020-03-17 | Stesura documento   |
|      2.0 | 2020-03-25 | Revisione documento |


## Indice

- [Revisioni](#revisioni)
- [Indice](#indice)
- [Finalità del documento](#finalità-del-documento)
- [Stato dell'arte](#stato-dellarte)
  * [Intelligenza Artificiale (AI) ed analisi clinica](#intelligenza-artificiale-ai-ed-analisi-clinica)
  * [Screening e diagnosi dei pazienti affetti da COVID-19](#screening-e-diagnosi-dei-pazienti-affetti-da-COVID-19)
- [Sinossi degli studi](#sinossi-degli-studi)
  * [Studio 1: Analisi di immagini radiologiche polmonari](#studio-1-analisi-di-immagini-radiologiche-polmonari)
    + [Obiettivi dello studio](#obiettivi-dello-studio)
    + [Popolazione dello studio](#popolazione-dello-studio)
    + [Periodo dello studio](#periodo-dello-studio)
    + [Dati analizzati](#dati-analizzati)
    + [Risultati attesi](#risultati-attesi)
  * [Studio 2: Analisi di immagini ecografiche cardiache (e polmonari)](#studio-2-analisi-di-immagini-ecografiche-cardiache-e-polmonari)
    + [Obiettivi dello studio](#obiettivi-dello-studio-1)
    + [Popolazione dello studio](#popolazione-dello-studio-1)
    + [Periodo dello studio](#periodo-dello-studio-1)
    + [Dati analizzati](#dati-analizzati-1)
    + [Risultati attesi](#risultati-attesi-1)
- [Trattamento dei dati personali e dei risultati raggiunti](#trattamento-dei-dati-personali-e-dei-risultati-raggiunti)
- [Note](#note)


## Finalità del documento

Il presente documento ha la finalità di illustrare il progetto di ricerca che il gruppo di lavoro #defeatCOVID-19 intende portare avanti al fine di sviluppare un sistema di supporto alle diagnosi di patologie polmonari. A tale scopo nel presente documento sarà presentato lo stato dell'arte della ricerca in ambito di machine learning e saranno inquadrate le potenzialità dello strumento che si vuole sviluppare e il percorso di sviluppo del piano di ricerca.


## Stato dell'arte

### Intelligenza Artificiale (AI) ed analisi clinica

Le moderne tecniche di imaging clinico sono in grado di offrire al medico informazioni preziose nella diagnosi precoce delle polmoniti con infiltrato interstiziale bilaterale, tipiche delle infezioni gravi da nuovo coronavirus. L'utilizzo di strumenti quali l'analisi radiologica in fase di ricovero e di decorso della malattia, unite al monitoraggio ecografico possono fornire un quadro clinico del paziente preciso consentendo al medico di  incrementare la possibilità di prognosi favorevole.

L'acquisizione di immagini mediante strumenti radiologici ed ecografici consente parimenti al medico di poter disporre di un quadro di valutazione che, unito ai dati clinici del paziente, può consentire l'adozione tempestiva di determinati protocolli di terapia, e monitorarne l'impatto nel tempo.

L'intelligenza artificiale  in campo di elaborazione di dati relativi ad immagini ha prodotto negli ultimi anni risultati estremamente significativi. Sfruttando la natura localizzata delle immagini fornite al modello di machine learning è possibile identificare la presenza di pattern di interesse con una precisione che, nei casi migliori, può arrivare a superare la capacità di analisi umana. Tali tecniche utilizzano estensivamente strumenti analitici noti come reti neurali. Tali strumenti, nella rappresentazione matematica generalizzata sono conosciuti come “universal learner”, si tratta quindi di modelli matematici in grado di approssimare, teoricamente, qualunque funzione ignota. Tali tecniche sono applicate efficacemente a processi di classificazione, ove la funzione da stimare è una complessa struttura matematica che lega l'immagine acquisita alla determinazione della presenza (o assenza) di un determinato oggetto all'interno di questa. Reti neurali trovano applicazione in vari aspetti della frontiera tecnologica: dal semplice riconoscimento del contenuto di un'immagine, alla guida autonoma dei veicoli, alla costruzione di strumenti in grado di “imparare” l'esperienza umana, modellandone il comportamento. In particolare questi ultimi consentono di ottenere, attraverso una fase detta “di addestramento”, un modello di machine learning in grado di comportarsi davanti ad un'immagine in modo analogo ad un esperto nell'estrazione delle informazioni in essa contenuta.

In ambito medico si sono affermati negli ultimi anni numerosi progetti di ricerca applicata in cui tecniche di machine learning (o, più genericamente, di intelligenza artificiale) sono utilizzate efficacemente a supporto dello specialista nella diagnosi, utilizzando estensivamente sistemi quali computed tomography (CT) <sup id="a1">[[1]](#f1)</sup> <sup id="a2">[[2]](#f2)</sup> e la Positron Emission Tomography (PET) <sup id="a3">[[3]](#f3)</sup>.

Recentemente, la ricerca ha focalizzato i propri sforzi sull'utilizzo di immagini radiologiche <sup id="a4">[[4]](#f4)</sup> ed ecografiche <sup id="a5">[[5]](#f5)</sup> <sup id="a6">[[6]](#f6)</sup> che, a differenza delle precedenti tecniche, sono estensivamente adottate a supporto della diagnosi, non richiedendo ingenti investimenti economici nè ponendo rischi per la salute del paziente.

### Screening e diagnosi dei pazienti affetti da COVID-19

A seguito della recente epidemia di nuovo coronavirus, gli ospedali si trovano sottoposti ad una pressione notevole che raggiunge il suo apice nelle fasi di screening di nuovi potenziali infetti e di diagnosi del decorso della patologia per i pazienti ospedalizzati. A ciò si aggiunge l'esigenza sempre crescente di identificare le aree di impatto dell'azione del virus ed il decorso anche di organi che, sebbene non direttamente interessati, subiscono il forte stress indotto dall'infezione da COVID-19. In tale scenario tra le tecniche che sono presenti nei protocolli di diagnosi e monitoraggio degli ospedali figurano: la radiografia polmonare e l'ecografia cardiaca (talvolta anche polmonare). Si tratta di tecniche volte alla determinazione del corretto funzionamento fisiologico degli organi oppure alla stima del danno al fine di poter giungere ad una prognosi.


## Sinossi degli studi

Come illustrato dettagliatamente in seguito, il presente progetto si compone di tre studi complementari. Obiettivo primario degli studi è quello di analizzare l'applicabilità di modelli di machine learning all'analisi di immagini radiologiche ed ecografiche, al fine di costruire un valido supporto alla diagnosi medica, consentendo in questo modo l'estensione delle procedure di screening ad un numero più ampio di pazienti. Conseguentemente, verrebbe snellito il lavoro dei tecnici di radiologia e dei medici specializzati, riducendo i tempi di attesa nei referti e aumentando la capacità diagnostica dei reparti. Obiettivo secondario dello studio è quello di identificare quali altri parametri (di seguito chiamate feature) possano influenzare l'insorgenza o lo sviluppo della patologia. In questo caso si adotterà una strategia di apprendimento supervisionato, attraverso la quale si immettono nella rete un insieme di feature cliniche e demografiche del soggetto che, in modo differente, possono essere legate alla patologia presa in esame, con l'obiettivo che la rete identifichi una regola che associ i dati dei soggetti in ingresso alla presenza o all'assenza della patologia. In questo contesto, invece di far estrarre alla rete i parametri provenienti dalle immagini, si immettono esplicitamente feature aggiuntive in modo che la rete possa apprendere la regola, per distinguere i soggetti nelle due classi, e impiegarla in compiti simili. Conseguenza di ciò è la possibile identificazione, attraverso un modello da una robusta explainability, delle feature (caratteristiche), tra le molteplici raccolte, che possano essere identificative della patologia. Ciò renderebbe possibile la profilazione del soggetto più incline all'insorgenza di COVID-19 e la prevenzione dell'aggravamento della patologia. La realizzabilità di questo terzo studio è supportata dalla raccolta dei dati “Se Disponibili” dei due studi di seguito dettagliati.  Dato il numero ancora fortunatamente contenuto di pazienti affetti da forme gravi di COVID-19 e la numerosità solitamente necessarie per la costruzione di un dataset sufficiente ad addestrare un modello ex-novo, si procederà in questo studio all'utilizzo di immagini pregresse disponibili presso l'ospedale rappresentanti situazioni sane, situazioni con patologie polmonari note (ad esempio polmoniti); e poi si procederà alla specializzazione dei modelli identificati mediante l'utilizzo della immagini disponibili di pazienti COVID-19.

Questo progetto si pone l'obiettivo di condurre due indagini parallele su differenti tipologie di immagini e consolidare poi in una fase posteriore i due modelli identificati al fine di esplicitare le correlazione tra casistiche simili di prognosi.

### Studio 1: Analisi di immagini radiologiche polmonari

#### Obiettivi dello studio

Una prima applicazione di modelli di analisi di immagini è relativa alle radiografie di una popolazione costituita da: pazienti sani / pazienti affetti da patologie polmonari / pazienti identificati (oppure sospetti) COVID-19 con patologie polmonari. Mediante la costruzione di un dataset di immagini ottenute dalla RX e poste in relazione con la diagnosi risultate sarebbe possibile addestrare il modello al riconoscimento di situazioni patologiche di polmoniti gravi. Inoltre, durante il decorso della malattia per i pazienti ospedalizzati, l'utilizzo di tale modello di analisi potrebbe consentire un monitoraggio costante anche in condizioni di disponibilità ridotta di personale, offrendo un feedback a supporto dell'attività diagnostica.

Tale pratica aiuterebbe a fornire tempestivamente un quadro clinico del paziente con conseguente:

- Incremento della possibilità di esito favorevole
- Diminuzione dei tempi di attesa
- Rapida individuazione delle ospedalizzazioni indispensabili rendendo più accessibili le postazioni di terapia intensiva
- Precisione di uno strumento operatore indipendente
- Minore utilizzo di altri metodi diagnostici operatore dipendente (che già scarseggiano sul territorio) con conseguente snellimento e alleggerimento del carico di lavoro dei laboratori di analisi

#### Popolazione dello studio

**Richiesto:** Immagini anonimizzate radiografiche polmonari di pazienti sani / affetti da patologie polmonari / identificati (oppure sospetti) COVID-19 con patologie polmonari in formato DICOM oppure equivalente.

**Se disponibili,** dati di rilevanza clinica relativi ai pazienti quali età, sesso, presenza di patologie pregresse, anamnesi familiare e terapie farmacologiche in atto.

**Se disponibili,** dati relative alla terapie di trattamento COVID-19 somministrate ai pazienti ed esito della prognosi.

#### Periodo dello studio

Marzo 2020 - Dicembre 2020

#### Dati analizzati

Saranno analizzate le RX torace e polmoni di tutti i pazienti disponibili  (sani/affetti da patologie polmonari/identificati -oppure sospetti- COVID-19 con patologie polmonari); unitamente alle informazioni di referto, così da costruire un dataset utile all'addestramento del modello di machine learning.

#### Risultati attesi

Sarà prodotto un modello di classificazione binaria della probabilità di diagnosi favorevole oppure sfavorevole, in base alle immagini fornite al sistema. Le probabilità espresse dal modello di machine learning, potranno essere interpretate come l'intervallo di confidenza di appartenenza ad una delle due classi possibili di diagnosi. I dati verranno analizzati con modelli computazionali di deep neural network con architettura specifica per analizzare le immagini; per l'analisi dei modelli verranno usate metriche specifiche quali:

- Precision & Recall
- F1 score del modello
- valutazione dei threshold nell'ottica di importanza di falsi negativi/falsi positivi
- Curva del Receiver Operating Characteristic (ROC)
- Area under curve (AUC)

Classe espressa e probabilità saranno i due valori che potranno essere integrati nella valutazione diagnostica.

Più nel dettaglio lo studio si pone l'obiettivo di effettuare una prima analisi d'insieme identificando i dati certamente incompatibili con il quadro clinico polmonite da COVID-19, che andranno ospedalizzati e/o trattati in modi e strutture differenti; e i casi dubbi o fortemente compatibili con il quadro clinico in esame, validati con ulteriori metodi diagnostici dalla Struttura Sanitaria e/o dall'ISS.

### Studio 2: Analisi di immagini ecografiche cardiache (e polmonari)

#### Obiettivi dello studio

L'utilizzo di tecniche ecografiche consente l'analisi del comportamento fisiologico dell'organo in esame. In questa fase si procederà ad acquisire dati prodotti da un ecografo in uso presso l'ospedale relativi ad una popolazione costituita da: pazienti sani / pazienti affetti da patologie cardiache / pazienti identificati (oppure sospetti) COVID-19 con patologie cardiache; così da poter costruire un modello di machine learning capace di identificare comportamenti patologici.

La disponibilità di immagini tempo-varianti relative alla fisiologia degli organi cardiaci di pazienti consentirà di addestrare un modello di machine learning in grado di riconoscere con precisione una situazione di comportamento sano oppure patologico del muscolo cardiaco.

Tale pratica aiuterebbe a fornire tempestivamente un quadro clinico del paziente con conseguente:

- Incremento della possibilità di esito favorevole
- Diminuzione dei tempi di attesa
- Rapida individuazione delle ospedalizzazioni indispensabili rendendo più accessibili le postazioni di terapia intensiva
- Precisione di uno strumento operatore indipendente
- Minore utilizzo di altri metodi diagnostici operatore dipendente (che già scarseggiano sul territorio) con conseguente snellimento e alleggerimento del carico di lavoro dei laboratori di analisi

#### Popolazione dello studio

**Richiesto:** Immagini anonimizzate di ecografie cardiache di tutti i pazienti disponibili (pazienti sani / pazienti affetti da patologie cardiache / pazienti identificati -oppure sospetti- COVID-19 con patologie cardiache) in formato DICOM oppure equivalente.

**Se disponibili,** dati di rilevanza clinica relativi ai pazienti quali età, sesso, presenza di patologie pregresse, anamnesi familiare e terapie farmacologiche in atto.

**Se disponibili,** dati relative alla terapie di trattamento COVID-19 somministrate ai pazienti ed esito della prognosi.

#### Periodo dello studio

Marzo 2020 - Dicembre 2020

#### Dati analizzati
Saranno analizzate le immagini ecografiche relative alla funzionalità cardiaca di pazienti sani / pazienti affetti da patologie cardiache / pazienti identificati (oppure sospetti) COVID-19 con patologie cardiache; unitamente alle informazioni di referto, così da costruire un dataset utile all'addestramento del modello di machine learning.

#### Risultati attesi
Sarà prodotto un modello di classificazione binaria della probabilità di diagnosi favorevole oppure sfavorevole, in base alle immagini fornite al sistema. Le probabilità espresse dal modello di machine learning, potranno essere interpretate come l'intervallo di confidenza di appartenenza ad una delle due classi possibili di diagnosi. I dati verranno analizzati con modelli computazionali di deep neural network con architettura specifica per analizzare le immagini; per l'analisi dei modelli verranno usate metriche specifiche quali:

- Precision & Recall
- F1 score del modello
- valutazione dei threshold nell'ottica di importanza di falsi negativi/falsi positivi
- Curva del Receiver Operating Characteristic (ROC)
- Area under curve (AUC)

Classe espressa e probabilità saranno i due valori che potranno essere integrati nella valutazione diagnostica.

Più nel dettaglio lo studio si pone l'obiettivo di effettuare una prima analisi d'insieme identificando i dati certamente incompatibili con il quadro clinico polmonite da COVID-19, che andranno ospedalizzati e/o trattati in modi e strutture differenti; e i casi dubbi o fortemente compatibili con il quadro clinico in esame, che andranno validati con ulteriori metodi diagnostici dalla Struttura Sanitaria e/o dall'ISS.


## Trattamento dei dati personali e dei risultati raggiunti

Si rende noto che il trattamento dei dati avverrà nel rispetto dei principi fissati all'articolo 5 del Regolamento (UE) 2016/679, in forma anonima e per le finalità espressamente dichiarate nel presente documento.

I risultati degli studi condotti andranno a supporto gratuito di tutto il personale medico nazionale e saranno, pertanto, impiegabili in strutture private e pubbliche nei reparti preposti all'identificazione e al trattamento del COVID-19.

I dati verranno salvati in formato DICOM e trattati in una cartella protetta sui server di Neosperience S.p.A.

Neosperience S.p.A e Looptribe S.r.l. si fanno garanti del trattamento e della conservazione dei dati utilizzati e raccolti durante lo studio per un periodo di 2 anni (periodo di riferimento 2020-2021).

## Note
1. <b id="f1">[^](#a1)</b> S. Chen *et al.*, "Automatic Scoring of Multiple Semantic Attributes With Multi-Task Feature Leverage: A Study on Pulmonary Nodules in CT Images," in *IEEE Transactions on Medical Imaging*, vol. 36, no. 3, pp. 802-814, March 2017.
2. <b id="f2">[^](#a2)</b> Y. Chunran, W. Yuanvuan and G. Yi, "Automatic Detection and Segmentation of Lung Nodule on CT Images," *2018 11th International Congress on Image and Signal Processing, BioMedical Engineering and Informatics (CISP-BMEI)*, Beijing, China, 2018 , pp. 1-6.
3. <b id="f3">[^](#a3)</b> G. Nalbantov, A. Dekker, D. De Ruysscher, P. Lambin and EN Smirnov, "The Combination of Clinical, Dose-Related and Imaging Features Helps Predict Radiation-Induced Normal-Tissue Toxicity in Lung-cancer Patients - An in-silico Trial Using Machine Learning Techniques" *2011 10th International Conference on Machine Learning and Applications and Workshops*, Honolulu, HI, 2011, pp. 220-224.
4. <b id="f4">[^](#a4)</b> [https://www.pyimagesearch.com/2020/03/16/detecting-covid-19-in-x-ray-images-with-keras-tensorflow-and-deep-learning/](https://www.pyimagesearch.com/2020/03/16/detecting-covid-19-in-x-ray-images-with-keras-tensorflow-and-deep-learning/)
5. <b id="f5">[^](#a5)</b> Y. Liang, R. He, Y. Li and Z. Wang, "Simultaneous segmentation and classification of breast lesions from ultrasound images using Mask R-CNN," 2019 *IEEE International Ultrasonics Symposium (IUS)*, Glasgow, United Kingdom, 2019, pp. 1470-1472.
6. <b id="f6">[^](#a6)</b> L. Zhang, H. Zhu and T. Yang, "Deep Neural Networks for fatty liver ultrasound images classification," *2019 Chinese Control And Decision Conference (CCDC)*, Nanchang, China, 2019, pp. 4641-4646.
