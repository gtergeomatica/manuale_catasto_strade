Fruizione dell'interfaccia web
==================================

.. image:: img/interfaccia3.png

L'interfaccia web del nuovo strumento webGIS per la gestione del Catasto Strade è semplice, intuitiva e di facile utilizzo.

E' composta principalmente dall'area di mappa dove vengono visualizzati i dati, due toolbar da cui si accede alle principali funzionalità (es. stampa, editing, strumenti di misura e ricerca, ecc.) o agli strumenti di zoom e pan, l'albero dei layer da cui è possibile accendere/spegnere i singoli layer o l'intero gruppo, che verranno automaticamente visualizzati nell'area di mappa, e un menu da cui selezionare lo sfondo cartografico da visualizzare in area di mappa.

Funzionalità di base
-----------------------------

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/QkhGyZk2Juc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

"""""""""""""""""""""""""""""""""""""""""""""""
    

Ricerca per attributo
-----------------------------

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/_BfZ0XfndTw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
    
"""""""""""""""""""""""""""""""""""""""""""""""

Stampa
-----------------------------

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/DGpLJkqav9Q" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
    
"""""""""""""""""""""""""""""""""""""""""""""""
    
Misura
-----------------------------

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/Rnkttf-Z2nk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

"""""""""""""""""""""""""""""""""""""""""""""""

Tabella attributi e selezione
-----------------------------

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/7kGRwqG4Aqs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

