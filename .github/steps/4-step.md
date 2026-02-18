## Step 4: Attiva il workflow

_Ora hai aggiunto un workflow completamente funzionante al tuo repository! :smile:_

### 📖 Teoria: Vedere il tuo workflow in azione

Tutti i workflow in esecuzione e terminati possono essere visti nella scheda **Actions** del tuo repository.

Poiché hai impostato il workflow per essere eseguito sull'evento `pull_request`, si attiverà automaticamente quando viene aperta una pull request.

> [!TIP]
> I workflow associati alla pull request possono essere visti anche nel log della pull request vicino al pulsante merge. Puoi anche [creare una regola](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets#require-status-checks-to-pass-before-merging) che impedisce l'unione (merge) se il workflow fallisce!

### ⌨️ Attività: Attiva il workflow

1. Nella scheda **Pull requests**, crea una pull request dal branch `welcome-workflow` verso `main`.

1. Nota il commento che il workflow aggiunge alla pull request.

1. Nota l'area vicino al pulsante merge che dice "All checks have passed" (Tutti i controlli sono passati).

1. Con la pull request creata e il nostro workflow attivato, Octocat preparerà il passaggio successivo in questo esercizio!

### ⌨️ Attività: Ispeziona il workflow

1. Nella parte superiore del repository, seleziona la scheda **Actions**.

1. Nella barra laterale sinistra, seleziona il workflow chiamato **Post welcome comment**.

  > 💡 **Tip:** Puoi ignorare le altre actions. Quelle servivano per insegnare questo esercizio.

1. Fai clic sulla prima voce di esecuzione intitolata **Welcome workflow** per mostrare un diagramma dei job dell'esecuzione.

1. Fai clic sul job chiamato **Post welcome comment** per vedere i log completi.


<details>
<summary>Hai problemi? 🤷</summary><br/>

- Controlla la scheda **Actions** per i dettagli e gli errori dell'esecuzione del workflow.

</details>
