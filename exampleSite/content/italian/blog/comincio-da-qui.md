---
title: "Comincio da qui"
date: 2020-05-12T12:14:34+06:00
image: "https://res.cloudinary.com/dario-caricchio/image/upload/w_1000,h_731,c_fill,f_auto,g_center/v1621548322/slider/slider-1_csdco1.jpg"
tags: ["design","web","development"]
description: "This is meta description."
draft: false
---

# Indice
Questo sembra funzionare:
```markdown
# Table of Contents
1. [Example](#example)
2. [Example2](#example2)
3. [Third Example](#third-example)
4. [Fourth Example](#fourth-examplehttpwwwfourthexamplecom)


## Example
## Example2
## Third Example
## [Fourth Example](http://www.fourthexample.com) 
```

Questo no:
```markdown
# Table of contents
1. [Introduction](#introduction)
2. [Some paragraph](#paragraph1)
    1. [Sub paragraph](#subparagraph1)
3. [Another paragraph](#paragraph2)

## This is the introduction <a name="introduction"></a>
Some introduction text, formatted in heading 2 style

## Some paragraph <a name="paragraph1"></a>
The first paragraph text

### Sub paragraph <a name="subparagraph1"></a>
This is a sub paragraph, formatted in heading 3 style

## Another paragraph <a name="paragraph2"></a>
The second paragraph text
```

# "On the line"
Inizio questo primo articolo con una citazione del film "[Gli stagisti](https://it.wikipedia.org/wiki/Gli_stagisti)", un film che parla anche di tecnologia ma soprattutto di umanità, di voglia di mettersi in gioco, di tentare e fallire così tante volte fino a raggiungere il successo sperato e, si, anche del lato oscuro del mondo tech (seppur sempre con toni scherzosi).
Non a caso ho scelto proprio questo titolo, il film in questione è un ottimo spunto di riflessione con cui iniziare a scrivere l'introduzione di questo primo articolo. E a sua volta mi ispira a fare altre citazioni. Ma per il momento le terrò per me, di certo non mancheranno le occasioni per menzionarle. Tuttavia vorrei lasciare a tutti gli intrepidi che ogni giorno si mettono in gioco e che affrontano le sfide e le difficoltà che la vita gli pone davanti le seguenti parole:

<blockquote class="blockquote">
<p class="mb-0">"Il successo non è mai definitivo, il fallimento non è mai fatale; è il coraggio di continuare che conta."</p>
<p class="mb-0">"Successo è passare da un fallimento all’altro senza perdere l’entusiasmo."</p>
<p class="mb-0">~ Winston Churchill</p>
</blockquote>

Piccola digressione. Per chi non mi conoscesse, ricordo moltissime citazioni e spesso le uso come risposte ai quiz sui social o come "Hello World" più avanzato nello sviluppo di applicazioni d'esempio, in modo da avere uno scopo quando inizio ad esplorare le potenzialità di una nuova tecnologia semplicemente di un campo che finora risultava inesplorato per la mia persona. Chi è nel campo Big Data capirà subito non appena dirò che è un po' come la _Word Count_.

Non sono uno sviluppatore web, o perlomeno non è il campo in cui lavoro al momento della scrittura di questo articolo; tuttavia credo che ogni occasione per uscire dalla propria _comfort zone_ ed imparare qualcosa di nuovo possa farci crescere, ci renda migliori e soprattutto sviluppa le nostre capacità, come ad esempio la logica.
Inoltre mi balenava l'idea di scrivere da me un sito portfolio personale da un po' di tempo. Avevo già fatto diversi tentativi in passato usando varie tecnologie, più o meno complicate. Beh, il termine "complicato" è qualcosa di relativo dopotutto: forse l'approccio che ho utilizzato per l'attuale implementazione potrebbe risultare più complicato rispetto a dei CMS già _out of the box_, come ad esempio Wordpress o Drupal. Per cui approfondirò nelle prossime sezioni l'argomento, elencato le mie personali motivazioni e le caratteristiche degli strumenti che ho utilizzato per creare dariocaricchio.ml.

