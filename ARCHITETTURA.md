# Architettura multi-agente di iaFlux Studio

**Documentazione tecnica del metodo di produzione interno.**

Titolare: NEW MULTISERVICE S.R.L.S. — Caserta.
Responsabile: Antonio Santoro.
Data di redazione: 24 agosto 2026.
Natura del documento: descrizione di un metodo di lavoro interno, non di un prodotto in vendita. Vedere §11.

Tutti i conteggi riportati sono ricontati alla data di redazione sui contratti effettivamente presenti. Dove un dato non è misurato, il documento lo dichiara invece di stimarlo.

---

## 1. Il principio: perché un solo modello generalista non basta

Il problema non è la competenza del modello. Un modello generalista di ultima generazione sa di fotografia di prodotto, di normativa sulle locazioni brevi, di sicurezza elettrica e di conformità alimentare più di quanto sappia una piccola impresa. Il problema è cosa succede a quella competenza dentro una sessione di lavoro reale.

Tre fallimenti osservati, ricorrenti, indipendenti dal modello:

**Diluizione.** Quando un unico contesto contiene il brief, i vincoli di brand, le regole di legge, le trappole tecniche note e la richiesta corrente, le istruzioni non vengono ignorate: vengono pesate male. La regola più specifica — quella che vale in un solo caso su cento — è esattamente quella che si perde per prima, ed è quella che serve. La regola che dice "in questo dominio un passo va eseguito solo dopo aver verificato l'assenza di tensione" pesa quanto la regola che dice "non usare superlativi".

**Nessuno è incaricato di dire di no.** Un assistente che ha appena prodotto un testo e a cui si chiede se il testo va bene ha un incentivo strutturale a confermare. Non è malafede, è la forma del compito: continuare un lavoro è più naturale che demolirlo. Se produzione e giudizio stanno nella stessa testa, nella stessa conversazione, con la stessa memoria di ciò che è appena costato produrre, il giudizio è compromesso prima di iniziare.

**Nessun formato obbligato per il verdetto.** "Mi sembra buono, forse rivedrei l'illuminazione" non è un verdetto: è una conversazione. Non si può contare, non si può contestare, non blocca niente.

Un contratto di specializzazione risolve queste tre cose e nient'altro. Non rende il modello più intelligente. Fa quattro operazioni concrete:

1. **Perimetro.** Definisce cosa quell'attore tratta e, soprattutto, cosa non tratta. Il perimetro negativo conta più di quello positivo: è ciò che impedisce a un attore di rispondere con sicurezza fuori dalla propria competenza.
2. **Strumenti.** Dichiara esplicitamente quali strumenti quell'attore può usare. Tutti i 181 contratti presenti lo dichiarano; 88 di essi non hanno alcun accesso alla rete. Un attore che deve giudicare un file su disco non ha bisogno di navigare, e non naviga.
3. **Forma del verdetto.** Chi giudica non restituisce un'opinione, restituisce un esito da un insieme chiuso. Esempi in uso: PASS/FAIL su checklist tecnica; ECCELLENTE / OTTIMA / BUONA / RIFARE sulla qualità di uno scatto; APPROVA / APPROVA CON RISERVA / RIFAI su un asset tridimensionale, con il vincolo esplicito che non esiste un quarto esito. Un esito chiuso si può contare e si può contestare.
4. **Owner della correzione.** Ogni verdetto negativo deve indicare la leva di correzione a livello di parametro e chi la deve girare. Un blocco senza leva è un blocco inutile.

C'è una quinta proprietà, meno ovvia e più importante di tutte: **il giudizio si esercita sull'artefatto, non sul racconto dell'artefatto.** Il gate che valuta i render tridimensionali apre e guarda il file; non gli è consentito emettere un verdetto sulla descrizione che qualcun altro ne ha dato. E non emette verdetto affatto se prima non esiste su disco un riferimento approvato con criteri misurabili scritti: senza bersaglio non si giudica. Questa singola regola elimina la classe di errori in cui un sistema di controllo approva una cosa che non ha mai visto.

---

## 2. La mappa dei ruoli

Il sistema ha quattro livelli. La descrizione è per funzione: i nomi interni degli attori non sono rilevanti e non vengono pubblicati.

### Livello 1 — Orchestrazione

