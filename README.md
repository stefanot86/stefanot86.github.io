# stefanot86.github.io

Pagine pubbliche delle mie app: informative sulla privacy e documenti che devono stare a un
indirizzo stabile, perché Google Play e gli store in genere chiedono un indirizzo pubblico e poi
si aspettano di ritrovarlo lì.

Qui ci sono **copie**. La fonte di ogni pagina è versionata nel repository dell'app a cui
appartiene, accanto al codice che la fa dire il vero: se un giorno un'app cambia il suo rapporto
con i dati, la correzione parte da là e arriva qui, non il contrario.

| Pagina | App |
| --- | --- |
| `padelpoint/informativa/` | PadelPoint, italiano |
| `padelpoint/informativa/en/` | PadelPoint, inglese |

Sono file HTML completi e senza dipendenze: nessun font remoto, nessun foglio di stile esterno,
nessuno script. Un'informativa che per mostrarsi chiama tre server contraddice quello che c'è
scritto dentro.

Il file `.nojekyll` disattiva Jekyll: non serve, sono pagine statiche già pronte, e senza di lui
la pubblicazione fa un passo in più ad ogni modifica.
