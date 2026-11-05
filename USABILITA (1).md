# Principi di usabilità del progetto

Raccolta delle riflessioni emerse dai test sull'app. Vanno applicate a ogni nuova funzione e a ogni modifica.
Chi usa l'app: il direttore del coro (carica e organizza) e i coristi (consultano, leggono, annotano), spesso in piedi, in prova o in concerto, con tablet e smartphone, a volte senza internet.

## 1. Mobile prima di tutto
- Ogni schermata va pensata e controllata prima su telefono (circa 360 px di larghezza), poi sugli schermi più grandi.
- Nelle schede il titolo sta in alto, a tutta larghezza; le azioni stanno in una riga sotto. Mai titoli schiacciati a sinistra da una fila di pulsanti.
- Bersagli di tocco comodi (almeno 38–40 px), anche con poca luce e le mani occupate.

## 2. Icone al posto delle parole
- Dove l'icona è riconoscibile, si usa l'icona e non la parola, per risparmiare spazio.
- Ogni icona ha sempre un nome accessibile (`aria-label`) e una descrizione al passaggio o alla pressione prolungata (`title`).
- Le due schede principali (Archivio, Raccolte) restano con il testo, perché sono la navigazione.
- Esempi già applicati: torna indietro (freccia), play/pausa, velocità con − e +, filtri (genere, lingua, periodo, ordina, preferiti), nuovo spartito (+), leggi, allega file, altre azioni, strumenti di annotazione.

- Un'icona va usata solo se è capita da sola. Se i test mostrano che non lo è (esempio: la graffetta per caricare il PDF, scambiata per una puntina), si toglie dalla scheda e l'azione passa in un menu con testo chiaro, oppure si cambia simbolo.
- Un dato mancante va reso visibile (esempio: "senza file" accanto al brano) così l'utente capisce cosa può fare.

## 3. Tutto ciò che si apre ha lo stile dell'app
- Tendine, menu, finestre e selettori (compresa la ruota dei colori) non usano mai i controlli nativi del telefono.
- Vanno costruiti con lo stesso stile in vetro del resto: sfondo semitrasparente con sfocatura, bordo chiaro, ombra morbida, riflesso sul bordo superiore, angoli arrotondati.
- La voce selezionata si riconosce dal colore d'accento e da una spunta; un filtro attivo mostra un puntino sull'icona.

## 4. Coerenza grafica
- Tema azzurro e blu, chiaro e scuro in base al dispositivo.
- Azioni principali con sfumatura blu-azzurra; azioni secondarie in vetro neutro.
- Stessi raggi, ombre e bordi in tutta l'app. Ogni elemento nuovo si confronta con quelli esistenti prima di essere considerato finito.

## 5. Lettore delle partiture
- La partitura occupa tutto lo schermo; i comandi stanno in un pannello sovrapposto che non ruba spazio.
- Il pannello scende dall'alto e si nasconde trascinandolo verso l'alto. Si nasconde da solo quando si scorre la partitura verso il basso o si avvia lo scroll automatico. Si riapre toccando la maniglia.
- Lo scroll automatico si imposta con la durata del brano. Play e pausa con icona; la velocità si corregge solo con − e +, senza percentuali.
- Le funzioni secondarie (impostazioni del metronomo) stanno dietro una freccia verso il basso e si aprono verso il basso.
- Gli strumenti di annotazione stanno in basso, per non coprire il pannello dei comandi. Penna, evidenziatore, testo, gomma, annulla e ruota dei colori sono icone.

- Le stesse regole valgono **dentro il lettore**: pannello dei comandi, barra di Annota, ruota dei colori e impostazioni del metronomo seguono icone, vetro, coerenza e bersagli di tocco della parte esterna.
- Nel pannello: la durata ha l'icona dell'orologio, il metronomo ha la sua icona con la parola, l'icona della matita (Annota) sta in fondo alla riga del metronomo. Nelle impostazioni, ogni numero ha un'etichetta (BPM, Battiti).
- Nella barra di Annota gli strumenti sono separati dai colori e dall'annulla con sottili divisori; i colori sono cerchi da 30 px, comodi da toccare.

## 6. Meno elementi, più chiari
- Si tolgono i controlli che l'utente non capisce (frecce brano precedente/successivo) e quelli doppi (stella nel lettore, già presente nell'Archivio).
- Le azioni distruttive (elimina brano) non stanno a portata di tocco accidentale: sono dentro il menu ⋮ e chiedono conferma.
- Le azioni di aggiunta a una raccolta e di creazione di una nuova raccolta stanno nella stessa finestrella.

- Niente finestre native del browser (conferma, richiesta di testo, avvisi): non sempre funzionano e non hanno lo stile dell'app. Si usano finestre in vetro dell'app.
- Ogni azione distruttiva (elimina brano, elimina raccolta) apre una finestra di conferma che spiega cosa succede; il pulsante di annullamento è quello predefinito.
- Una finestra senza una funzione per la × in alto non la mostra: si chiude toccando fuori o con Esc.
- Ogni inserimento ha il suo annullamento immediato (la × accanto a "Inserito", i brani "Appena inseriti" da toccare per togliere).
- Per inserire in fretta più elementi si usa il completamento automatico: si scrive poche lettere, compaiono i suggerimenti, un tocco li aggiunge e il campo resta pronto per il successivo. Nello stesso modo si suggeriscono le raccolte già esistenti per non crearne di doppie.
- Quando una raccolta è vuota, al centro c'è un grande + che invita a iniziare.

## 7. Dati e uso senza internet
- L'app deve funzionare offline (PWA) e salvare sul dispositivo partiture, annotazioni, preferiti e frequenza di utilizzo.
- La condivisione tra direttore e coristi richiede un backend (fase 2); fino ad allora i dati restano sul dispositivo e questo va detto chiaramente.

## 8. Come si lavora
- Il feedback arriva da prove su dispositivi veri: ogni riflessione si registra qui e si applica anche alle parti dell'app non citate.
- Prima di consegnare una modifica: controllare mobile, tema chiaro e scuro, coerenza del vetro, nomi accessibili delle icone, comportamento senza internet.

## Da valutare in futuro
- Icone anche per le schede Archivio e Raccolte, solo se i test mostrano che sono capite senza testo.
- Pulsante "brano successivo" con un nome chiaro per leggere una raccolta di seguito.
