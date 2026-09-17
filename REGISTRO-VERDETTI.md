# Registro pubblico dei verdetti dei gate

Registro pubblico dei verdetti dei gate. Una riga per ogni cantiere in cui un gate ha emesso un verdetto su una consegna, con la data, cosa è stato giudicato, quale gate, quanti testi o consegne sono stati respinti sul totale e a quale giro. Si aggiorna quando c’è un verdetto nuovo, non a scadenza fissa: una riga in meno vale più di una riga inventata. La colonna "da dove viene" indica il registro interno da cui esce il numero; i registri grezzi non sono pubblici. Quando un giro è stato chiuso da una revisione interna e non da un gate, la riga lo dice: serve a non attribuire a un gate un verdetto che non ha emesso. Dove il giudizio riguarda un pacchetto di testi e non singole consegne, la colonna dell’esito riporta i rilievi invece del rapporto fra respinti e totale.

| Data | Cosa è stato giudicato | Gate | Esito | Giro | Da dove viene |
|---|---|---|---|---|---|
| 14 giugno 2026 | cantiere sui contenuti del sito iaflux.it, 16 testi | controllo della lingua (as-editor) | 15 respinti su 16 | primo giro (il secondo non è stato contato) | registri del cantiere wf_85678eac, riassunti nel caso studio pubblicato il 16 settembre 2026 |
| 14 giugno 2026 | stesso cantiere, 16 testi | controllo dei fatti (claim-check, senza contratto nel roster) | 11 respinti su 16 | primo giro | registri del cantiere wf_85678eac |
| 14 giugno 2026 | stesso cantiere, 16 testi | conformità (as-compliance) | 4 respinti su 16 | primo giro | registri del cantiere wf_85678eac |
| 17 settembre 2026 | piano editoriale del blog iaflux.it (19 schede di articolo e mappa dei link) | red team (redteam-adversarial) | RESPINTO: 35 rilievi, 7 bloccanti | primo giro; il secondo verdetto del red team non è ancora stato emesso | documento del red team nella cartella del piano, non pubblico |
| 17 settembre 2026 | stesso piano, dopo le correzioni | revisione interna (gr-seo-content), non un gate | 29 rilievi chiusi, 6 trasformati in precondizioni | secondo giro | registro interno dei verdetti del blog, non pubblico |
| 17 settembre 2026 | testi dell’onda 0 del blog (box del template, descrizione di categoria, chiusure di 4 post, meta, testi del repository) | controllo della lingua (as-editor) | PATCH_NEEDED: 9 rilievi bloccanti, 13 non bloccanti | primo giro | documento del gate as-editor nella cartella dell’onda 0, non pubblico |
| 17 settembre 2026 | stessi testi, dopo le correzioni del primo giro | controllo della lingua (as-editor) | PATCH_NEEDED: 4 rilievi bloccanti, 4 non bloccanti | secondo giro | documento del gate as-editor nella cartella dell’onda 0, non pubblico |
| 17 settembre 2026 | stessi testi, dopo le correzioni del secondo giro | controllo della lingua (as-editor) | PATCH_NEEDED: 1 rilievo bloccante (una frase di questa introduzione), 5 non bloccanti | terzo giro | documento del gate as-editor nella cartella dell’onda 0, non pubblico |
| 17 settembre 2026 | stessi testi, dopo la correzione del terzo giro | controllo della lingua (as-editor) | PASS | quarto giro: i testi vanno online | documento del gate as-editor nella cartella dell’onda 0, non pubblico |

Aggiornato il 17 settembre 2026. Autore: Antonio Santoro, iaFlux Studio (Caserta).
