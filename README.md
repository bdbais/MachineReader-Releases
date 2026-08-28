# MachineReader — download beta

Repository pubblico per il download delle versioni beta di MachineReader.

## Installazione

1. Scaricare **[LATEST APK — ultima beta](https://github.com/bdbais/MachineReader-Releases/releases/latest)** dalla pagina delle release. Il collegamento punta direttamente al file da installare, senza pagine intermedie.
2. Se necessario, consultare il [manuale utente](downloads/Manuale_utente_MachineReader_Beta.pdf).
3. Aprire il file sul dispositivo Android e autorizzare l'installazione da questa fonte, se richiesto.
4. Al primo avvio seguire i tre passaggi guidati: password, fornitore del servizio e primo cliente.

## Novità beta 25

- chi si ritrova una password imposta dalle versioni precedenti la può **togliere al primo accesso**: l'app lo chiede una volta sola, subito dopo lo sblocco;
- fino alla beta 23 la password era obbligatoria, quindi nessuno l'aveva scelta davvero: senza questa domanda la novità della beta 24 sarebbe rimasta invisibile a tutti;
- chi attiva la password di sua iniziativa dalle Impostazioni non viene interrogato: ha già scelto;
- la rimozione da una sessione già aperta non richiede di ridigitare la password, perché chi è dentro ha comunque accesso ai dati.

### Verifica beta 25

- SHA-256: `3DA29A3A9F35B72A363C8B5A534AD468C7762C9ED703FA9E089DECBB03927A49`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, identità del codice fra pacchetto pubblicato e gemello di prova, aggiornamento sul posto, installazione e avvio: superati;
- 47 test strumentati e 8 unitari superati;
- provato sul dispositivo: password ereditata, scelta proposta, rimozione, riavvio senza richiesta, dati intatti.

## Novità beta 24

- **la password di accesso diventa facoltativa**: l'app parte senza chiederla e si attiva quando serve da Impostazioni, Sicurezza;
- chi ha già impostato una password la mantiene: aggiornando non cambia nulla;
- senza password l'archivio resta cifrato e legato al telefono, ma chi lo ha in mano può aprire l'app; con la password attiva la chiave viene riavvolta dalla password e la copia apribile dal dispositivo viene eliminata;
- attivare, cambiare o togliere la password non riscrive mai l'archivio: la chiave dei dati resta la stessa;
- togliendo la password decade anche l'accesso biometrico, che proteggeva la stessa chiave;
- senza password non vengono offerti biometria, riblocco automatico e cambio password, che non avrebbero nulla da proteggere;
- tolto il campo «Link del logo» dalla configurazione guidata: non ha mai funzionato, perché quel valore è l'identificativo di un allegato cifrato e non un indirizzo. La carta intestata si carica da Fornitore;
- configurazione guidata ridotta a due passi: fornitore e primo cliente.

Per i pochi telefoni a 32 bit è disponibile [MachineReader-0.1.0-beta24-armeabi-v7a.apk](downloads/MachineReader-0.1.0-beta24-armeabi-v7a.apk).

### Verifica beta 24

- SHA-256: `387CEEC959379BC395D2F1FD873652619D3866616A2F137DBFBDE51196DF66D1`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, identità del codice fra pacchetto pubblicato e gemello di prova, aggiornamento sul posto, installazione e avvio: superati;
- 45 test strumentati e 8 unitari superati;
- provato sul dispositivo: aggiornamento da una versione con password, che viene mantenuta e apre i dati; installazione nuova che parte senza password; attivazione della password dalle Impostazioni e richiesta al riavvio successivo.

## Novità beta 23

- pacchetto ridotto da 89 MB a **19 MB**: rimosso il codice non utilizzato e le librerie per architetture che i telefoni non usano;
- download molto più rapido e meno attesa durante il controllo di sicurezza di Android;
- riparato il pulsante «Inserisci dati manualmente» dentro la schermata dello strumento, che non produceva alcun effetto;
- ora compare anche l'avviso di salvataggio non riuscito mentre si sta compilando una verifica;
- nomi leggibili conservati nelle segnalazioni di errore, per facilitare la prova sul campo.

Per i pochi telefoni a 32 bit è disponibile [MachineReader-0.1.0-beta23-armeabi-v7a.apk](downloads/MachineReader-0.1.0-beta23-armeabi-v7a.apk). Se l'installazione del file principale segnala «app non installata», usare quello.

### Verifica beta 23

- SHA-256: `6C1D1E85622BE8DE25C3DB65271F175A3C1B718AC3500087925EB42F6B82447D`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, identità del codice fra pacchetto pubblicato e gemello di prova, aggiornamento sul posto sopra la beta 21, installazione e avvio: superati;
- 39 test strumentati e 8 unitari superati; inserimento manuale completo fino al PDF firmato provato sul pacchetto ridotto.

## Novità beta 22

- la chiave che cifra l'archivio non esiste più in chiaro sul dispositivo: è custodita avvolta dalla password e, con accesso biometrico attivo, da una chiave protetta dall'autenticazione dell'utente;
- senza password né autenticazione i dati non sono leggibili nemmeno con accesso fisico al telefono;
- gli archivi delle versioni precedenti vengono riscritti alla prima apertura, mantenendo la stessa password;
- cambio della password di accesso dalle Impostazioni, senza riscrivere l'archivio;
- accesso con impronta o volto automatico all'avvio, attivabile e disattivabile in qualsiasi momento;
- riblocco automatico dopo un'assenza configurabile, senza perdere la verifica in corso;
- anteprima nelle app recenti oscurata e screenshot bloccati;
- fotografie dei display conservate dentro l'app, non più nella galleria del telefono;
- copia di sicurezza dell'archivio a ogni salvataggio, con ripristino automatico;
- pacchetti condivisi illeggibili saltati invece di bloccare la sincronizzazione;
- fotografia dello strumento accanto al link del manuale;
- rapporti PDF impaginati su più fogli, con avviso stampato sui dati inseriti a mano;
- norma ambigua fra due classi rifiutata invece che indovinata.

### Prima di aggiornare

Creare un backup cifrato dalle Impostazioni. Al primo accesso l'archivio viene riscritto: l'attesa cresce con la quantità di allegati, non chiudere l'app. L'accesso con impronta o volto va riattivato una volta.

### Verifica beta 22

- SHA-256: `98D78E97A46AD4D820DB133121E38008E3CF84026B29F3F2E2CDC3CF2E35FED9`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, aggiornamento sul posto sopra la beta 21, installazione e avvio: superati su `MachineReader_API34`;
- 38 test strumentati, 8 test unitari e scambio fra due operatori su due dispositivi: superati.

## Novità beta 21

- elenco clienti più compatto, ordinato e immediatamente leggibile;
- schede con icona cliente, nome, numero di strumenti, modifica e apertura rapida;
- barra di acquisizione estesa su tutta la larghezza della home;
- Fotocamera, Immagini e Inserimento manuale occupano tre spazi uguali;
- area di tocco alta 64 dp, adatta all'uso con una mano;
- test UI dedicato superato sull'emulatore `MachineReader_API34`;
- manuale aggiornato.

### Verifica beta 21

- SHA-256: `FFD27F0EB02EF96BD9FCBDC34AD5BA11290978387193AE44325134F5DA4D75DC`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, test UI, installazione e avvio: superati su `MachineReader_API34`.

## Novità beta 20

- pulsanti d'azione adattivi alla larghezza reale disponibile;
- icona e testo restano sulla stessa riga anche con display stretto o caratteri Android ingranditi;
- spaziatura e dimensione del testo si riducono gradualmente soltanto quando necessario;
- area di tocco dei comandi invariata, per mantenere semplicità e accessibilità;
- corretti in particolare i comandi affiancati **Modifica** e **Clona**;
- manuale aggiornato con il nuovo comportamento.

### Verifica beta 20

- SHA-256: `AE577F09DBD2922DDB66248CFD6F85AEB274FF5FC5F6E042DA3A7AC6FE230C9D`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- firma, ZIP alignment, metadati, installazione e avvio: superati su `MachineReader_API34`.

## Novità beta 19

- nuova procedura obbligatoria di pubblicazione in due fasi;
- l'APK versionato viene pubblicato prima senza modificare il collegamento Latest;
- il file viene riscaricato dal repository pubblico e confrontato con SHA-256;
- firma, struttura ZIP, versione interna, installazione e avvio vengono verificati automaticamente;
- `MachineReader-latest.apk` viene aggiornato soltanto dopo il superamento di tutti i controlli;
- la beta precedente rimane disponibile per il ripristino;
- manuale aggiornato con la procedura in caso di download incompleto o pacchetto non valido.

### Verifica beta 19

- SHA-256: `FD538C77C995B70FB05D69948109C108F5F2AFCE0C54249D8DBB114671B622ED`
- certificato SHA-256: `8a5e03eba7ba28786d2956aabcb12da21269bb5041b09f5f996b3e7d7ad899f8`
- installazione e avvio: superati su `MachineReader_API34`.

## Novità beta 18

- controllo preventivo dell'intera serie di fotografie prima di creare la lettura;
- rifiuto delle immagini prive di sufficienti riferimenti a norma, parametri tecnici, unità di misura o esito;
- eliminato il precedente ripiego che compilava i parametri mancanti con valori dimostrativi;
- i parametri non riconosciuti restano vuoti e vengono segnalati come da controllare;
- riconoscimento dell'esito `SUPERATO` o `NON SUPERATO` anche quando compare soltanto nell'ultima pagina;
- segnalazione delle possibili norme EN/IEC/CEI non configurate, senza generare automaticamente soglie o parametri non verificati;
- test automatici, changelog interno e manuale aggiornati.

## Novità beta 17

- nuova icona **Inserisci dati manualmente** accanto a Fotocamera e Immagini nella home;
- percorso alternativo dalla scheda dello strumento già selezionato;
- scelta obbligatoria della norma prima della compilazione dei parametri;
- compilazione manuale di valori, data, ora, esito complessivo, operatore e firma;
- possibilità di creare un nuovo strumento durante il percorso rapido;
- il PDF conserva il normale formato del rapporto;
- il Markdown dichiara esplicitamente che i dati sono stati caricati a mano e non provengono dall’OCR;
- manuale e changelog aggiornati.

## Novità beta 16

- sincronizzazione automatica dell’archivio condiviso dopo l’accesso, attiva per impostazione predefinita;
- nuovo interruttore **Sincronizza all’avvio** nelle Impostazioni;
- disattivando l’automatismo la cartella resta collegata e **Sincronizza ora** continua a funzionare;
- riepilogo più chiaro con stato dell’automatismo e data dell’ultimo controllo;
- manuale aggiornato con il nuovo comportamento.

## Novità beta 15

- dimensione testo selezionabile tra Compatta, Normale e Grande, con adattamento automatico sui display stretti;
- etichette principali accorciate o mantenute su una sola riga;
- firma con sfondo trasparente, anche durante la rigenerazione di firme salvate in precedenza;
- carta intestata ritagliata, centrata, orientata e ravvivata automaticamente senza deformazioni;
- eliminata la colonna Esito dalla tabella delle misure: SUPERATO/NON SUPERATO compare soltanto come esito complessivo in testata;
- nuovo pulsante **Rigenera PDF** per applicare al rapporto i dati aggiornati di fornitore, cliente e strumento senza rifare la lettura;
- manuale aggiornato con il nuovo flusso.

## Novità beta 14

- controllo automatico degli aggiornamenti dopo l’accesso;
- dialog semplice con versione, note, **Scarica aggiornamento** e **Più tardi**;
- eventuali problemi di rete non interrompono l’avvio o il lavoro;
- procedura descritta nel manuale, insieme al controllo manuale nelle informazioni dell’app.

## Novità beta 13

- archivio multi-operatore configurabile su una cartella condivisa Drive, OneDrive, Dropbox o locale;
- pacchetti `.mrsync` cifrati e separati per operatore, senza sovrascrivere quelli precedenti;
- controllo automatico all’avvio e pulsante **Sincronizza ora**;
- fusione additiva e deduplicata di clienti, strumenti, letture e allegati;
- conflitti conteggiati e dati locali conservati senza sovrascrittura silenziosa;
- audit semplificato con creatore, data di creazione, ultimo modificatore e ultima modifica;
- dati audit inclusi nell’esportazione Excel.

## Novità beta 12

- sostituiti nell’interfaccia e nei documenti tutti i riferimenti a macchina/macchine con strumento/strumenti;
- il pulsante **Esporta elenco su Excel** è disabilitato quando il cliente non ha strumenti;
- aggiunta icona Excel al comando di esportazione;
- carta intestata configurabile direttamente nella modifica dei dati del fornitore e utilizzata nella testata dei PDF.

## Novità beta 11

- firma a video e nome operatore incorporati in ogni PDF;
- modifica, clonazione, eliminazione e rigenerazione PDF delle letture;
- modalità sequenziale per verificare più strumenti con una sola firma;
- scanner multipagina con ritaglio, rotazione e miglioramento automatici;
- immagini originali mostrate prima dei dati OCR e allegabili al PDF su scelta;
- carta intestata del fornitore da fotografia, immagine o PDF, senza etichetta “Fornitore” nella stampa;
- `ESITO: SUPERATO / NON SUPERATO` in testata e righe “NON CONTROLLATO” escluse;
- importazione elenco strumenti tramite modello CSV modificabile con Excel;
- esportazione Excel compatibile con cliente, strumenti e storico letture;
- data e ora ricavate dai metadati EXIF quando disponibili, sempre verificabili e modificabili;
- norme predefinite corrette: EN 61010 CL I, EN 61010 CL II ed EN 62353 CL I/BF;
- navigazione Back corretta, doppio Back entro 5 secondi per uscire e sessione mantenuta alla rotazione.

## Avvertenze

Questa è una beta destinata a prove e valutazione. I dati OCR, la norma selezionata, i limiti e gli esiti devono sempre essere verificati da un operatore qualificato.

Il codice sorgente è conservato in un repository privato. Questo repository contiene soltanto documentazione e pacchetti pubblici di distribuzione.

## Aggiornamenti

Nell’app aprire **Altro → Informazioni sull’app → Controlla e scarica aggiornamenti**. L’app controlla il file pubblico `latest.json` e, se trova una versione più recente, mostra il pulsante **Scarica APK**. La decisione di scaricare e installare resta sempre esplicita.

Non viene utilizzata la sezione GitHub Releases, così GitHub non mostra pacchetti automatici denominati “Source code”.