## Motivazioni
Innanzitutto credo molto nella condivisione della conoscenza e del sapere. Il mondo dell'informatica è in continua evoluzione, c'è una lacuna enorme nelle conoscenze e spesso basta davvero poco per imparare molto. D'altronde molte delle conoscenze che ho, per fortuna o per difetto, le ho apprese attraverso pubblicazioni scientifiche, documentazioni e articoli come questo più che dai libri (che ciononostante sono e rimangono una delle fonti primarie del sapere informatico ed ingegneristico, non fraintendetemi).
Inoltre ritengo che l'open-source aiuti la crescita, sia del sistema informatico che delle persone che ci accedono o che contribuiscono. Per questo motivo, è possibile visionare il codice sorgente dei miei "esperimenti" sul mio profilo [GitHub](https://github.com/dariocaricchio). Soltanto durante il tempo libero mi dedico a questi _side projects_, per cui potrebbe non essere tutto in ordine (vi ho avvisati in anticipo).
Infine questo progetto, oltre ad essere una motivazione per spingermi ad imparare nuovi concetti, doveva essere qualcosa di _semplice_, economico e soprattutto flessibile, poiché non sapevo se avrei potuto mantenerlo costantemente. In parole povere: qualcosa di cui me ne sarei potuto anche dimenticare per diverso tempo una volta realizzato se necessario. Questa motivazione deriva proprio dalle mie esperienze passate, in cui l'uso di sistemi avanzati non mi garantivano la flessibilità (passato diverso tempo, facevo prima a ricominciare da capo piuttosto che aggiustare il sito per andare incontro ai nuovi aggiornamenti/cambiamenti) oppure non garantivano l'economicità della soluzione (soluzioni semi-gestite che però costavano di più, per un semplice sito web portfolio che mi facesse da _vetrina_ sul mondo non mi sembrava un grande affare).
Per quanto concerne i framework per lo sviluppo di applicazioni web, avevo un certo "pregiudizio": non avendo molto tempo ed essendo sempre proiettato mentalmente verso i due campi del Big Data e del Machine Learning, la ritenevo un impresa un po' ardua da realizzare sia in termini di costi temporali e sia come forza lavoro da dover dedicare. Finché, in una delle mie numerose ricerche, non sono giunto a conoscenza di **Hugo** e, in generale, delle tecniche **JAMStack**.
Nei prossimi capitoli parlerò proprio di questi strumenti e di questi concetti, ma, come detto in precedenza, non essendo un web developer o simile eviterò di approfondire molto, favorendo invece la semplicità.
Quindi, senza ulteriore indugio, andiamo ad approfondire i concetti che compongono questa guida e soprattutto questi strumenti.


# Come ho creato il mio portfolio web