"""""""""""""""""""""""""""""""""""""""""""""""

Editing eventi puntuali e lineari
-----------------------------

Per accedere agli strumenti di editing dello strumento webGIS del Catasto Strade è necessario fare il login con il proprio utente e password. Solo alcuni utenti hanno i permessi necessari per poter procedere alla modifica e aggiunta on line degli eventi puntuali e lineari, quindi solo questi utenti, una volta loggati, potranno visualizzare e utilizzare gli strumenti di editing.

Una volta entrati con il proprio utente, qualora si abbiano i permessi per la modifica on line, saranno disponibili tre pulsanti nella toolbar laterale:

* Edition: consente l'editing sia degli elementi puntuali che di quelli lineari a partire dalla geometria che deve essere disegnata dall'operatore sulla mappa
* Nuovo evento puntuale: consente di aggiungere un nuovo evento puntuale a partire dalla progressiva della strada relativa
* Nuovo evento lineare: consente di aggiungere un nuovo evento lineare a partire dalle progressive iniziale e finale dell'evento

Edition tool
""""""""""""""""""""""""""""""""
E' sufficiente selezionare dal menù a tendina il layer a cui si vuole aggiungere un nuovo evento puntuale o lineare e premere il tasto "Add". Una volta selezionato il layer si potrà procedere a disegnare la geometria sulla mappa.
In caso di eventi puntuali con un solo click del mouse si crea la nuova geometria che potrà essere spostata tenendo premuto il tasto sinistro del mouse. Per quanto riguarda invece gli eventi lineari, cliccando con il mouse sulla mappa si crea la nuova geometria lineare, a ogni click del mouse corrisponde un nuovo vertice della geometria lineare, con il doppio click del mouse viene terminato l'editing della geometria. Modificando un veneto lineare si attivano inoltre alcuni strumenti di editing che permettono di spostare i singoli vertici della geometria lineare, traslarla, ruotarla e modificarla eliminandone una parte.

Sullo strumento webGIS non sono implementate funzioni di snap, in fase di editing non è quindi possibile "agganciarsi" precisamente alle geometrie di route disegnando i nuovi eventi puntuali o lineari. Per ovviare quindi al problema di nuovi eventi non perfettamente collocati sulle route sono stati implementati lato database delle funzioni (triggers) che collocano punti e vertici degli elementi lineari esattamente sulle geometrie di route spostando la geometria disegnata dall'operatore sul punto più vicino della geometria route.

Una volta disegnata la geometria si può procedere alla compilazione della tabella degli attributi relativa alla geometria appena disegnata. A seconda dell'evento che si sta modificando, si possono riempire i diversi campi della tabella inserendo manualmente l'informazione o scegliendola da menù a tendina in caso di colonne con relativa decodifica.
Altre colonne come ad esempio 'data inserimento', 'data aggiornamento' o 'utente ultima modifica' non sono editabili in quanto vengono automaticamente riempite dal database al momento del salvataggio delle modifice. Nel caso ad esempio dell'evento lineare 'ponti e viadotti' è possibile caricare nelle colonne 'scheda vincolo' e 'scheda tecnica' allegati in formato pdf e nella colonna 'Foto' delle immagini semplicemente cliccando sul pulsante che peremette di scegliere il file dal proprio pc.
Qualora le colonne definite obbligatorie lato progetto Qgis non venissero compilate, lo strumento restituirà un errore non permettendo all'operatore di salvare le modifiche.

Terminato il disegno geometrico e compilata la tabella è possibile salvare il nuovo elemento premendo sul pulsante salva. Una volta salvata sarà immediatamente visibile sulla mappa.

Nuovo evento puntuale
""""""""""""""""""""""""""""""""
Con questo strumento è possibile aggiungere nuovi eventi puntuali a partire dalla progressiva su cui si vuole collocare il nuovo evento. Anche in questo caso è sufficiente selezionare il layer da modificare e cliccare sul pulsante 'Compila attributi evento', varrà quindi visualizzato il form relativo alla tabella attributi dell'evento che si sta modificando e anche in questo caso sarà possibile riempire i singoli campi con le stesse modalità descritte per lo strumento precedente (es. compilazione manuale, menù a tendina, ecc.).
Con questo strumento non si deve disegnare la geometria sulla mappa ma è necessario inserire il numero della progressiva su cui si vuole collocare il nuovo evento puntuale e il codice strada.

Nuovo evento puntuale
""""""""""""""""""""""""""""""""
Con questo strumento è possibile aggiungere nuovi eventi lineari a partire dalla progressiva di inizio e fine del evento. Anche in questo caso è sufficiente selezionare il layer da modificare e cliccare sul pulsante 'Compila attributi evento', varrà quindi visualizzato il form relativo alla tabella attributi dell'evento che si sta modificando e anche in questo caso sarà possibile riempire i singoli campi con le stesse modalità descritte per lo strumento precedente (es. compilazione manuale, menù a tendina, ecc.).
Con questo strumento non si deve disegnare la geometria sulla mappa ma è necessario inserire il numero della progressiva di inizio e di fine del nuovo evento lineare e il codice strada e automaticamente verrà creata una nuova geometria lineare con inizio e fine nelle progressive indicate e con l'andamento del tratto di route identificata dal codice strada indicato.

Modifica degli attributi e eliminazione delle geometrie esistenti
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
Per modificare gli attributi di un evento puntuale o lineare esistente è sufficiente identificare l'evento che si vuole modificare dallo strumento tabella attributi o semplicemente cliccandoci sopra con il mouse e cliccare sul tool edit (identificato dall'icona con la matita) che compare nella toolbar alla riga della tabella corrispondente all'evento che si vuole modificare o nella toolbar del popup che si apre cliccando dalla mappa sull'evento. Una volta attivato lo strumento edit per il singolo elemento sarà possibile modificarne gli attributi contenuti nella tabella.

Seguendo la stessa procedura descritta sopra si può anche procedere all'eliminazione di un elemento. In questo caso una volta attivato lo strumento Edit è sufficiente inserire in corrispondenza del campo 'Data eliminazione' la data in cui viene eliminato l'elemento servendosi del calendario che compare cliccando sull'apposito pulsante. Una volta inserita la data di eliminazione e salvate le modifiche, l'evento eliminato non sarà più visualizzato.

NB. Con questa procedura di eliminazione la geometria non viene più visualizzata sia nello strumento webGIS che nel progetto Qgis ma la geometria resta comunque salvata nel data base. Per procedere all'effettiva eliminazione dell'evento (es. in caso di errori grossolani, test o altro) rivolgersi agli amministratori di sistema del Servizio Strade della Provincia di Novara).

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/iz5LkQ-sTRs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
"""""""""""""""""""""""""""""""""""""""""""""""


