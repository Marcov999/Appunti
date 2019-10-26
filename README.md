# Appunti

Appunti di Geometria 2, scritti e mantenuti da Marco Vergamini, Alessio
Marchetti, Luigi Traino.

Ogni riferimento a persone esistenti o a fatti realmente accaduti è puramente
casuale.

## Inroduzione
Questi appunti sono basati sul corso di Geometria 2 tenuto dai professori
Roberto Frigerio e Jacopo Gandini nell'anno accademico 2019/2020. Sono dati per
buoni i contenuti dei corsi del primo anno, in particolare Analisi 1 e
Geometria 1. Verranno omesse o soltanto hintate le dimostrazioni più semplici,
ma si consiglia comunque di provare a svolgerle per conto proprio. Ogni tanto
sarà commesso qualche abuso di notazione, facendo comunque in modo che il
significato sia reso chiaro dal contesto. Inoltre, la notazione verrà
alleggerita man mano, per evitare inutili ripetizioni e appesantimenti nella
lettura. Si ricorda anche che questi appunti sono scritti a più mani, non sempre
subito dopo le lezioni, non sempre con appunti completi, ecc... Spesso saranno
rivisti, verranno aggiunte cose che mancavano perché c'era poco tempo (o
voglia... potrebbero mancare argomenti più o meno marginali... insomma, non è un
libro di testo per il corso, ma vuole essere un valido supporto per aiutare gli
studenti che seguono il corso. Speriamo di essere riusciti in questo intento.

## Come compilare
Come noto, per via delle refs bisogna compilare i files Latex un numero
variabile di volte. Inoltre la compilazione produce un mucchio di file ausiliari
utili solo al compilatore che tendono ad intasare la working directory. Pertanto
ho scritto un  piccolo Makefile che si prende cura di tutte queste cose. Per
ottenere il pdf assicurarsi di essere con il terminale nella cartella
`Geometria2` e dare il comando `make`. I files ausiliari si troveranno nella
cartella `Geometria2/build`.

## Come utilizzare git
Git organizza la storia della repo con delle "istantanee" organizzate in un
albero. Ogni istantanea &egrave; chiamata _commit_. Per indicare a git quali
files includere nell'istantanea, utilizzare il comando
```
git add FILE1 FILE2 ...
```
Per dirgli di includere tutti i file, usare
```
git add *
```
**Nota**: anche i files modificati dall'ultimo commit vanno aggiunti nuovamente.
Per vedere lo stato della repo (in particolare cosa &egrave; successo
dall'ultimo commit) dare
```
git status
```
Per committare le modifiche, utlilizzare
```
git commit -m "MESSAGGIO"
```
Dove il messaggio &egrave; una piccola descrizione di cosa si &egrave; fatto nel
commit. Per caricare tutto sul server, utilizzare
```
git push
```
Per scaricare le modifiche fatte dagli altri:
```
git fetch
```

### Cose che sperabilmente non servono
Se due persone lavorano in contemporanea caricare potrebbe diventare un
problema. Per ovviare al problema utilizzare `git merge`. Dato che
verosimilmente si tratta di problematiche rare per il lavoro che stiamo facendo,
consiglio di usare Google in caso di estremo pericolo.

Per fare delle modifiche "pericolose" potrebbe essere un'idea furba spostarsi su un nuovo branch. In linea di massima i comandi sono:
```
// Creare un nuovo branch
git checkout -b nuovo_branch

// Spostarsi su un branch esistente
git checkout nuovo_branch

// Modifiche ai files
git add *
git commit -m "Ho fatto del lavoro sul nuovo branch"

// Ricongiungersi al ramo principale
git checkout master
git merge nuovo_branch

// verosimilmente l'ultimo comando dara` dei problemi. Auguri.
```

## Altre note

### I blocchi
I blocchi sono elementi numerati. In genere corrispondo a un teorema,
definizione, esempio ecc. Per utilizzare un blocco utilizzare la sintassi
```
\begin{block}[NOME]
    % contenuto del blocco
\end{block}
```
dove `NOME` indica il tipo di blocco. Si hanno dei blocchi predefiniti
(cio&egrave; con il `NOME` settato). Li riassumo nella tabella:

|blocco|`NOME`|
|---|---|
|`thm`|Teorema|
|`lm`|Lemma|
|`defn`|Definizione|
|`prop`|Proposizione|
|`cor`|Corollario|
|`ex`|Esempio|
|`exc`|Esercizio|
|`sol`|Soluzione|
|`oss`|Osservazione|
|`ftt`|Fatto|

Si utilizzano con la sintassi del tipo:
```
\begin{defn}
    % la definizione
\end{defn}
```

Inoltre, usando la sintassi del blocco, utilizzando `block*` si ottengono
blocchi non numerati.

### Ordine e coerenza nella repo
- Preferire l'inizio di un nuovo paragrafo (inserendo una linea vuota nel
    sorgente) all'andata a capo semplice con il `\\`.
- Cercare di inquadrare tutti i contenuti importanti all'interno di un blocco.
- Creare un nuovo file nella cartella `Geometria2/secs` per ogni nuova
    subsection. Ricordarsi di includere le varie sezioni nel `main.tex` con il
    comando `\input{secs/FILE.tex}`. I titoli non vanno inseriti nei file
    separati ma direttamente nel main.
- Per le formule che prendono una linea intera, preferire i delimitatori
    `\[` e `\]` ai `$$`. _Nota: alcune parti devono ancora essere "bonificate"._
- Mantenere (per la leggibilit&agrave;) una larghezza del testo di 80 caratteri.
- All'interno del testo, preferire il comando `\dots` al posto dei punti di
    sospensione (`...`).
- Committare spesso.
- Tenere circa aggiornato questo README.
- *SCRIVERE CIO` CHE SI FA SUL todo.txt*.

### Diagrammi commutativi cheat sheet
__TODO__ inserire sezione.

### Simboli strani e customizzati cheat sheet
__TODO__ inserire sezione.
