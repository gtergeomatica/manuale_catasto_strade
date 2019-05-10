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



Eventi puntuali e lineari
---------------------------------------
Tutti gli altri elementi stradali si suddividono in eventi puntuali e lineari.

Nella fattispecie:

Gli **eventi puntuali** attualmente presenti sul CS sono: 


* t_areatraffico
* t_cipporifkm
* t_concessioni
* t_datipatrimoniali
* t_gruppoluminoso
* t_grupposegnale
* t_operecontinuitaidraulica"

Oltre a:

* r_segnalefisico
* r_pubblicita



Gli **eventi lineari** attualmente presenti sul CS sono: 

* t_corpostradale
* t_protezambientecircostante
* t_corsia
* t_protezcorpostradale
* t_cunettemargine
* t_sezionestradale
* t_direzionemarcia
* t_sismicita
* t_dispositivoritenuta
* t_piazzolesosta
* t_sovrappassisottopassi
* t_gallerie
* t_tortuosita
* t_illuminazione
* t_transitabilita
* t_marciapiedi
* t_arginelli
* t_operesostegno
* t_vegetazione
* t_banchine
* t_orografia
* t_centriabitati
* t_passaggilivello
* t_pistaciclabile
* t_pavimentazionecarreggiata
* t_canalifiumi
* t_pontiviadotti
 


