## Step 3: Aggiungi uno step al tuo file workflow

_Ottimo lavoro l'aggiunta di un job al tuo workflow! :dancer:_

### 📖 Teoria: Introduzione agli step nei job

Gli [step](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions#jobsjob_idsteps) sono i mattoni dei job, che ti permettono di automatizzare attività come il checkout del codice, l'esecuzione di comandi o l'uso di Action open source. Vengono eseguiti in sequenza nell'ambiente del job ma come processi indipendenti. A differenza del codice tradizionale con uno spazio di variabili condiviso, [input](https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions#inputs) e [output](https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions#outputs-for-docker-container-and-javascript-actions) devono essere dichiarati esplicitamente.

> [!TIP]
> La parte migliore di GitHub Actions è il [marketplace](https://github.com/marketplace?type=actions) dove la community ha già costruito molti strumenti gratuiti utili per [trovare e personalizzare](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/using-pre-written-building-blocks-in-your-workflow)!

### ⌨️ Attività: Aggiungi uno step al tuo file workflow

1. Nel branch `welcome-workflow`, apri il tuo file `.github/workflows/welcome.yml`.

1. Aggiungi uno step al job `welcome` per pubblicare un commento sulle nuove pull request usando GitHub CLI:

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   jobs:
     welcome:
       name: Post welcome comment
       runs-on: ubuntu-latest
       steps:
         - run: gh pr comment "$PR_URL" --body "Welcome to the repository!"
           env:
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
             PR_URL: ${{ github.event.pull_request.html_url }}
   ```

1. Esegui il commit delle tue modifiche direttamente nel branch `welcome-workflow`.

1. Con le informazioni sullo step aggiunte, Octocat esaminerà il tuo lavoro e preparerà il passaggio successivo in questo esercizio!

<details>
<summary>Hai problemi? 🤷</summary><br/>

- Assicurati che la sezione `steps` sia sotto il job `welcome` e correttamente indentata.
- Assicurati di avere le variabili d'ambiente corrette impostate.

</details>
