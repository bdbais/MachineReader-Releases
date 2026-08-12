# MachineReader — download beta

Repository pubblico per il download delle versioni beta di MachineReader.

## Installazione

1. Scaricare **[LATEST APK — ultima beta](downloads/MachineReader-latest.apk)**. Il collegamento punta direttamente al file da installare, senza pagine intermedie.
2. Se necessario, consultare il [manuale utente](downloads/Manuale_utente_MachineReader_Beta.pdf).
3. Aprire il file sul dispositivo Android e autorizzare l'installazione da questa fonte, se richiesto.
4. Al primo avvio seguire i tre passaggi guidati: password, fornitore del servizio e primo cliente.

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