Un unico ruolo di orchestrazione sta sopra tutti i domini. Non produce nulla nel merito. Fa quattro cose: instrada la richiesta al dominio competente, decide la priorità quando i domini competono per lo stesso tempo umano, impone l'ordine dei gate, e fa salire al titolare tutto ciò che è una decisione e non un'esecuzione. Un ruolo che orchestra e insieme produce nel merito perde l'indipendenza necessaria a bloccare il proprio lavoro: per questo il confine è esplicito.

### Livello 2 — Domini

I domini attivi alla data di redazione, con il numero di contratti per ciascuno:

| Dominio | Contratti |
|---|---|
| Cucina professionale | 22 |
| Dottrina e testi religiosi | 20 |
| Locazioni brevi e ospitalità | 17 |
| Performance marketing e SEO (Italia/UE) | 16 |
| E-commerce e catalogo (Italia) | 16 |
| Grafica tridimensionale e web interattivo | 13 |
| Pipeline immagini e-commerce | 13 |
| Fotografia e video da smartphone | 13 |
| Sito web proprietario | 12 |
| Cinofilia | 12 |
| Pronto intervento elettrico | 8 |
| Contenuti canale salute (mercato USA) | 6 |
| Editoriale salute e benessere (mercato USA) | 5 |
| Strategia di marketing (mercato USA) | 3 |
| Ruoli trasversali (verifica, refutazione, finanza, dati, memoria) | 5 |
| **Totale** | **181** |

Un ulteriore dominio è congelato e i suoi contratti non sono in uso.

Cinquantaquattro contratti su 181 — cucina, cinofilia, testi religiosi — non hanno alcuna destinazione commerciale. Sono dichiarati qui deliberatamente, per una ragione tecnica: sono la prova che l'impianto di controllo non è tarato su un solo settore. Il gate che blocca un accoppiamento canino geneticamente pericoloso, il gate che blocca una preparazione alimentare fuori catena del freddo e il gate che blocca un passo di lavoro elettrico prima della verifica di assenza tensione sono la stessa struttura applicata a tre rischi diversi. Un impianto che regge solo dove è nato non è un impianto, è un caso fortunato.

### Livello 3 — Specialisti

Dentro ogni dominio, ruoli verticali che producono: chi scrive, chi implementa, chi elabora immagini, chi imposta il tracciamento, chi progetta l'illuminazione di una scena. Sono la maggioranza numerica del sistema. Nessuno di loro ha potere di approvazione sul proprio lavoro.

### Livello 4 — Verificatori e gate

Due funzioni distinte, spesso confuse:

- **Verificatore funzionale**: accerta che il deliverable faccia ciò che dichiara. Checklist di completezza, esecuzione di test, confronto tra ciò che il testo afferma e l'evidenza disponibile, conferma oggettiva del "fatto" invece di quella dichiarata.
- **Gate**: ha potere di blocco su una categoria di rischio. Non migliora il deliverable, decide se esce.

Sopra entrambi, un ruolo di refutazione adversariale il cui mandato è cercare i modi in cui la cosa fallisce (§5).

---

## 3. Il routing: come si decide chi prende la richiesta

Il routing non è una scelta di opportunità, è un insieme di regole scritte. Le principali:

**Per dominio.** La richiesta va al dominio competente, non a quello che l'ha trattata l'ultima volta. Un agente non lavora fuori dal proprio dominio: se una richiesta di marketing tocca un contenuto sanitario, il marketing la cede al dominio editoriale sanitario e non la tratta lui.

**Per natura dell'artefatto, non per somiglianza superficiale.** Una immagine fotorealistica ha tre origini possibili e tre domini diversi: se è generata da un modello va alla pipeline immagini; se è calcolata a partire da una scena tridimensionale costruita da noi va al dominio 3D; se è una ripresa reale va al dominio fotografico. Tre percorsi, tre insiemi di difetti tipici, tre gate diversi. Trattarle come "immagini" è il modo più rapido per applicare il controllo sbagliato.

**Regole dure che non dipendono dal dominio di partenza:**

- Qualsiasi testo in italiano destinato al pubblico passa dal gate editoriale italiano, chiunque l'abbia scritto.
- Qualsiasi affermazione riguardante la salute umana passa dal revisore clinico. La salute animale non passa da lì: ha un dominio proprio, e la sovrapposizione tra i due è essa stessa un errore da prevenire.
- Nessuna spesa pubblicitaria parte prima della verifica preliminare sul tracciamento: se non si può misurare l'esito, non si spende.
- Nel dominio del pronto intervento elettrico l'ordine dei due gate è fisso e non si inverte: prima il gate sul gesto che può ferire una persona, poi il gate su ciò che arriva al cliente. Un testo perfetto che descrive una manovra pericolosa è un fallimento peggiore di una manovra sicura descritta male.
- Qualsiasi consolidamento finanziario passa dal ruolo di controllo finanziario; qualsiasi lettura di dati che attraversa più basi dati passa dal ruolo dati.

