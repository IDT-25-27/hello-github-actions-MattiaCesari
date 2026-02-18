## Step 1: Crea un file workflow

### 📖 Teoria: Introduzione ai workflow

Un **workflow** è un processo automatizzato che definisci nel tuo repository. I workflow sono descritti nei file YAML memorizzati nella directory `.github/workflows`. Ogni workflow è attivato da specifici [eventi](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows) che accadono nel tuo repository come l'apertura di una pull request, il push del codice, o la creazione di una issue.

I workflow ti permettono di automatizzare attività come la compilazione (build), il test, o il deployment del tuo codice, e possono rispondere a quasi tutte le attività nel tuo progetto.

> [!NOTE]
> Se vuoi saperne di più consulta queste risorse:
> - [Capire GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
> - [Eventi che attivano i workflow](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows)
> - [Prezzi dei runner Actions](https://docs.github.com/en/billing/reference/actions-runner-pricing)

### ⌨️ Attività: Crea un file workflow

1. Apri questo repository in una nuova scheda del browser così puoi lavorare sugli step mentre leggi le istruzioni in questa scheda.

1. Nella scheda **Code** del tuo repository, crea un nuovo branch chiamato `welcome-workflow`.

   <img width="400" alt="create branch screenshot" src="https://github.com/IDT-25-27/idt-25-27-classroom-173794-hello-github-actions-hello-github-actions/blob/main/.github/images/create-branch-screenshot.png?raw=true" />

1. Nel branch `welcome-workflow`, naviga nella directory `.github/workflows`.

1. Crea un nuovo file chiamato `welcome.yml` nella directory `.github/workflows` con il seguente contenuto:

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   ```

   > [!NOTE]
   > Questo è un file workflow incompleto. È normale se ricevi un messaggio di errore. Un passo alla volta! 😎

1. Esegui il commit delle tue modifiche direttamente nel branch `welcome-workflow`.

1. Con il tuo file workflow committato, Octocat controllerà il tuo lavoro e preparerà il passaggio successivo in questo esercizio!

<details>
<summary>Hai problemi? 🤷</summary><br/>

- Assicurati di essere nel branch `welcome-workflow` quando crei il file workflow.
- Controlla due volte il percorso del file e l'indentazione YAML.

</details>
