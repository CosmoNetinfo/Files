# CosmoNet Files – Hosting Gratuito per Download

Questo repository contiene i file che vengono serviti dal dominio:

**https://files.cosmonet.info/**

Viene usato per distribuire le applicazioni, gli archivi ZIP e le guide di CosmoNet tramite link diretti.

---

## Struttura delle cartelle

La struttura base è:

- `app/` – file **APK** (app Android)
- `zip/` – file **ZIP** (archivi, tool, pacchetti)
- `guide/` – file **PDF** e guide varie
- `index.html` – pagina di benvenuto con i link principali

Puoi aggiungere altre cartelle se ti servono (es. `img/`, `tools/`), basta rispettare la stessa logica.

---

## Regola fondamentale per i link

Il link pubblico di un file è sempre:
https://files.cosmonet.info/ + [percorso del file nel repository]

Esempi:

- File `app/CosmonetApp.apk`  
  → `https://files.cosmonet.info/app/CosmonetApp.apk`

- File `zip/BackupTool_1.0.zip`  
  → `https://files.cosmonet.info/zip/BackupTool_1.0.zip`

- File `guide/GuidaCosmoNet.pdf`  
  → `https://files.cosmonet.info/guide/GuidaCosmoNet.pdf`

⚠ **Attenzione alle maiuscole**: `CosmonetApp.apk` è diverso da `cosmonetapp.apk`.

---

## Come caricare nuovi file (metodo semplice via sito GitHub)

### 1. Apri il repository

Vai su:  
`https://github.com/CosmoNetinfo/Files`

Assicurati di vedere le cartelle `app`, `zip`, `guide`.

### 2. Caricare un APK

1. Entra nella cartella `app/`.
2. Clicca in alto a destra su **Add file → Upload files**.
3. Seleziona il file APK dal tuo PC (es. `MiaApp-1.0.apk`).
4. In basso, nel box del commit, scrivi un messaggio semplice (es. `Add MiaApp 1.0 APK`).
5. Clicca sul pulsante verde **Commit changes**.

**Link risultante:**

Se il file è `app/MiaApp-1.0.apk`, il link sarà:

`https://files.cosmonet.info/app/MiaApp-1.0.apk`

### 3. Caricare un file ZIP

1. Entra nella cartella `zip/`.
2. **Add file → Upload files**.
3. Carica il file ZIP (es. `ToolBackup.zip`).
4. Commit (es. messaggio: `Add ToolBackup zip`).

**Link risultante:**

`https://files.cosmonet.info/zip/ToolBackup.zip`

### 4. Caricare una guida PDF

1. Entra nella cartella `guide/`.
2. **Add file → Upload files**.
3. Carica il PDF (es. `GuidaCosmonet.pdf`).
4. Commit (es. messaggio: `Add CosmoNet guide`).

**Link risultante:**

`https://files.cosmonet.info/guide/GuidaCosmonet.pdf`

---

## Come ricavare da solo il link di un file

1. Vai nella repo `Files` su GitHub.
2. Apri la cartella giusta (`app`, `zip`, `guide`, …).
3. Clicca sul file (es. `MiaApp-2.0.apk`).
4. Sopra al file vedrai il percorso, per esempio:

   `Files / app / MiaApp-2.0.apk`

5. Il tuo link pubblico è:

   `https://files.cosmonet.info/app/MiaApp-2.0.apk`

### Doppio controllo con GitHub Pages

Se vuoi verificare che il percorso sia corretto, prova prima con l’URL GitHub:

`https://cosmonetinfo.github.io/Files/app/MiaApp-2.0.apk`

Se funziona lì, funzionerà anche:

`https://files.cosmonet.info/app/MiaApp-2.0.apk`

---

## Come usare questi link sul sito CosmoNet (WordPress / Altervista)

### Pulsante “Scarica”

1. Modifica la pagina/articolo in WordPress.
2. Aggiungi un **blocco pulsante**.
3. Nel campo URL incolla il link, per esempio:

   `https://files.cosmonet.info/app/CosmonetApp.apk`

4. Salva la pagina.

### Link testuale

1. Scrivi il testo (es. “Scarica l’app Android qui”).
2. Seleziona “qui”.
3. Clicca sull’icona del link.
4. Incolla l’URL del file hosting.

---

## Cosa NON fare

- **Non usare solo l’URL della cartella**, tipo:
  - `https://files.cosmonet.info/app/`
  - `https://files.cosmonet.info/zip/`

  Questi URL danno **404** perché le cartelle non hanno `index.html` e GitHub Pages non mostra l’elenco dei file.

- **Non cambiare i record DNS** che puntano `files.cosmonet.info` a GitHub (`cosmonetinfo.github.io`), a meno di sapere esattamente cosa stai facendo.

---

## Uso con Git (facoltativo, da PC)

Se lavori anche in locale nella cartella `L:\hostig files`:

### Aggiungere o aggiornare file
powershell
cd "L:\hostig files"
Copia o sostituisci i file nelle cartelle (app, zip, guide, ...)
git add .
git commit -m "Aggiorna file hosting"
git pull --rebase origin main
git push

I link pubblici seguiranno sempre la stessa regola:

`https://files.cosmonet.info/` + percorso del file.
Per usarlo:
Vai su https://github.com/CosmoNetinfo/Files.
Add file → Create new file.
Nome: README.md.
Incolla tutto il testo sopra.
Fai Commit changes.
