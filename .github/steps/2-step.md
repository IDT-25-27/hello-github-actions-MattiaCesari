## Step 2: Aggiungi un job al tuo file workflow

Ottimo lavoro! :tada: Hai aggiunto un file workflow!

### 📖 Teoria: Introduzione ai job

Un [job](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions#jobs) è un gruppo di step che vengono eseguiti insieme sullo stesso [runner](https://docs.github.com/en/actions/using-github-hosted-runners/using-github-hosted-runners/about-github-hosted-runners) all'interno di un workflow. Ogni job è definito nella sezione `jobs` ed è eseguito in modo indipendente e in parallelo per impostazione predefinita.

I job ti aiutano a organizzare il tuo workflow in unità logiche, come la compilazione (building), il test o il deployment del tuo codice.

> [!Tip]
> Puoi definire un job da eseguire con più [variazioni usando una strategia a matrice](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/running-variations-of-jobs-in-a-workflow).

### ⌨️ Attività: Aggiungi un job al tuo file workflow

1. Nel branch `welcome-workflow`, apri il tuo file `.github/workflows/welcome.yml`.

1. Modifica il file per aggiungere la sezione `jobs` e 1 job chiamato `welcome`, che verrà eseguito sull'ultimo sistema operativo Ubuntu.

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
   ```

1. Esegui il commit delle tue modifiche nel branch `welcome-workflow`.

1. Con le informazioni sul job aggiunte, Octocat esaminerà il tuo lavoro e preparerà il passaggio successivo in questo esercizio!

<details>
<summary>Hai problemi? 🤷</summary><br/>

- Assicurati che la sezione `jobs` sia correttamente indentata nel tuo file YAML.
- Conferma di stare modificando il file e il branch corretti.

</details>
