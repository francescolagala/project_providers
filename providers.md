### Secondo l'analisi delle specifiche richieste si propongono i seguenti diagrammi:

### ER:
![image](https://image.ibb.co/e1r1M9/ER.png)

### UML:
![image](https://image.ibb.co/bFsDZU/UML.png)

### Use Case:
![image](https://image.ibb.co/hLvT19/UseCase.png)

### PUNTI SALIENTI:
- PM e ASSISTANT:accesso con le credenziali aziendali (Single-Sign-On)

- ASSISTANT: può invitare uno o più providers

- PROVIDER: se riceve un invito può registrarsi attraverso un form. 
A registrazione avvenuta il provider riceverà una password temporanea da personalizzare

- PM: può creare una CAMPAIGN di reclutamento.
All'atto della creazione può selezionare una lista di providers*

- PROVIDER: Se indicato come provider all'atto di creazione di una CAMPAIGN riceve un email di notifica.

- PROVIDER: Può registrare un PROFILE inserendone i dati e allegando un CV.

- PROVIDER: Può associare un PROFILE ad una CAMPAIGN.

- PM: Quando un PROFILE viene associato alla propria CAMPAIGN riceve una email di notifica.

- PM: Può approvare o meno i PROFILE inviati dai PROVIDERS.

- PM: Può chiudere una CAMPAIGN.
All'atto della chiusura i PROVIDERS associati alla campaign e gli ASSISTANT riceveranno una email di notifica.
Nella mail sarà presente una lista dei PROFILE idonei e le indicazioni su come procedere per l'offerta.


NOTES:
*Un futuro sviluppo dovrà prevedere un ranking per i providers con priorità di notifica.


