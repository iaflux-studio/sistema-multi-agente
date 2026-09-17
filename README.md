# Architettura multi-agente — iaFlux Studio

**181 agent specializzati, 19 domini, 22 gate con potere di blocco.**

Criterio di conteggio dei gate, scritto il 17 settembre 2026. Un agent conta come gate quando il suo contratto gli dà il potere di fermare una consegna: il nome termina in "-gate" o "-verifier", oppure è uno dei ruoli di controllo elencati per nome nella classificazione della plancia (as-editor, as-compliance, iaflux-art-director, iaflux-quality, qa-verifier, redteam-adversarial, ed-fact-checker, ed-legal-ftc-us, ed-medical-reviewer, str-compliance, cuc-haccp-sicurezza, cuc-allergeni-compliance, cuc-assaggio-qualita, cin-genetica, cin-benessere-etica). Con questo criterio i gate sono 22, e sono marcati uno per uno nella colonna "Gate" del roster: il numero si riconta dal roster, non si crede sulla parola. Fino a oggi il 22 era pubblicato senza il criterio e senza l’elenco. Un secondo criterio, più stretto, conta solo i contratti la cui descrizione dichiara "GATE" o "potere di blocco": con quello i contratti sono 14, e i due elenchi non sono uno dentro l’altro. Tredici nomi coincidono; nove ruoli di controllo bloccano per contratto senza dichiararlo nella prima riga (as-compliance, ed-fact-checker, ed-legal-ftc-us, ed-medical-reviewer, iaflux-art-director, iaflux-quality, qa-verifier, redteam-adversarial, str-compliance); un contratto, as-finance, scrive "GATE" riferendosi ai passi della propria pipeline e non a un potere di blocco su una consegna, e per questo non è fra i 22. È un difetto dei contratti, e sta nella lista delle cose da sistemare. I verdetti emessi dai gate sono nel [registro pubblico dei verdetti](REGISTRO-VERDETTI.md).
Questo è il metodo con cui iaFlux Studio produce il proprio lavoro. Non è un prodotto in
vendita, non è un framework rilasciato: è documentazione di come lavoriamo, pubblicata
perché a chi valuta un fornitore serve poterla leggere.

- **[ARCHITETTURA.md](ARCHITETTURA.md)** — ruoli, routing, gate, catena di verifica,
  dove decide l'umano, gestione degli errori, limiti dichiarati
- **[ROSTER.md](ROSTER.md)** — i 181 contratti, per dominio, generati dai file reali

---

## Perché non basta un modello solo

Un modello generalista sa di fotografia di prodotto, di normativa, di sicurezza elettrica.
Il problema non è la competenza: è la **diluizione**. Quando un unico contesto contiene il
brief, i vincoli di marca, le regole di legge e la richiesta corrente, le istruzioni non
vengono ignorate — vengono *pesate male*. La regola che vale in un caso su cento è la prima
che si perde, ed è esattamente quella che serve.

Un contratto di specializzazione dichiara tre cose: cosa quell'agente possiede, cosa **non**
gli compete, e a chi passa il lavoro. Su 181 contratti, tutti e 181 dichiarano gli strumenti
a cui possono accedere — 88 non hanno alcun accesso di rete.

## Il pezzo che quasi nessuno pubblica: come ce ne accorgiamo quando si rompe

![La plancia del Villaggio degli Agenti](immagini/villaggio-agenti.png)

Ogni agente al lavoro è un robottino nella casa del suo dominio. La riga in alto è la verità
letta dal disco; **il disegno si adegua al numero vero, mai il contrario.** Se anche un solo
agente restasse fuori dal disegno, la plancia lo grida in rosso invece di nasconderlo.

*(Nella schermata le etichette del lavoro sono sostituite con descrizioni generiche: i titoli
veri sono nomi di progetti e di clienti. Struttura, ruoli e numeri sono quelli reali.)*

### I numeri che ci hanno fatto cambiare idea

**La soglia di caduta è 20 minuti, non 12.** Misurata su **1.624 agenti conclusi**: la pausa
più lunga fra due gesti supera 5 minuti nel 19,2% dei casi, 12 minuti nel 6,8%, 20 minuti nel
4,9%, 30 minuti nel 3,9%. A 12 minuti un agente sano su quindici veniva dichiarato morto.

**Su 114 agenti che sembravano caduti, 97 erano stati interrotti da una persona.** Solo 13
stavano davvero lavorando. Guardare l'orologio invece del motivo faceva gridare al lupo
cinque volte su sei.

> **Prima di dichiarare un guasto, leggi come è finita la cosa — non da quanto è ferma.**

**Un errore che vale la pena raccontare.** La prima versione classificava come «falliti» gli
agenti che restituivano meno di 40 caratteri. Su tutto l'archivio, i dieci «falliti» erano
gate che avevano risposto `{'verdict': 'PASS', 'defects': []}` — 34 caratteri, e lavoro
perfetto. *Una regola che premia la verbosità giudica lo stile, non l'opera.* Col criterio
corretto — conta se il risultato *c'è*, non quanto è lungo — l'archivio dà **1.928 rientri e
1.928 esiti, zero a mani vuote**.

### Come si riconosce un agente avvitato

Quattro sonde, tarate in produzione: la stessa chiamata ripetuta almeno quattro volte ·
dodici gesti uguali con non più di tre firme diverse · fermo oltre la soglia · trascrizioni
gemelle, che segnalano uno stallo di più agenti insieme.

## Cosa NON abbiamo

- **Nessun registro di audit cronologico.** Ci sono i verdetti conservati, con il motivo
  scritto e il responsabile della correzione. Non un log datato riga per riga.
- **Il tasso di respingimento dei gate non è misurato in modo continuo.** È registrato cantiere per cantiere nel [registro dei verdetti](REGISTRO-VERDETTI.md), che oggi copre due cantieri: quello del 14 giugno 2026, ricostruito dai registri di lavorazione, e quello del 17 settembre 2026. Per i cantieri precedenti non è ricostruibile.

Sono le due risposte oneste, e sono qui perché una pagina che rivendica controlli senza
dichiarare i propri buchi non è verificabile — è pubblicità.

## Limiti dichiarati

Gli agenti **non sono autonomi**: l'autonomia è deliberatamente limitata e le decisioni che
contano restano a una persona. C'è automazione di processo — code, temporizzatori, ripresa
dagli errori — e c'è la specializzazione del giudizio. Sono due cose diverse, con rischi
diversi, e confonderle è il modo tipico di costruire un'affermazione insostenibile.

---

**iaFlux Studio** — NEW MULTISERVICE S.R.L.S., Caserta
Sito: <https://www.iaflux.it> · Contatto: studio@iaflux.it

Documentazione rilasciata con licenza [CC BY 4.0](LICENSE). I numeri di questo documento sono
stati ricontati il 26 agosto 2026; ogni aggiornamento riporta la data del nuovo conteggio.