Ponti e Viadotti - note compilazione form
""""""""""""""""""""""""""""""""""""""""""""""
**Istruzioni**

La tabella attributi del layer del layer "Ponti e Viadotti" è stata redatta seguendo il modello della "Scheda di censimento ponti di Livello 0" del Ministero delle Infrastrutture e della Mobilità Sostenibile  (link: https://www.mit.gov.it/sites/default/files/media/notizia/2020-05/3_All_A_Scheda_censimento_ponti.pdf) . 

Con il fine di semplificare la fruibilità del form di compilazione, questo è stato impostato per essere a "visibilità dinamica" quando si è in presenza campi "dipendenti", cioè che hanno senso di essere compilati solo nel caso sia compilato un altro campo (o più semplicemente spuntato), o nel caso in cui quest'ultimo assuma uno specifico valore. Così facendo, si sono nascosti i "campi dipendenti", i quali vengono visualizzati solo al verificarsi di una particolare condizione sul campo da cui "dipendono". Questo è il caso di specificazioni e note aggiuntive.

Prendendo ad esempio il gruppo "Classi di Conseguenza (Secondo Definizione EN 1990:2002)", come possiamo vedere nelle immagini sotto riportate, il campo "Adeguata giustificazione se inferiore a CC3" compare solo se il campo "Classi di conseguenza" assume i valori "CC1" e "CC2", ma non nel caso assuma valore "CC3".

.. image:: img/note_form1.PNG
  :align: center
  
.. image:: img/note_form2.PNG
  :align: center

Inoltre, per aiutare la compilazione, si sono aggiunti dei tooltip al passaggio del mouse su alcuni campi (contraddistinti da un asterisco nero "*" in fondo al nome), con suggerimenti e note informative. 

.. image:: img/note_form3.PNG
  :align: center

Per poter aggiungere tutte quelle informazioni che non trovano spazio nei campi presenti, si è inserito in fondo al form il campo "note".

È stata necessaria la creazione di una "tabella figlia" per gli allegati, considerando come "tabella padre" il layer "Ponti e Viadotti". Questo è stato fatto principalmente per due motivi: a) natura di alcuni dati, che potrebbero essere multipli per la stessa geometria; b) per una migliore organizzazione del form. 

Non è possibile però popolare la "tabella figlia" mentre si crea la geometria, ma bisogna agire in un secondo momento. Per fare ciò, si seleziona la geometria con il mouse e si clicca "Modifica" (icona con la matita) dal popup.

.. image:: img/note_form5.PNG
  :align: center

Si aprirà il form di compilazione degli attributi, ma questa volta in fondo alla pagina saranno presenti le "tabelle figlie" e attraverso un menù a tendina sarà possibile selezionarle e modificarle!

.. image:: img/note_form4.PNG
   :align: center

**ATTENZIONE**: per cancellare una geometria, sarà prima necessario cancellare i dati nelle "tabelle figlie", se questi sono prsenti.


"""""""""""""""""""""""""""""""""""""""""""""""



