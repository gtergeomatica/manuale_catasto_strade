# manuale-emergenze-pcge
Manuale del nuovo sistema di Gestione Emergenze della Protezione Civile di Genova


## Descrizione del manuale
Questo manuale è stato redatto sulla base delle *Linee guida di design per i servizi digitali della PA* in formato reStructredText.
[Le linee guida per il design dei servizi digitali della Pubblica Amministrazione](http://design-italia.readthedocs.io/it/stable/index.html) usando stili forniti dal [repository Github release 2019.1](https://github.com/italia/design-linee-guida-docs)
Si tratta di uno strumento di lavoro per la Pubblica Amministrazione che serve ad orientare la progettazione di ambienti digitali fornendo indicazioni relative al *service design*, alla *user research*, al *content design* e alla *user interface*. 

I contenuti del manuale linee guida sono scritti in file .rst e possono essere aggiornati via GitHub. Qui è disponibile una [guida alla sintassi RST](http://docutils.sourceforge.net/docs/user/rst/quickref.html).

Altre risorse per l'editing in formato .rst sono:
- [Editor per il testo](http://rst.ninjs.org/)
- [Editor per le tabelle](http://truben.no/table/)
- [Estensione Chrome per Google spreadsheet](https://chrome.google.com/webstore/detail/markdowntablemaker/cofkbgfmijanlcdooemafafokhhaeold)
- [Altro](http://docutils.sourceforge.net/docs/user/links.html#editors)

## Version control e release della documentazione
Il manuale beneficia del *version control system* di GitHub, per cui esiste una traccia pubblica di tutte le modifiche effettuate e dei relativi autori.


## Stile della documentazione
Le linee guida sono scritte seguendo la [style guide di redazione dei testi pubblici](http://design-italia.readthedocs.io/it/stable/doc/content-design/linguaggio.html). In particolare:
- linguaggio semplice e comprensibile ad un pubblico ampio
- brevità e uso di elenchi
- ricorso ad esempi, meglio se supportati da immagini e link

Il manuale può essere fruito anche in formato .epub e .pdf

## Compilazione della documentazione
I file contenuti in questo repository possono essere modificati sul proprio computer ed essere convertiti in formato HTML per validarne i cambiamenti. È necessario innanzitutto installare il tema di Docs Italia attraverso il seguente comando:

`pip install -r requirements.txt`

Quindi lanciare il comando [Sphinx](http://www.sphinx-doc.org) per validare e generare la documentazione, che sarà consultabile all'indirizzo `./html/index.html`:

`sphinx-build -n -W -T -b html . html`
