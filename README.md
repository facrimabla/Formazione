# Foglio Partita

App per il telefono da usare in panchina durante la partita di pallavolo.
Per ogni set (3) si segnano:

- la **formazione** sul campo (posizioni 4-3-2 in rete, 5-6-1 in fondo)
- le **sostituzioni** (massimo 8 per set): chi esce, chi entra, punteggio
- i **time out** (massimo 2 per set) con il punteggio

In più:

- campo **Nome partita** in alto
- il punteggio si formatta da solo: scrivendo `1512` compare `15-12`
- pulsante **Esporta**: scarica un file di testo con il riepilogo della partita
- pulsante **Nuova partita**: cancella tutto (serve un secondo tocco per confermare)
- i dati restano nel browser del telefono, anche se chiudi la pagina
- funziona anche senza connessione, dopo la prima apertura

## File del progetto

Tutti nella stessa cartella, senza sottocartelle:

| File | A cosa serve |
| --- | --- |
| `index.html` | l'app |
| `manifest.webmanifest` | permette di installarla come app |
| `sw.js` | la tiene disponibile anche offline |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | icona sulla schermata Home |
| `README.md` | queste istruzioni |

## Pubblicare su GitHub Pages

1. Su GitHub crea un nuovo repository (ad esempio `foglio-partita`).
2. Carica **tutti** i file della cartella (**Add file → Upload files**, seleziona tutto e trascina).
3. Vai in **Settings → Pages**.
4. In **Build and deployment** scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, poi **Save**.
5. Dopo uno o due minuti la pagina è online su:
   `https://NOME-UTENTE.github.io/foglio-partita/`

## Installarla come app sul telefono

Apri l'indirizzo **direttamente nel browser**, non da un link dentro WhatsApp, Telegram, Instagram o altre app: il loro browser interno non permette l'installazione.

- **iPhone:** apri in **Safari** → Condividi → **Aggiungi a Home**. Se non vedi la voce, scorri verso il basso l'elenco delle azioni.
- **Android:** apri in **Chrome** → menu ⋮ → **Installa app** (su alcune versioni **Aggiungi a schermata Home**).

Se la voce **Installa app** non compare:

- controlla che l'indirizzo inizi con `https://` e che tutti i file siano stati caricati;
- apri la pagina, aspetta qualche secondo, ricaricala una volta e riapri il menu;
- se avevi già aggiunto una versione precedente alla Home, rimuovila e aggiungila di nuovo.

Una volta installata si apre a tutto schermo, con la sua icona.

## Aggiornare l'app

Dopo aver sostituito `index.html` su GitHub, apri l'app due volte: la prima mostra la versione salvata e scarica quella nuova, la seconda mostra quella aggiornata. Se cambi altri file, aumenta il numero di versione in `sw.js` (`foglio-partita-v1` → `foglio-partita-v2`).

## Da sapere

- I dati sono salvati **sul telefono e nel browser** con cui li inserisci. Non passano ad altri dispositivi e si perdono se cancelli i dati del sito. Esporta a fine partita se vuoi conservarli.
- Usa sempre lo stesso indirizzo: browser o indirizzi diversi hanno dati separati. L'app installata e la pagina aperta nel browser possono avere dati separati su iPhone.
- I font vengono caricati da Google Fonts. Senza connessione l'app funziona lo stesso, con un carattere di sistema.