## Requisiti
Suppongo che chiunque si appresti a leggere questa seconda parte dell'articolo non sia un novizio dell'informatica e che almeno i concetti e gli strumenti base siano stati già acquisiti. In particolare mi riferisco a:
- **HTML** e **CSS** (quest'ultimo senza entrare nel dettaglio)
- l'uso di un qualsiasi linguaggio di programmazione; basta conoscere gli statement principali che solitamente sono comuni alla maggior parte di essi, come l'**if-else** ad esempio. A scanso di equivoci, si evidenzia che verrà utilizato **JavaScript**
- familiarità con la definizione, la struttura e la logica dei così detti "file di configurazione", i quali di solito utilizzano **YAML**, **JSON** o **TOML**
- conoscere un minimo **Markdown**
- concetti base di rete come **hosting**, **DNS**, **SSL** e gestione del dominio
- saper usare almeno le funzioni basi di **Git**, come creare un repository, fare operazioni di pull, di commit e di push et similia.

Questi sono i principali requisiti, non bisogna essere esperti di tutti questi concetti poiché, come vedremo, non sono niente di invalicabile; tutt'al più sarà necessario spendere un po' più tempo su ciò che non si conosce, esattamente come ho fatto anch'io. Se stai leggendo fin qui, d'altronde, è perché vuoi imparare qualcosa che ancora non sai. 😉

## Tecnologie e visione d'insieme
Il mio sito è un sito <ins>**statico**</ins> generato con [Hugo](https://gohugo.io/), ospitato su [Netlify](http://netlify.com/) e basato sulle tecniche [JAMStack](https://jamstack.org/).
Vediamo in breve come verranno adoperati questi strumenti da una prospettiva un po' più alta. Hugo è un framework per la creazione di siti statici. Basterà prendere un template HTML modificato per Hugo e caricarlo su di un vostro repository. Una volta personalizzato e modificato opportunamente il template per andare incontro al proprio gusto personale, si effettuerà l'operazione di pubblicazione del sito attraverso la piattaforma Netlify.

A questo punto potreste domandarvi "_ma perché usare proprio questo approccio?_".
Domanda lecita, in fin dei conti; la risposta è molto semplice: perché fa al caso mio, viste le [motivazioni](#motivazioni) di cui sopra. Se vi ritrovate nella stessa casistica, sono sicuro che sarà la giusta soluzione anche per voi.
Vediamo un po' più nel dettaglio cosa mi ha spinto a scegliere questo approccio.

Hugo ed i template permettono uno speed-up della creazione del proprio sito importante, implementando anche i meccanismi di basi dei siti statici, fornendo una documentazione chiara da consultare e rendendo lo sviluppo molto più abbordabile. Inoltre il sito sarà responsive, il ché non è qualcosa da sottovalutare.
A parte un investimento iniziale, contribuire al sito richiede poco tempo, giusto quello che riesco a dedicare.

Netlify copre tutta la parte relativo non solo al Deploy, ma anche all'hosting, alla gestione del dominio e alla sicurezza, gestendo lo scambio dei certificati per l'instaurazione di connessioni sicure e cifrate tramite [Let's Encrypt](https://letsencrypt.org/), una Certificate Authority no-profit, automaticamente ed in modo del tutto trasparente all'utente.

Tutto questo non ha alcun costo. Infatti l'hosting su Netlify è gratuito fino a 100GB al mese.
Se proprio si vuole usare un dominio personalizzato (poiché Netlify utilizzera il proprio sottodominio, come ad esempio https://example.netlify.app/ ), il costo rimane comunque irrisorio poiché trattasi in genere di cifre come 10€ all'anno, meno di 1€ al mese.
Però alla fine dell'articolo metterò un capitolo in cui mostrerò come avere un dominio personalizzato con alcuni suffissi liberi senza alcun costo aggiuntivo.

Riassumendo:
- flessibile (poco tempo)
- economico (addirittura a costo zero)
- mantenibile nel tempo (interventi quando possibile)
- facile e veloce da realizzare

## Sviluppare in locale
Come detto nella visione d'insieme, bisogna in primis partire da un template. Potete trovarli effettuando una banale ricerca sul web. [Hugo Themes](https://themes.gohugo.io/) e [JamStack Themes](https://jamstackthemes.dev/) ne sono un esempio. Una volta scelto, mettetelo sul vostro repository (spesso basta una banale fork) e clonatelo sulla vostra macchina.
Bisogna installare Hugo per poter sottomettere i comandi. [Qui](https://gohugo.io/getting-started/installing/) ci sono le istruzioni per farlo in qualsiasi modo, ma essendo il sottoscritto un utilizzatore della shell e della linea di comando, personalmente l'ho installato con il gestore di pacchetti.

Vi consiglio di fare attenzione al file README e alla licenza che troverete all'interno del template che utilizzerete. Leggeteli bene, in particolare il primo poiché ci sono le istruzioni, i comandi e qualche suggerimento che vi permetteranno di prendere confidenza col template stesso.

Uno dei punti focali di hugo è il comando `hugo server`. Spesso affiancato da parametri come `--themesDir <path>` (dove `<path>` è il path in cui è specificato il proprio tema), questo permette di lanciare il "server" locale di hugo per fare l'operazione di building del sito e poterlo visionare attraverso un qualsiasi browser andando, di default, all'indirizzo `localhost:1313`. Suggerisco di usare Firefox poiché con Chrome e la nuova versione di Edge (basata su Chromium) viene effettuata un meccanismo di caching della pagina che non permette di sfruttare la funzionalità di hugo server di ri-buildare le pagine che sono state modificate in tempo reale mentre il server era già attivo, fornendo di fatto un anteprima di come sarà il sito.

Una volta effettuate le modifiche, bisogna semplicemente fare commit e push di quest'ultime sul proprio branch. Se come me siete i soli a contribuire al vostro progetto, allora potreste banalmente lavorare semplicemente sul master, tuttavia suggerisco di usare altri branch in modo da usare il master come versione di riferimento per la fase di deploy; quindi soltanto quando avrete una nuova versione "completa" del sito la mergerete nel master, innescando così anche il deploy della nuova versione stessa.
Si, perché (seppur non l'abbia ancora detto) su Netlify basterà specificare il repository ed il branch da cui prendere la versione del sito da pubblicare ed automaticamente (secondo le configurazioni nel repository che solitamente sono già pronte con il template e le impostazioni che avrete usato su questa piattaforma) questa verrà buildata e deployata (come si suol dire in gergo). Quindi vi bastera committare e pushare/mergiare sul repository le vostre modifiche e tutto il meccanismo partità in automatico.

Una cosa è bene che venga specificata. Non mettete le immagini che userete nel sito all'interno del repository (nonostante spesso nei template, forse per comodità, ciò avviene). Ci sono diversi servizi, alcuni gratuiti entro certi limiti come avviene per Netlify, che vi permettono di caricare le vostre immagini e di indirizzarle attraverso un link all'interno del codice del vostro sito. Quello che uso io è [Cloudinary](https://cloudinary.com/): semplicemente caricate le vostre immagini, copiate il link ed incollate dove vi serve.
Potete anche usare dei tag di ottimizzazione, ad esempio:
> https://res.cloudinary.com/dario-caricchio/image/upload/w_auto,c_scale,f_auto/v1621548322/slider/slider-1_csdco1.jpg

`w_auto,c_scale,f_auto` infatti sono stati aggiunti all'URL in modo che le API di Cloudinary possano fornire delle immagini con altezza, scala e fattore automatico.

### CMS
Gli interventi detti finora sono _manuali_ e per le mie esigenze ed il mio modo di lavorare è più che adatto. Tuttavia vorrei fare presente che è possibile anche usare un CMS come [Forestry ](https://forestry.io/). Ce ne sono anche altri, ma come detto non li utilizzo personalmente.
Si usano per scrivere in Markdown tramite un editor online, per caricare le immagini (che forse è la parte più noiosa) e committare direttamente sul repository.

Un altro consiglio, soprattutto per i neofiti, è quello di usare [Stackbit](https://www.stackbit.com/). In questo modo, tramite la piattaforma online, è possibile selezionare il proprio tema, il framework generatore del sito statico (come Hugo, ad esempio), così detto Headless CMS (come Forestry) ed il Provider Git su cui è presente il vostro repository.

"E perché non l'hai usato anche tu?", è questo che vi state domandando. Beh, semplicemente perché, ribadisco, volevo imparare qualcosa di nuovo e mettere le mani in pasta è il modo migliore che io conosca. Ho iniziato a fare il tutto in modo "manuale" e una volta scoperto queste altre possibilità mi sono reso conto che non facevano per me ed ho continuato per la mia strada, ma per chi ha davanti una carriera che può sfruttare anche questi strumenti, per chi vuole approfondire queste tematiche o semplicemente per chi si trova meglio con tool simili allora è bene fare una menzione, indirizzare e lasciare al lettore la facoltà di scegliere in funzione delle proprie esigenze.

## Deploy
TODO


## BONUS
Come ottenere un dominio personalizzato (o quasi) gratis con .tk e myfrenom.




[Farsi un sito (come il mio) a zero spese mensili - YouTube](https://www.youtube.com/watch?v=O_IViNjCApU)
Indice: 
- Perché una masterclass
- Hugo, Github e Netlify 
- Panoramica del sito
- Quanto spendo per l'hosting
- Hugo in localhost e Git
- Cloudinary per le immagini 
- Consigli per iniziare (Stackbit e YAMStack) 
- Vantaggi di questo metodo 
-  Gestione dominio e SSL 
- Codice del sito
- Markdown e nuove pagine
- Generare le pagine statiche
- CSS, JS e webfont
- Json della sezione libri
- Pubblicazione di una recensione
- Codice sconto per il corso di Boolean




TODO:
- Aggiornare immagine
- Scrivere Skeleton
- Tutorial Hugo