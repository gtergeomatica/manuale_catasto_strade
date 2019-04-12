Funzionalità di amministrazione del Catasto Strade
====================================================

Le funzionalità di creazione/gestione di eventi sono possibili solo per il profili di
tipo 1 e 2 (*Amministratore di sistema* e *Responsabile Centrale PC*).




I progetti QGIS
------------------------

Il principio fondamentale su cui si basa il sistema informativo del catasto strade è la possibilità di gestire tramite l'utilizzo di Qgis desktop la pubblicazione e la visualizzazione dei dati sul web. Questo può essere fatto in due modi:

* impostando opportunamente le proprietà del progetto Qgis e dei singoli layer da pubblicare;
* impostando opportunatamente le diverse opzioni proposte dal plugin Lizmap.

A seconda dei diversi contenuti che si vogliono visualizzare on-line, sono stati creati diversi progetti Qgis ognuno corrispondente a una diversa interfaccia web. Qualora si volesse creare un nuovo progetto e quindi la corrispondente visualizzazione web, sarà sufficiente creare appunto un nuovo progetto Qgis, caricare i dati da pubblicare al suo interno, impostare le proprietà del progetto e dei singoli layer e infine utilizzare il plugin Lizmap per procedere alla pubblicazione. In automatico verrà creata la pagina web corrispondente al progetto con tutte le caratteristiche definite tramite le proprietà di Qgis e il plugin Lizmap.
Un eventuale nuovo progetto deve essere salvato all'interno della cartella NuovoCS dove sono state create due cartelle:

* progetti_pubblici: i progetti salvati in questa cartella e configurati per la pubblicazione su web sono accessibili a chiunque accedendo all'interfaccia web;
* progetti_privati: i progetti salvati in questa cartella e configurati per la pubblicazione su web sono accessibili solo attraverso opportune password.

Come già accennato, molte delle caratteristiche dell'interfaccia web possono essere definite impostando le proprietà del progetto e/o dei singoli layer direttamente da Qgis

Proprietà del progetto
"""""""""""""""""""""""""""""""""""""""""""
In Qgis dal menù Progetto selezionare la voce Proprietà, si aprirà una finestra di dialogo da cui selezionare la voce 'Qgis server'

Da qui si possono impostare diverse proprietà che verranno poi trasferite alinterfaccia web salvando il progetto stesso. In particolare da qui è possibile definire:

* Capabilities del Servizio:
.. image:: img/service_cap.png
Si tratta di informazioni generali come il titolo dello strumento webGIS che può essere diverso da quello del file di progetto Qgis, i dati dell'ente e della persona di riferimento, una breve descrizione, ecc.
Le informazioni inserite in questa finestra di dialogo saranno trasferite allo strumento web una volta salvato il progetto e sranno visibili cliccando sul pulsante 'Informazioni' nella toolbar alla sinistra dello schermo.
.. image:: img/service_cap_web.png

* Capabilities dei servizi WMS:
.. image:: img/wms_cap.png
Da qui è possibile impostare l'estensione della mappa da visualizzare on line, i codici EPSG supportati dai servizi WMS, escludere determinati layer e layout di stampa dalla visualizzazione web, ecc.
* Capabilities dei servizi WMTS:
.. image:: img/wmts_cap.png
Da qui si abilita l'interrogazione dei diversi layer che verranno pubblicati e visualizzati visualizzati nello strumento webGIS. Spuntando le caselle in corrispondenza del progetto tutti i layer caricati al suo interno saranno interrogabili lato web. Agendo invece sui singoli layer sarà invece possibile definire quali rendere interrogabili sul web e quali no.
* Capabilities dei servizi WFS:
.. image:: img/wfs_cap.png
Da qui si abilita la pubblicazione dei singoli layer come servizi WFS che è necessaria per poter utilizzare alcuni tools propri dello strumento webGIS come l'editing on line, sia delle geometrie che delle tabelle associate, e la ricerca.
Anche in questo caso è possibile definire quali layer pubblicare come WFS e quali no. Spuntando le diverse caselle in corrispondenza di ogni layer si abilita la pubblicazione come WFS, la modifica, inserimento e rimozione delle geometrie e relative informazioni alfanumeriche.

Proprietà del layer
"""""""""""""""""""""""""""""""""""""""""""
Una volta caricati i dati all'interno del progetto Qgis, siano essi vettoriali, raster, altri servizi WMS, ecc., vengono visualizzati all'interno del pannello Layers (a sinistra).
L'ordine con cui vengono disposti i diversi layer all'interno del pannello Layers determina l'ordine con cui saranno disposti i diversi layer nell'albero dei layer dell'interfaccia web (si veda ima sotto.) Inoltre l'ordine dei layer determina anche l'ordine di visualizzazione in caso di sovrapposizione delle geometrie. In Qgis infatti, il primo layer dall'alto è quello che si sovrappone a tutti gli altri che seguono. 
.. image:: img/nuovo_evento.PNG

Nell'esempio dell'immagine sopra, il layer bla si sovrappone infatti al layer blabla e blablabla.
Clickando con il tasto destro del mouse su un singolo layer si accede a un menù dal quale selezionare la voce Proprietà, si aprirà una finestra da cui sara possibile impostare le caratteristtiche principali del layer (es. stile di rappresentazione, limiti di scala nella visualizzazione, caratteristiche della tabella associata per i dati vettoriali, ecc.) che verranno immediatamente trasferite alinterfaccia web salvando il progetto stesso e utilizzando il plugin lizmap.

In particolare dalle proprietà del layer è possibile definire:

* Stile:
* Etichette:
* Proprietà dei campi della tabella:
* Tipologia dei campi della tabella:
* Visualizzazione del layer dipendente dalla scala:

Il plugin lizmap
-----------------------------------





Lizmap web client
---------------------------------------------------


aaa



Aggiunta gruppi e utenti
"""""""""""""""""""""""""""""""""""""""""""




Aggiunta/modifica repository
"""""""""""""""""""""""""""""""""""""""""""


