# CycleTrack — Pubblicazione su GitHub Pages + APK con PWABuilder

Questa cartella contiene tutto il necessario:
- `index.html` — l'app
- `manifest.json` — descrittore PWA (nome, icone, colori)
- `service-worker.js` — abilita il funzionamento offline
- `icon-192.png`, `icon-512.png`, `icon-*-maskable.png` — icone dell'app

## PARTE 1 — Pubblicare su GitHub Pages

1. Vai su [github.com](https://github.com) e crea un nuovo repository pubblico
   (es. nome: `cycletrack`).
2. Carica **tutti i file di questa cartella** nella radice del repository
   (usa "Add file → Upload files" sul sito, oppure git da terminale).
3. Nel repository vai su **Settings → Pages**.
4. In "Source" seleziona il branch `main` e la cartella `/ (root)`, poi Save.
5. Dopo 1-2 minuti il sito sarà online a un indirizzo tipo:
   `https://tuonomeutente.github.io/cycletrack/`
6. Apri quell'indirizzo dal telefono per verificare che l'app funzioni
   (puoi già fare "Aggiungi a Home" dal browser a questo punto).

## PARTE 2 — Generare l'APK con PWABuilder

1. Vai su [pwabuilder.com](https://www.pwabuilder.com)
2. Incolla l'URL del tuo sito GitHub Pages
   (es. `https://tuonomeutente.github.io/cycletrack/`)
3. Clicca "Start" — PWABuilder analizza il manifest e mostra un punteggio.
4. Vai alla sezione **Android** (icona Android) → "Generate Package".
5. Lascia le opzioni di default (va bene "Signing key: generate new"),
   oppure personalizza nome pacchetto, versione, ecc.
6. Scarica lo ZIP generato: conterrà l'**APK firmato** pronto da installare,
   più il file `.aab` se vuoi pubblicarla su Google Play Store.

## Note

- Per installare l'APK sul telefono: abilita "Origini sconosciute" / "Installa
  app sconosciute" nelle impostazioni Android, poi apri il file APK.
- I dati delle sessioni sono salvati in locale (localStorage) — restano sul
  dispositivo e non vengono inviati altrove.
- Se in futuro modifichi `index.html`, ricarica il file su GitHub: GitHub
  Pages si aggiorna automaticamente in 1-2 minuti. Non serve rigenerare
  l'APK a meno che tu non voglia ridistribuire una nuova versione del
  pacchetto installabile.