Ordinanze 
""""""""""""""""""""""""""""""""""""""""""""""
**Note e istruzioni alla compilazione del form**

Il progetto denominato "Ordinanze", originariamente indicato come "Transitabilità", è stato realizzato per ospitare le ordinanze di limitazione alla viabilità permanenti e temporanee.


.. image:: img/ordinanze_map.PNG
   :align: center

Il progetto è incentrato su un unico layer denominato appunto Ordinanze, la cui stilizzazione categorizzata permette di:


* distinguere tra le varie tipologie di ordinaza (Senso unico Alternato, Limitazione, Chiusura) e tipologia di ostacolo (es. cantiere).
* limitare la visibilità di ordinanze non più in vigore 
* segnalalare la data di inzio della limitazione per ordinanze non ancora in vigore.

Il form di inserimento dati è diviso in tre parti:

* Posizione:  informazioni minime necessarie al funzionamento del CS (Codice strada e Progressiva inizale e finale)
  N.B.: Il layer ordinanze accetta solo gemetrie di tipo lineare, è perciò necessario che la prossiva inziale e finale siano diverse. In caso di Ordinaze che riportino una sola indicazione chiometrica si richiede di inserire come progressiva finale la progressiva indicata + 1.
* Limitazione: dati relativi alla limitazione
* Altre informazioni: Note (campo per annotazioni libere) e Data eliminazione (campo da compilare  per nascondere elementi dalla mappa).

.. image:: img/form_ordinanze.PNG
   :align: center

Tra i dati relativi alla limitazioni, in particolare:

* Numero e data delibera fanno riferimento ai dati identificativi del provvedimento
* Provvedimeto richiede il caricamento obbligatorio di un allegato in formato .pdf
* Tipologia limitazione distingue le limitazioni temporane e permanenti 
* Data entrata in vigore e  data rimozione sono richieste per il calcolo automatico del campo Durata giorni
* Tipologia ostacolo e tipologia ordinanza forniscono dettagli sulla tipologia di limitazione
* Descrizione è un campo libero in cui si consiglia di copiare e incollare l'oggetto del provvedimento in formato pdf
* Revoca, da compilare in caso di revoca del provvedimento prima della Data di rimozione prevista
* Campi relativi a Richesta Esterna (da gestore di sottoservizi) sono dedicati al provvediemnto collegato al provvedimento principale

La tabella sottostante il layer Ordinanze (denominata per ragioni 'storiche' t_transitabilita) è dotata ad una procedura automatica (trigger) che si occupa della gestione delle mail di notifica nei seguenti casi:

* Inserimento nuova ordinanza 
* Modifica ordinanza esistente
* Revoca ordinanza attraverso compilazione di apposito campo Revoca

**ATTENZIONE**: Per ordinanze che riguardano tutte le strade provinciali, ad esempio 'Obbligo di catene', per evitare di appesantire visivamente la mappa si consiglia di creare un pop-up all'apertura della mappa (tramite apposito script javascript per Lizmap). 


""""""""""""""""""""""""""""""""""""""""""""""


Incidenti
""""""""""""""""""""""""""""""""""""""""""""""
**Note**

Il progetto denominato 'Incidenti' è stato realizzato per la mappatura dei dati sugli incidenti stradali comunicati dal servizio TWIST di Regione Piemonte e semplificati dalla Provincia di Novara per l'archiviazione sul CS. 

I dati vengono importati nel GeoDB in apposita tabella (t_incidenti) tramite script python appositamente predisposto da Gter. 
Lo script si occupa di localizzare gli incidenti sulla rete stradale ricostruendo il codice Strada e la progressiva a partire dalle coordinate e viceversa.
Per aggiungere nuovi dati alla tabella bisogna fare richiesta via mail o ticket con allegato un file in formato con le specifiche concordate. Il formato deve essere xlsx e i nomi delle colonne devono corrispondere a quelle definite in fase di primo invio.

Il progetto contine due soli tematismi princiali  

* Incidenti - Layer puntuale in cui ad ogni punto corrisponde un incidente con le relative informazioni rilevate dalle forze dell'ordine. I dati relativi alla localizzazione degli incidenti devono essere validati 
* Mappa di concentrazione  - Le mappe di concentrazione (Heatmap) sono strumenti utili per identificare la densità di punti che rappresentano un certo fenomeno. La mappa di concentrazione degli incidenti ha la finalità di mostrare i punti della rete stradale in cui si verificarano più incidenti (black points o punti neri). Per la valutazione dei punti neri si segnala di considereare che la localizzazione dei punti deve essere prima validata attraverso le opportune maschere di verifica e l'arco temporale dei dati presenti sul CS potrebbe essere non rappresentativa del fenomeno.

.. image:: img/heatmap.PNG
   :align: center

**Validazione geometrica e alfanumerica dei dati**

Il layer Incidenti è può essere modificato attraverso l'apposito pannello Modifica dati. I possibili casi su cui è necessario intervenire sono due:

* Incidente con localizzazione errata - Attivare la modifica tramite il pop-up o la tabella persente nel pannello Dati
* Incidente non localizzato - Per visualizzare gli incidenti non localizati accedere al pannello Dati, dove è presente l'apposita tabella denominata 'Incidenti (dato geometrico assente)'.

**ATTENZIONE**:  In entrambi i casi si richiede di selezionare il campo 'Dati corretti manualmente'.

Il form di inserimento dati è diviso in tre parti:

* Dati Incidente - contenente i dati descrittivi degli incidenti cosi come trasmessi dalle forze dell'ordine (es. data e ora, veicoli coincolti, nnumeor morti e feriti) - i dati qui presenti non sono modificabili
* Correzione Posizione - sezione in cui confrontare i Dati elaborati automaticamente dal Catasto e i Dati originali forniti dalle forze dell'ordine  Eventualmente modificare i dati utili al CS e segnarli come modificati manualmente.
* Dati Catasto - Altre informazioni, Note (campo per annotazioni libere) e Data eliminazione (campo da compilare  per nascondere elementi dalla mappa).

.. image:: img/form_correzione_posizione.PNG
   :align: center
   

""""""""""""""""""""""""""""""""""""""""""""""


