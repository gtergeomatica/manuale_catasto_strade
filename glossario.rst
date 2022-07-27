Glossario
==================

Geodatabase
--------------------------------------
Si tatta di un sistema informatico per l'organizzazione e memorizzazione dati (database) dotato di una sua estensione geografica (geo) 
che permette la memorizzazione dei dati secondo gli opportuni sistemi di coordinate (CRS: *Coordinate Reference System*). 
E' normalmente  costituito da tre componenti:

* **spaziale**: indica la posizione
* **semantica**: indica gli attributi
* **relazionale**: indica le relazioni



GIS
--------------------------------------
*Geographic Information System* secondo l'acronimo inglese o *Sistema Informativo Territoriale* (SIT) usando l'acronimo italiano è definito come un insieme organizzato di procedure o metodi matematici, risorse umane e risorse materiali (dati e software) utilizzati per raccogliere,
aggiornare, condividere, elaborare e visualizzare informazioni utili alla pianificazione, progettazione e controllo del territorio e 
delle sue infrastrutture.



Elementi stradali, route e giunzioni
-------------------------------------
Si tatta degli elementi alla base del Catasto Strade di livello 2:

* Il layer *giunzioni* contiene i punti che uniscono due elementi_stradali e sono essenzialmente di due tipi: 
	- confine comunale
	- altro che racchiude tutte le giunzioni fra due diverse strade provinciali (caratterizzate da un diverso cod_strada) presenti sul CS
* Il layer *elementi_stradali* contiene le geometrie degli assi stradali (linee) che partono da una giunzione e arrivano ad un'altra e sono individuate da una prog_ini e da una prog_fin.
* Infine il layer *route* contiene le geometrie degli assi stradali unite fra di loro per ogni strada sulla base del cod_strada

A questi layer di base sono affiancati:

* il layer *progressive* che contine le indicazioni chilometriche calcolate sulla base delle progressive amministrative iniziali e finali degli elementi stradali con visualizzazione variabile in funzione della scala

* le viste elementi Stradali virtuali e elementi strdali completi: due viste create allo scopo di verficare la presenza di interruzioni tra gli elementi stradali che costituiscono le route. Idealmente, a parità di codice strada gli elementi stradali dovrebbero essere contigui tale per cui è possibile ricavare da questi una Linestring. Nei casi in cui sono presenti interruzioni importanti la creazione della Linestring non è possibile e si ottiene necessariamente una geometria di tipo Multilinestring. Ciò si traduce nel difficoltà di creazione eveniti lineari in corrispondenza di interruzioni per i problemi derivanti dalla gestione della procedura di segmentazione dinamica che consente di ottenere dalle coordinate le progressive ( vedi trigger snap_geometry_line).
Elementi Stradali virtuali rappresentano degli elementi stradali fittizi e quindi detti virtuali, generati in corrispondenza delle interruzioni tragli elementi stradali di una stessa route.
Elementi stradali completi contiene la totalità  degli elementi stradali 'reali' e degli elemetni stradali virtuali, è la vista che può essere utilizzata al posto degli elementi_stradali per ottenere un grafo stradale senza interruzioni.




Eventi puntuali e lineari
---------------------------------------
Tutti gli altri elementi stradali si suddividono in eventi puntuali e lineari.

Nella fattispecie:

Gli **eventi puntuali** attualmente presenti sul CS sono: 


* t_accessi (Accessi)
* t_attrlineeelettriche (Attraversamento linee elettriche)
* t_baypass (Bypass)
* t_casecantoniere (Case cantoniere)
* t_cippi (Cippi)
* t_illuminazionepuntuale (Illuminazione puntuale)
* t_impiantipubblicitati (Impianti pubblicitari)
* t_operecontinuitaidraulica (Opere di continuità idraulica)
* t_rotatorie (Rotatorie)
* t_segnaleticaorizzontale (Segnaletica orizzontale)
* t_segnaleticaverticaale (Segnaletica verticale)
* t_sezionestradale (Sezione stradale)
* t_sicurezzastradale (Sicurezza stradale)
* t_verde (Verde)

Oltre a:

* r_segnaleticacomponenti (Segnaletica verticale - Componenti)



Gli **eventi lineari** attualmente presenti sul CS sono: 

* t_arginelli (Arginelli)
* t_carreggiate (Tratte omogenee - Carreggiate)
* t_centriabitati (Centri abitati)
* t_corpo (Corpo stradale)
* t_corsie (Tratte omogenee - Corsie)
* t_cunette (Cunette)
* t_delimitazionetratta (Delimitazione tratte)
* t_elementononcensito (Elementi non  censiti)
* t_fosso (Fossi)
* t_galleriesovrappassi (Gallerie e sovrappassi)
* t_illuminazionelineare (Illuminazione lineare)
* t_intersezioni (Intersezioni)
* t_lineeelettricheparallele (Linee elettriche parallele)
* t_marciapiedi (Marciapiedi)
* t_pavimentazione (Pavimentazione)
* t_pertinenzediservizio (Pertinenze di servizio)
* t_piazzole (Piazzole)
* t_pisteciclabili (Piste ciclabili)
* t_pontiviadottisottopassi (Ponti)
* t_protezioneambiente (Dispositivi di protenzione ambientale)
* t_ritenuta (Dispositivi di ritenuta)
* t_sezione (Sezione)
* t_tracciati (Tracciati)
* t_trattideclassificati (Tratti declassificati)

Oltre a:

* r_schedecontrollo (Ponti - Schede di controllo)
* r_schedecontrollo_img (Ponti - Schede di controllo - Immagini )
* r_schedeponte (Ponti - Schede ponte)
 


