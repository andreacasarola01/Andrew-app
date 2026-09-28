# Quaderno di Tavola — versione Netlify (gratuita, con Google Gemini)

## File
- `index.html` — l'app
- `netlify/functions/analyze.js` — la funzione server che chiama Gemini in modo sicuro
- `netlify.toml` — configurazione Netlify

## Come pubblicarla gratis

1. Vai su https://aistudio.google.com/apikey, accedi con un account Google e crea una chiave API gratuita (clicca "Create API key"). Non serve carta di credito per il livello gratuito.
2. Vai su https://app.netlify.com e registrati gratuitamente (Google o email).
3. Nella dashboard Netlify: "Add new site" → "Deploy manually", poi trascina l'**intera cartella** di questo progetto (non solo index.html) nella zona di caricamento.
4. Nel sito creato vai su Site configuration → Environment variables → Add a variable:
   - Key: `GEMINI_API_KEY`
   - Value: la chiave presa al passo 1
5. Vai su Deploys → Trigger deploy → Deploy site, così la variabile viene letta.
6. Apri il link del sito (tipo `nomesito.netlify.app`) e prova: scrivi la dieta, scatta una foto di un pasto.

## Limiti del livello gratuito
Google Gemini offre un certo numero di richieste gratuite al giorno (di solito abbondante per un uso personale). Se un giorno lo superi, l'app mostrerà un errore e basta aspettare il giorno dopo — nessun addebito automatico.

La chiave resta sempre sul server Netlify: il browser non la vede mai.
