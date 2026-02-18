## Step 5: Unisci e sperimenta

_Ottimo lavoro! Hai creato e testato il tuo primo workflow di GitHub Actions!_ :rocket:

### 📖 Teoria: Quando vengono eseguiti i workflow

Quando crei un workflow in un branch, è abilitato solo per quel branch finché non lo unisci (merge) nel branch predefinito (`main`). Quando un workflow è nel branch predefinito, si applica all'intero repository.

Ogni nuova pull request, indipendentemente dal branch, ora attiverà automaticamente il workflow che hai creato.

> [!TIP]
> Alcuni trigger di eventi, come [workflow_dispatch](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#workflow_dispatch) e [schedule](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#schedule) funzioneranno solo se il file workflow esiste nel branch predefinito.

### ⌨️ Attività: Unire la tua pull request

1. Unisci (merge) la tua pull request nel branch `main`.

1. Prova ad aprire un'altra pull request per vedere il tuo workflow eseguirsi di nuovo!

