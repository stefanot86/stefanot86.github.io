# Informativa sulla privacy

Questa cartella è la **fonte** dell'informativa. La pagina pubblicata è una copia: si modifica
qui, si ricopia là. Un'informativa che vive solo su un sito non ha storia, e fra due anni nessuno
sa più quando è cambiata né perché.

| File | Lingua |
| --- | --- |
| `index.html` | italiano |
| `en/index.html` | inglese |

Due pagine e non una bilingue: Play Console accetta un indirizzo dell'informativa **per ogni
lingua della scheda**, quindi ognuna delle due ha il suo. In cima a ciascuna c'è il collegamento
all'altra, per chi arriva sulla lingua sbagliata.

Sono due file HTML **completi e senza dipendenze**: nessun font remoto, nessun foglio di stile
esterno, nessuno script. Un'informativa che spiega quali dati escono dal telefono non deve, per
mostrarsi, chiamare tre server.

## Prima di pubblicare

Le due pagine sono complete: l'indirizzo di contatto è `stefanoto@gmail.com`, scritto per esteso e
come collegamento `mailto:`. È pubblico per scelta — Play chiede comunque un modo per raggiungere
lo sviluppatore — e sta in una pagina indicizzata, quindi prima o poi i raccoglitori di indirizzi
lo troveranno. Se un giorno diventasse un problema, si cambia qui e si ripubblica: è il vantaggio
di avere la fonte in repository.

Da controllare la **data** in cima alle due pagine: dice quando l'informativa è stata scritta
l'ultima volta, e va aggiornata solo quando il testo cambia davvero — non ad ogni
ripubblicazione.

## Dove è pubblicata

Sul repository pubblico **`stefanot86/stefanot86.github.io`**, con GitHub Pages. Non su questo
repository, che è privato: sul piano gratuito Pages funziona solo sui repository pubblici, e
renderlo pubblico vorrebbe dire pubblicare tutto il codice.

```
https://stefanot86.github.io/padelpoint/informativa/       italiano
https://stefanot86.github.io/padelpoint/informativa/en/    inglese
```

Là dentro le due pagine sono **copie**, e lo dicono nel commento in testa: la fonte è qui, accanto
al codice che le fa dire il vero. Le correzioni partono da qui e si ricopiano là — mai il
contrario, o la pagina pubblicata e l'app finirebbero per raccontare cose diverse.

Nel repository pubblico ci sono anche due file che non vengono da qui: una pagina di radice, perché
un 404 sul dominio che ospita un'informativa sulla privacy non ispira fiducia a chi tronca
l'indirizzo per curiosità, e un `.nojekyll`, perché sono pagine statiche già pronte e non serve
che Jekyll le rielabori.

C'è poi `app-ads.txt`, nella radice del sito, e questo invece viene da qui: la fonte è
`play/app-ads.txt`. Lo cerca AdMob per verificare che chi vende gli spazi pubblicitari dell'app
sia davvero lo sviluppatore. Deve stare esattamente in `https://stefanot86.github.io/app-ads.txt`,
e il sito web dello sviluppatore in Play Console deve essere `https://stefanot86.github.io`: AdMob
lo cerca sul dominio dichiarato nella scheda. La riga dentro dice l'ID editore AdMob; cambia solo
se cambia l'account AdMob, e vale per tutte le app pubblicate con lo stesso sito.

### Aggiornare una pagina pubblicata

1. Correggere il file qui, e aggiornare la data in cima.
2. Ricopiarlo in `padelpoint/informativa/` del repository pubblico, rimettendo il commento che dice
   che quella è una copia.
3. Verificare che la pagina si apra: Pages ricostruisce in un minuto circa.

In Play Console va l'indirizzo italiano nella scheda italiana e quello inglese nella scheda
inglese.

## Quando va rifatta

Ogni volta che l'app cambia il **rapporto** con i dati, non ogni volta che cambia l'app. In
concreto:

- se compare un altro permesso nel manifest;
- se entra un'altra libreria di terzi che parla con la rete (analisi, crash), o se il banner
  AdMob cambia natura (altri formati, altre schermate, il modulo di consenso);
- se nasce un account, una sincronizzazione o una condivisione fra dispositivi;
- se l'app comincia a conservare un dato di natura diversa da quelli elencati.

Il testo attuale dice, in tutte e due le lingue: un solo permesso, Internet, usato solo dal
banner AdMob in fondo alla home e alle statistiche, con i dati che quel banner usa (ID
pubblicità, IP, informazioni sul dispositivo, interazioni con l'annuncio) e come limitarli;
nessun account, nessuno strumento di analisi, dati delle partite nell'archivio privato dell'app.
E dichiara gli altri tre casi in cui qualcosa esce dal telefono — il backup automatico di
Android, il file esportato dall'utente, la frase passata al motore di sintesi vocale. Se una di
queste frasi non è più vera, l'informativa va corretta **prima** di pubblicare la versione nuova.