Concessioni
""""""""""""""""""""""""""""""""""""""""""""""
**Note**

Il progetto Concessioni, pubblicato nella repository Lizmap denominata 'Ufficio Concessioni' è stato ralizzato allo scopo di visualizzare su CS le istanze di concessioni gestite tramite la piattaforma Istanze-Online (Gis&Web).

Per consentire l'integrazione con il catasto sono state predisposte due tabelle: una per le concessioni puntuali (eventop.t_concessioni_p) e una per le concessioni lineari (eventol.t_concessioni_l) e le rispettive viste.
Gis&Web si occupa della sincronizzazione dei dati secondo modalità e tempistiche volte ad aggionrnare lo stasus delle istanze. Non si tratta però di una replica massiva di dati ma di un trasferimento di alcune info minime quali ad esempio codice strada e progressive, tipo concessione e scadenza. Un campo è destinato a contenere il link per accedere, previa autenticazione, alla pagina del procedimento sul portale Istanze Online.

Le concessioni puntuali e lineari sono visuzlizzate con simbologia categorizzata realizzata sulla base delle tipologie di istanze gestite dalla piattaforma Istanze-Online, cosi come definite al seguente servizio Web:
https://provincianovara.istanze-online.it/iol_strade/resources/getTipoIstanza 
e sulla base di queste importate nel CS in apposita tabella dello schema normativa.

.. image:: img/concessioni.PNG
   :align: center


""""""""""""""""""""""""""""""""""""""""""""""


Progetto correzioni
""""""""""""""""""""""""""""""""""""""""""""""
**Note**

Nella repository privata è presente un progetto denominato nuovo_cs_novara_correzioni.qgs dedicato alle eventuali correzioni da effettuare ai temestismi fondamentali del CS, in particolare Route, Eventi lineati e Progressive.
Che in altri progetti non sono configurati per essere modificati al fine di evitare modifiche accidentali o di utenti non autorizzati.
Nello specifico il progetto è stato predisposto per:

* modifica delle denominazioni convenzionali delle Route 
* modifica delle progressive iniziali e finali delle route e degli elemnti stradali in casi di mancata corrispondenza con i cippi

  **ATTENZIONE** - In caso di correzione progressive ricordarsi di aggiornare parallelamente elementi stradali e route.
               Successivamente è necessario svolgere la seguente procedura per 'rigenenrare' il layer dedicato alle progressive (t_progressive)
               utilizzando i dati presenti nella vista v_progressive che sulla base degli elementi stradali è calcolata:

               1 - effettuare modifiche sulle tabelle route e elementi_stradali
               
               2 - backup tabella statica progressive nello storico  
                     create table storico.t_progressive_[data] as (select * from geometrie.t_progressive tp);
                     
               3 - truncate tabella statica t_progressive
                     truncate geometrie.t_progressive;
      
               4 - rigenerazione progressiva con query da v_progressive        
                     insert into geometrie.t_progressive select * from geometrie.v_progressive;

La procedura descritta sopra va seguita anche in seguito alle cessione, totale o parziale, di una strada.

   
