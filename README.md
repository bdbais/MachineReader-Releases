# MachineReader — download beta

Repository pubblico per il download delle versioni beta di MachineReader.

## Installazione

1. Scaricare **[LATEST APK — ultima beta](downloads/MachineReader-latest.apk)**. Il collegamento punta direttamente al file da installare, senza pagine intermedie.
2. Se necessario, consultare il [manuale utente](downloads/Manuale_utente_MachineReader_Beta.pdf).
3. Aprire il file sul dispositivo Android e autorizzare l'installazione da questa fonte, se richiesto.
4. Al primo avvio seguire i tre passaggi guidati: password, fornitore del servizio e primo cliente.

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