**Regola di proporzione.** Il sistema non lancia 181 attori su ogni richiesta: sarebbe costoso e più lento del lavoro stesso. Il default è una risposta diretta o un solo attore. La catena completa si attiva su richiesta esplicita del titolare oppure automaticamente quando il compito tocca una di queste cinque categorie: macchine che si muovono o alimentano, obblighi di legge, minori, stati persistenti (dati che restano scritti da qualche parte), difetti silenziosi (errori che non producono alcun messaggio di errore).

Per i lavori piccoli vale una regola intermedia, adottata dopo una misurazione, non per principio: **due gate invece di quattro**, scelti in base a ciò che il lavoro tocca — usabilità più editoriale se tocca interfaccia e microcopy; verifica funzionale più refutazione se tocca logica, dati o stati; editoriale più verifica funzionale se è solo testo pubblico. La misura che ha prodotto la regola è nel §10.

---

## 4. I gate con potere di blocco

Un gate è definito da tre proprietà: una categoria di rischio, un esito da un insieme chiuso, e la capacità di impedire l'uscita del deliverable. Le categorie presidiate:

**Sicurezza fisica di una persona.** Nel dominio elettrico, un gate presidia la catena di sezionamento (sezionare, bloccare, verificare l'assenza di tensione), la regola per cui l'invasività di una procedura non può mai decrescere lungo la sequenza, e le fonti che possono rialimentare un quadro già sezionato — gruppi di continuità, impianti fotovoltaici, generatori. Nel dominio alimentare, un gate presidia analisi dei pericoli, punti critici di controllo, limiti critici, catena del freddo, allergeni ed etichettatura.

**Salute umana.** Per i contenuti sanitari destinati al pubblico la catena è di quattro attori distinti: revisione clinica (accuratezza, controindicazioni, gruppi a rischio, grading dell'evidenza — sperimentazione controllata contro studio osservazionale contro plausibilità meccanicistica), verifica dei fatti, revisione editoriale, revisione legale sulle regole pubblicitarie del mercato di destinazione. Quattro attori perché sono quattro errori diversi: un'affermazione può essere clinicamente corretta e pubblicitariamente illecita, o formalmente ineccepibile e clinicamente pericolosa per un sottogruppo.

**Salute e benessere animale.** Un gate blocca gli accoppiamenti geneticamente a rischio. È il caso più netto di blocco non negoziabile: nessun argomento commerciale, estetico o di richiesta del cliente può superarlo, perché l'esito del rischio è la sordità o la cecità di un animale che non ha voce nella trattativa.

**Persone in situazione di fragilità.** Un gate si attiva quando dietro una domanda c'è una persona reale in lutto, in crisi, in colpa, in malattia o con sofferenza psichica, e impedisce che un attore automatico si sostituisca a una persona competente. È il gate meno visibile e quello che protegge dal danno peggiore.

**Obblighi normativi e contrattuali.** Conformità delle locazioni brevi (codici identificativi, adempimenti verso le autorità, obblighi informativi, base giuridica per il contatto commerciale, minimizzazione dei dati); conformità e-commerce; perimetro abilitativo nel dominio tecnico, cioè il divieto di dichiarare di eseguire lavori per i quali non si hanno i titoli.

**Verità delle fonti e grado di autorità.** Nel dominio dei testi, due gate separati: uno apre i testi originali e verifica che la citazione dica davvero ciò che si sostiene; l'altro verifica che sia dichiarato il *grado di autorità* di quanto affermato — se è una posizione definita, una posizione autorevole ma non definitiva, una valutazione prudenziale o un'opinione libera. La separazione è tecnicamente interessante fuori dal suo dominio: una citazione può essere esatta e usata per sostenere una cosa che non sostiene. Sono due errori distinti e servono due controlli distinti.

**Qualità percepita e vendibilità.** Verdetti a esiti chiusi su scatti fotografici e su asset tridimensionali, sempre con leva di correzione e responsabile del fix. Con una limitazione dichiarata al §6: il giudizio finale sul gusto non è delegato a un attore automatico.

**Accessibilità.** Un gate presidia la conformità del sito proprietario agli standard di accessibilità.

**Dati.** Nessuna spesa pubblicitaria senza verifica preliminare della strumentazione di misura.

### Cosa succede quando un gate blocca

Il deliverable non esce. Non esce nemmeno se è finito, impaginato, e già costato tempo: questa è la condizione che rende il gate qualcosa di più di una formalità (l'esempio del §8 è esattamente questo caso).

Il verdetto negativo deve contenere: il motivo, la leva di correzione a livello di parametro, il responsabile del fix. Il lavoro rientra dal punto in cui è stato bloccato, non dall'inizio: rifare tutto è il modo più efficace per rendere odioso un controllo e farlo aggirare.

### Chi può scavalcare un gate

**Nessun attore automatico può scavalcare un altro attore automatico.** Non esiste gerarchia tra pari e non esiste "riprovare finché passa": ripresentare lo stesso artefatto senza modifiche non è un ricorso.

**Il titolare può decidere di procedere comunque**, con due condizioni operative: la motivazione è scritta e i criteri di abbandono sono fissati prima. Il precedente in uso viene da un pattern di decisione applicato agli investimenti, dove il verdetto contrario del gruppo di revisione può essere superato dal titolare solo con razionale documentato e criteri di uscita.

**Ma la scavalcabilità non è uniforme, e conviene dirlo con precisione.** Ci sono due tipi di gate:

- Gate il cui oggetto è un **giudizio interno** (questo è abbastanza buono? questa priorità è giusta?). Superabile: è una valutazione, e l'ultima valutazione spetta a una persona.
- Gate il cui oggetto è un **obbligo esterno** — una norma, un rischio fisico, la salute di qualcuno. Qui "scavalcare" è una parola che inganna: la decisione interna non tocca l'obbligo. Superare il gate non elimina il rischio, lo trasferisce a una persona fisica che ne risponde. Il sistema può registrare quella scelta; non può renderla sicura.

---

## 5. La catena di verifica

L'ordine è: **specialista → implementatore → verificatore funzionale → refutazione adversariale.** L'ordine non è estetico.

**Prima si conferma che funziona, poi si cerca come si rompe.** Cercare i modi di rottura di una cosa che non è ancora completa produce rumore: si trovano difetti che sarebbero spariti col completamento. Il verificatore funzionale accerta lo stato "fatto" in modo oggettivo: esegue, confronta i claim con l'evidenza, riporta gli esiti reali con l'output effettivo, compreso quello dei test falliti.

**Poi entra la refutazione, con un mandato invertito.** L'attore adversariale non ha il compito di dire se il lavoro è buono. Ha il compito di **refutare**: default scettico, si assume che il deliverable sia difettoso finché non è provato il contrario, e si cercano edge case, assunzioni mai verificate, affermazioni non supportate, punti singoli di rottura, e i modi concreti in cui la decisione fallisce.

La ragione per cui il mandato è invertito è strutturale, non caratteriale. Un verificatore valutato sulla correttezza delle sue conferme converge sul confermare: confermare è a costo zero e non produce conflitto. Un attore il cui unico output valido è una lista di difetti non ha una via d'uscita silenziosa: se non trova niente deve dichiararlo esplicitamente, e quella è un'affermazione forte, contestabile e attribuibile. Si sposta il costo dal dire "no" al dire "sì".

Questo è anche il motivo per cui il ruolo di refutazione è separato dal ruolo che orchestra e da quello che produce, e ha uno dei contratti a cui è imposto il modello di ragionamento più costoso: 32 contratti su 181 fissano esplicitamente il modello superiore, 19 fissano quello standard, i restanti 130 ereditano l'impostazione della sessione. La regola di allocazione è: modello superiore sui ruoli di giudizio, modello standard sull'esecuzione.

**Il costo della catena è reale e lo misuriamo.** §10.

---

## 6. Human-in-the-loop: cosa non decide mai un attore automatico

**Se una cosa è bella, o abbastanza buona da uscire.** È la regola più controintuitiva del sistema e la più solida. Il lavoro finito viene consegnato da guardare, e il verdetto lo dà una persona. Non viene preceduto da un'approvazione automatica, e non si comunica alla persona un verdetto già formato: sarebbe un ancoraggio. La regola è stata rafforzata dopo un caso concreto — un gate estetico lanciato su un lotto di immagini è stato fermato a metà dal titolare, perché stava producendo un giudizio che non gli serviva e che rischiava di sostituire il suo. La distinzione che ne è uscita, e che regge:

> Verifica di **fatto** (funziona? l'affermazione è supportata? è conforme?) → attori automatici, con potere di blocco.
> Giudizio di **valore** (è bello? vende? va bene così?) → persona, sempre, senza eccezioni.

Gli attori che **producono** restano pienamente in uso. È chi **giudica il gusto** che non è delegato.

**Cosa resta sempre alla persona, per regola operativa:**

- La pubblicazione. Nessun contenuto raggiunge un canale pubblico come effetto automatico di un'approvazione interna.
- L'impegno di denaro: attivazione di campagne a pagamento, acquisti, prezzi, sconti, impegni verso clienti.
- Gli adempimenti che richiedono l'identità del titolare presso una pubblica amministrazione. Non è una scelta: è tecnicamente impossibile delegarli, e nell'esempio del §8 è esattamente il punto in cui il sistema si ferma.
- L'accettazione di un rischio residuo dopo un blocco.
- Le comunicazioni verso terzi identificati.
- La scelta di quali progetti vivono e quali si chiudono.

**Onestà sul confinamento.** Queste sono regole operative scritte nei contratti, non un confinamento tecnico. Tutti i 181 contratti dichiarano accesso a lettura, scrittura ed esecuzione locale. La differenziazione tecnica effettiva e verificabile riguarda l'accesso alla rete: 88 contratti non ne hanno alcuno, 54 hanno la sola ricerca, 37 hanno ricerca e recupero diretto di risorse, 2 il solo recupero. La distribuzione segue la funzione: 16 contratti su 16 nel dominio del marketing hanno accesso alla rete, 0 su 12 nel dominio del sito proprietario, 3 su 13 nella pipeline immagini. Chiunque valuti questo sistema deve sapere che il perimetro è **contrattuale**, e che un confinamento più forte sarebbe un miglioramento reale, non una formalità.

---

## 7. Gestione degli errori e delle contraddizioni

**Quando due attori si contraddicono**, la contraddizione non si risolve per anzianità, per livello gerarchico né dando ragione all'ultimo che ha parlato. Si risolve risalendo alla fonte: vince chi porta un riferimento verificabile e apribile. Se nessuno dei due ce l'ha, la questione non viene risolta dal sistema: sale al titolare come decisione, dichiarata come decisione e non come verità accertata. La differenza è importante, perché una decisione presa in assenza di prova va registrata come tale e riaperta quando la prova arriva.

**Quando un attore sbaglia**, il deliverable torna al punto di blocco con la leva di correzione indicata. L'errore singolo non è interessante. È interessante l'errore *ricorrente*: quando lo stesso tipo di errore si ripresenta, non si corregge il singolo caso — si scrive una regola. La base di conoscenza operativa conta alla data di redazione **76 trappole tecniche** catalogate, **24 regole di metodo** e **12 pattern** riusabili, tutte nate da incidenti reali e non da revisione teorica. Ogni voce risponde a tre domande: cos'è successo, perché ha ingannato chi guardava, come si applica la correzione.

**Le classi di errore che catalogare ha effettivamente cambiato:**

- Un controllo che restituisce zero risultati per una differenza di maiuscole, e che viene letto come "nessun problema trovato". Un controllo che tace è peggio di uno che sbaglia: sembra una conferma.
- Una correzione applicata a uno solo di due documenti gemelli. L'altro non invecchia visibilmente: continua a sembrare valido mentre è già falso.
- Una suite di test costruita escludendo, senza accorgersene, proprio il caso che falliva.
- Controlli di build verdi per il motivo sbagliato: passano, ma non stanno misurando ciò che si crede.
- Un vincolo apparentemente troppo severo interpretato come difetto da allentare, quando è la difesa che stava prevenendo un bug reale. La regola derivata: prima di ammorbidire un vincolo, cercare il bug che quel vincolo previene.
- Credito esaurito su un servizio esterno: incidente completamente muto, nessun errore, solo assenza di risultato.
- Uno stato di risposta positivo da un servizio che non prova affatto che ciò che sta dietro sia vivo.
- Un campo lasciato vuoto che pubblica un valore predefinito sbagliato invece di fallire.

**Distinzione operativa:** un attore silenzioso non è un attore fallito. Esiste una regola specifica su come si distinguono i due casi, perché trattare il silenzio come fallimento produce riavvii inutili e trattarlo come normalità produce attese infinite.

**Ciò che il sistema non fa da solo:** non si autocorregge in modo permanente. Le regole nella base di conoscenza le scrive una persona, dopo l'incidente. Non c'è nessun meccanismo di apprendimento automatico dai propri errori, e chiunque affermi il contrario di un sistema simile va guardato con attenzione.

---

## 8. Come ci accorgiamo quando qualcosa si rompe

Un'architettura che non si osserva è una dichiarazione d'intenti. Questa si osserva da una
plancia che legge lo stato dal disco e mostra ogni agente al lavoro nella casa del suo
dominio — con i suoi numeri, il suo ultimo gesto e il tempo da cui è fermo.
La schermata e i numeri di esercizio sono nel [README](README.md).

### Il lavoro non esce da un posto solo

È il primo errore che abbiamo fatto: guardare una cartella sola e credere di vedere tutto.
Gli agenti lasciano traccia in tre posti diversi, e due erano invisibili.

1. I sotto-agenti di un flusso orchestrato, che hanno un registro di chi è nato e chi ha
   consegnato.
2. Gli agenti lanciati uno a uno, che **quel registro non ce l'hanno**: se hanno finito si
   capisce dalla forma dell'ultima battuta — chi ha finito chiude parlando, chi sta ancora
   lavorando chiude con una chiamata a uno strumento rimasta in attesa di risposta.
3. Le sessioni di lavoro stesse, dove la parte maggiore del lavoro viene svolta prima di
   qualsiasi delega. Erano le più visibili sullo schermo e le uniche assenti dal conteggio.

### La distinzione che cambia tutto: fermo non vuol dire morto

Un agente che non ha mai scritto un risultato **non è caduto**: nella grande maggioranza dei
casi è stato interrotto da una persona. Misurato sull'archivio: di 114 agenti mai chiusi, 97
avevano come ultima riga un'interruzione. Solo 13 stavano davvero lavorando.

La conseguenza è nel codice: si legge **come è finita** la cosa prima di ogni altro giudizio;
se è un'interruzione lo stato è «fermato da te», gravità zero, nessun allarme. Senza questa
distinzione una sorveglianza grida al lupo cinque volte su sei — e chi la guarda smette di
crederle, che è il modo in cui uno strumento di controllo muore.

Vale anche il caso opposto: dopo un arresto voluto, gli agenti fermati sembrano stalli. Si
considera caduto solo chi è fermo **mentre un collega dello stesso cantiere sta ancora
scrivendo**; altrimenti il cantiere è semplicemente chiuso.

### Cosa non dice l'orologio

L'ora di modifica di una cartella non dice se il lavoro è vivo: cambia quando si creano o si
cancellano file, non quando una trascrizione cresce. Un cantiere con un agente fermo da mezz'ora
e un collega che aveva scritto dodici secondi prima risultava «vecchio» e spariva dalla plancia.
Difetto silenzioso, nessun errore. Si guardano i file uno per uno.

## 9. Strumenti, tracciabilità e dati personali

### Strumenti

Ogni contratto dichiara esplicitamente il proprio insieme di strumenti: 181 su 181. Nessun contratto contiene credenziali. Il riferimento ai servizi esterni avviene per nome di variabile d'ambiente e i valori vivono fuori dai contratti — verificato con ricerca mirata su tutti i contratti alla data di redazione.

Ripartizione dell'accesso alla rete, che è la differenziazione tecnicamente effettiva:

| Accesso | Contratti |
|---|---|
| Nessun accesso alla rete | 88 |
| Sola ricerca web | 54 |
| Ricerca web e recupero diretto di risorse | 37 |
| Solo recupero diretto di risorse | 2 |

Il limite di questo modello è dichiarato al §6: il perimetro è contrattuale, non è una sandbox.

### Tracciabilità: cosa esiste e cosa no

**Esiste:**
- La trascrizione integrale di ogni sessione di lavoro, conservata localmente, da cui è ricostruibile a posteriori quale attore è intervenuto, su cosa e con quale esito.
- Una base di conoscenza curata, con voci datate e un ruolo dedicato alla sua igiene: consolidamento, rimozione dei fatti superati, conversione delle date relative in assolute. È il presidio contro la classe di errore più insidiosa, il documento che invecchia sembrando ancora valido.
- Per i flussi automatici di produzione, registrazione a livello di base dati con stato per singolo lavoro, costo per lavoro, storico dei cambi di stato e registro degli errori.

**Non esiste, e va detto:**
- Un **registro di audit strutturato e interrogabile a livello di singolo attore**: quale gate è stato eseguito, quando, su quale artefatto, con quale verdetto e quale motivazione. Oggi la ricostruzione richiede la lettura delle trascrizioni. È possibile, ma non è un audit trail. È la lacuna più seria dell'impianto di governance ed è la prima cosa da costruire.
- Un **registro unico dei gate**. Sette contratti portano la parola "gate" nel nome, altri esercitano potere di blocco senza averla. Dal 17 settembre 2026 l'elenco esiste: il criterio di conteggio è nel README e i 22 gate sono marcati uno per uno nella colonna "Gate" del ROSTER. Resta il difetto a monte: nove di quei contratti non dichiarano il potere di blocco nella propria descrizione, quindi il sistema non può ancora dimostrarlo leggendo solo il contratto.
- Versionamento uniforme: non tutti i progetti sono su un sistema di controllo di versione.

### Dati personali

Cosa vale operativamente:

- I dati che entrano nella lavorazione sono quelli necessari al lavoro commissionato, trattati su macchina del titolare e sui servizi dichiarati al cliente.
- Il gate di conformità del dominio locazioni brevi presidia esplicitamente, oltre alla normativa di settore, la base giuridica del contatto commerciale verso imprese, la minimizzazione dei dati raccolti e i limiti alla raccolta automatica da fonti web.
- I contratti degli attori non contengono dati personali di clienti: contengono metodo.

Punti aperti, dichiarati:

- Dove sono definiti termini di conservazione dei dati, in almeno un caso **non esiste ancora un processo che li applichi automaticamente**: la regola è scritta, l'esecutore no.
- Per alcune piattaforme di messaggistica di terze parti utilizzate per assistenti conversazionali non è disponibile un accordo sul trattamento adeguato a un uso professionale. Dove ce ne siamo accorti l'abbiamo registrato come rischio noto con mitigazioni operative, non come problema risolto.
- L'assenza del registro di audit descritta sopra è essa stessa un limite di conformità, non solo di ingegneria: rende più oneroso dimostrare cosa è stato fatto su un dato.

---

## 10. Metriche: cosa misuriamo e cosa non misuriamo

Questa sezione è deliberatamente povera di numeri. La regola interna è che una pagina senza numeri è preferibile a una con numeri non supportati.

### Misurato

- **Costo unitario di elaborazione** nel flusso automatico di immagini: media nell'ordine di due centesimi di dollaro per immagine, con registrazione del costo per singolo lavoro su base dati. Il costo è tracciato per lavoro, non stimato a posteriori.
- **Esiti terminali distinti** nel flusso automatico: ogni lavorazione termina in uno stato esplicito — riuscita, da rivedere, fallita — con coda, tentativi e recupero automatico dei lavori bloccati. Gli stati sono contabili per costruzione.
- **Costo in tempo della catena di controllo su un intervento piccolo**: un intervento minore su un sito cliente — spostamento di un elemento e aggiunta di un pannello informativo — è costato **59 minuti, di cui 35 di lavoro effettivo** e il resto di verifica. Questa misura ha prodotto una regola: sui lavori piccoli si applicano due gate invece di quattro (§3). È l'unica misura che abbiamo del costo del nostro stesso metodo, ed è un solo punto: non è una serie.
- **Dimensione della base di conoscenza operativa**: 76 trappole tecniche, 24 regole di metodo, 12 pattern, alla data di redazione.
- **Estensione del parco contratti nel tempo**: le date di modifica dei contratti vanno dal 15 aprile 2026 alla data di redazione, con aggiornamenti nell'ultima settimana. Il sistema è in manutenzione continua, non è stato scritto una volta.

### Previsto contrattualmente ma non consolidato

Il contratto del gate di qualità fotografica prevede il **tasso di RIFARE per lotto come indicatore di processo**. È dichiarato nel contratto; non esiste una serie storica consolidata. Va considerato un requisito scritto, non una misura disponibile.

### Non misurato oggi — e va iniziato a registrare

Elenco esplicito, perché un fornitore che pubblica un'architettura di controllo senza dire quali indicatori non ha sta descrivendo un desiderio:

1. **Tasso di respingimento per gate**: quante volte ciascun gate blocca, su quante esecuzioni. Senza questo non sappiamo se un gate stia lavorando o solo timbrando.
2. **Tasso di falsi positivi**: quanti blocchi vengono poi ribaltati da una persona. Un gate che blocca troppo viene aggirato, ed è il modo tipico in cui questi impianti muoiono.
3. **Tempo dal blocco alla correzione**, per categoria.
4. **Resa della refutazione adversariale**: quante volte trova un difetto che la verifica funzionale aveva lasciato passare. È la metrica che giustifica l'esistenza stessa di quel ruolo, ed è quella che non abbiamo.
5. **Deliverable usciti saltando la catena**, e con quale esito.
6. **Costo in tempo e in risorse di calcolo della catena per classe di lavoro**, oltre al singolo punto misurato sopra.
7. **Difetti sfuggiti a tutti i controlli** e trovati dal cliente o dal mercato.

L'ultimo è il più importante e il più assente. **Senza la misura dei difetti sfuggiti, tutte le altre metriche sono autoreferenziali**: descrivono quanto il sistema è occupato, non quanto è efficace. È dichiarato qui perché è vero, non perché suoni bene.

---

## 11. I limiti dichiarati: cosa questo sistema non è

**Non è un prodotto software.** Non si vende, non si installa presso il cliente, non ha licenza, prezzo, versioni né supporto. È il metodo con cui iaFlux Studio produce il lavoro che consegna. Il cliente compra il risultato e la sua verificabilità, non il sistema.

**Non è un framework rilasciato.** Non c'è un runtime, un pacchetto, un'interfaccia da integrare. Non c'è niente da importare, e non è previsto che ci sia.

**Non è un sistema autonomo.** Nessun attore si attiva da solo su un evento esterno, nessuno prende decisioni non presidiate. L'automazione non presidiata esiste a un livello diverso e più basso — code, temporizzatori, recupero dei lavori bloccati nella pipeline di produzione — ed è automazione di processo, non agenti che decidono. La distinzione non è retorica: sono due cose con rischi completamente diversi e conviene non confonderle.

**Il perimetro degli attori è contrattuale, non tecnico.** Ripetuto qui perché è il limite più rilevante per chiunque valuti la robustezza dell'impianto. Il confinamento effettivo riguarda l'accesso alla rete; il resto è disciplina scritta.

**C'è un buco noto e non ancora chiuso.** Un audit interno su un catalogo tecnico ha rilevato che **nessun controllo trasversale verifica che un numero scritto in un testo esista nella fonte**. Peggio: la coppia produzione-revisione era ottimizzata al contrario, perché il ruolo di scrittura era istruito a includere sempre un dato numerico e il ruolo di revisione validava la presenza del dato e la correttezza della lingua, non la corrispondenza alla fonte. Un valore tecnico errato su una scheda prodotto è passato con esito positivo. Su un prodotto tecnico il numero *è* il prodotto: un valore sbagliato non è un refuso, è un difetto di conformità con conseguenze contrattuali. Oggi la mitigazione è procedurale — non fidarsi del controllo editoriale sui contenuti numerici e risalire alla fonte — e questo significa che dipende dalla disciplina, non dalla struttura. Non è chiuso.

**Il giudizio estetico non è delegato, e non lo sarà.** Chi cerca un sistema che decida al posto suo se una cosa è bella non troverà qui quello che cerca.

**Non c'è certificazione.** Nessun ente ha validato questo impianto. Nessuna delle affermazioni di questa pagina è stata verificata da un terzo. Quello che offriamo è che siano verificabili: i conteggi sono ricontabili, il caso del §8 è raccontato con il suo esito negativo, e le lacune sono elencate al §9 e al §10.

**I numeri di questa pagina invecchiano.** Un documento interno riportava 175 contratti quando erano 181: un conteggio scritto una volta e mai più ricontato. È stato corretto ricontando. Ogni aggiornamento di questa pagina richiede lo stesso ricontrollo, e la data di redazione in testa serve a quello.

**Il numero di agenti non è una metrica di qualità.** Centottantuno non significa niente per un cliente. Si può costruire un parco di duecento contratti che non blocca mai niente, e sarebbe teatro. L'unica cosa che conta è che su ogni consegna esista qualcuno il cui unico compito è dire di no, che abbia il potere di farlo, e che qualche volta lo faccia davvero — anche quando costa, anche quando a essere bloccato è chi ha costruito il sistema.

---
