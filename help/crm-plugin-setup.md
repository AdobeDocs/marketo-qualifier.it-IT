---
title: Configurare il plug-in CRM
description: Scopri come installare il plug-in di Marketo Qualifier CRM in Salesforce o Microsoft Dynamics 365. Configurare le azioni Salesforce per flussi di lavoro e campagne Marketo.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
subfeature_v2:
  - id: d2fe5f36-5653-5902-937c-9d3026104284
    internal-label: CRM integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: df256cf271296b82fab2ed10725a0d6bd165e05b
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%
---

# Configurare il plug-in CRM

Installa il plug-in di gestione delle relazioni con i clienti [!DNL Adobe Marketo Qualifier] in modo che i rappresentanti possano utilizzare [!DNL Marketo Sales Insights] e le informazioni generate dall&#39;intelligenza artificiale sulle pagine di record Lead, Contatto e Account senza uscire da Salesforce o Microsoft Dynamics 365. Il plug-in fornisce anche una visualizzazione Home per [assegnare la priorità ai lead nel CRM](admin-settings.md#prioritize-leads-in-the-crm-plugin).

In Salesforce, i rappresentanti possono anche aggiungere potenziali clienti a flussi di lavoro in uscita o campagne Marketo dalle visualizzazioni degli elenchi di lead e contatti e dalle singole pagine dei record.

## Prima di iniziare

Assicurati che gli utenti che installano e utilizzano il plug-in dispongano dell’accesso richiesto:

* **Amministratore Salesforce**: autorizzazione per installare pacchetti e modificare i layout di pagina.
* **Amministratore Microsoft Dynamics 365**: autorizzazione per importare soluzioni nell&#39;ambiente di destinazione in Power Apps.
* **Rappresentanti**: accesso a Marketo Qualifier e ai record CRM pertinenti.

L&#39;installazione del plug-in è separata da [connessione del CRM a Marketo Qualifier](getting-started.md#connect-your-crm).

## Installare in Salesforce

Installa il pacchetto, quindi aggiungi i relativi componenti alle pagine dei record utilizzate dai rappresentanti.

1. Apri la [pagina di installazione di Salesforce](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce) e accedi a Salesforce come amministratore.
1. Nella pagina di installazione del pacchetto, seleziona **[!UICONTROL Installa per tutti gli utenti]**, quindi seleziona **[!UICONTROL Installa]**.

   Puoi comunque controllare l’accesso dei singoli utenti tramite le autorizzazioni di Salesforce.

1. Quando viene richiesto di approvare l&#39;accesso di terze parti, selezionare la casella di controllo di approvazione e selezionare **[!UICONTROL Continua]**.
1. Al termine dell&#39;installazione, selezionare **[!UICONTROL Fine]**.

   L&#39;installazione richiede alcuni minuti. Verificare che il pacchetto sia visualizzato nella pagina **[!UICONTROL Pacchetti installati]**.

1. In Lightning App Builder, modificate le pagine di record Lead, Contatto e Account e aggiungete i componenti Marketo Qualifier.

### Aggiungere azioni alle visualizzazioni elenco

Configura **[!UICONTROL Aggiungi al flusso di lavoro in uscita]** e **[!UICONTROL Aggiungi a Marketo Campaign]** separatamente per le visualizzazioni elenco contatti e lead. Utilizza i pulsanti inclusi nel pacchetto per evitare duplicati.

1. Vai a **[!UICONTROL Configurazione]** > **[!UICONTROL Gestione oggetti]** e seleziona **[!UICONTROL Lead]** o **[!UICONTROL Contatto]**.
1. Apri **[!UICONTROL pulsanti, collegamenti e azioni]** e individua i pulsanti elenco **[!UICONTROL AMQ Aggiungi al flusso di lavoro in uscita]** e **[!UICONTROL AMQ Aggiungi a Marketo Campaign]**.
1. Apri il **[!UICONTROL layout pulsante Vista a elenco]** dell&#39;oggetto e seleziona **[!UICONTROL Modifica]**.

   A seconda della configurazione di Salesforce, il layout della vista a elenco potrebbe trovarsi in **[!UICONTROL Layout ricerca]** > **[!UICONTROL Vista a elenco]**.

1. Sposta entrambi i pulsanti elenco in **[!UICONTROL Pulsanti selezionati]** e salva.
1. Ripetere per l&#39;altro oggetto.

I rappresentanti selezionano uno o più record in una vista a elenco, quindi selezionano l&#39;azione.

### Aggiungere azioni alle pagine di record

Le azioni della pagina record devono essere configurate separatamente dai pulsanti della vista a elenco. Aggiungi entrambe le azioni a ciascun layout di pagina Lead e Contatto in uso.

1. Vai a **[!UICONTROL Configurazione]** > **[!UICONTROL Gestione oggetti]** e seleziona **[!UICONTROL Lead]** o **[!UICONTROL Contatto]**.
1. Apri **[!UICONTROL pulsanti, collegamenti e azioni]** e individua i pulsanti di dettaglio **[!UICONTROL AMQ Aggiungi al flusso di lavoro in uscita]** e **[!UICONTROL AMQ Aggiungi a Marketo Campaign]**.
1. Apri **[!UICONTROL Layout di pagina]** e modifica un layout assegnato ai tuoi rappresentanti.
1. Aggiungi entrambi i pulsanti di dettaglio a **[!UICONTROL Salesforce Mobile e Lightning Experience Actions]** e salva.
1. Ripetere l&#39;operazione per ogni layout applicabile e per l&#39;altro oggetto.

Le azioni vengono visualizzate nella barra delle azioni del record o nel relativo menu e si applicano al record visualizzato.

>[!NOTE]
>
>Queste azioni funzionano in Salesforce Lightning Experience desktop, non nell’app mobile Salesforce. La sezione di layout denominata **[!UICONTROL Salesforce Mobile e Lightning Experience Actions]** viene utilizzata anche per le azioni desktop.

### Sostituire un pulsante mancante

Se manca un pulsante in un pacchetto, crea un sostituto sotto i **[!UICONTROL pulsanti, collegamenti e azioni]** dell&#39;oggetto.

1. Selezionare **[!UICONTROL Nuovo pulsante o collegamento]**.
1. Immettere un&#39;etichetta per l&#39;azione, ad esempio `Add to Outbound Workflow` o `Add to Marketo Campaign`.
1. Scegliere **[!UICONTROL Pulsante elenco]** per una visualizzazione elenco o **[!UICONTROL Pulsante pagina dettagli]** per una pagina record.
1. Imposta **[!UICONTROL Source dei contenuti]** su **[!UICONTROL Pagina Visualforce]** e scegli la pagina delle azioni del pacchetto che corrisponde all&#39;azione, all&#39;oggetto e al posizionamento.

   Le posizioni Elenco lead, Dettagli lead, Elenco contatti e Dettagli contatto utilizzano pagine diverse. Verifica che la pagina selezionata corrisponda al posizionamento che stai configurando.

1. Per un pulsante elenco, selezionare **[!UICONTROL Richiedi selezione riga]**.
1. Salvare il pulsante e aggiungerlo al layout del pulsante della visualizzazione elenco appropriato o alle azioni della pagina record come descritto in precedenza.

### Controlla azioni Salesforce

Dopo aver salvato i layout, verificare che entrambe le azioni vengano visualizzate nelle visualizzazioni elenco Lead e Contatto e nelle pagine record. Verificare ogni azione elenco con i record selezionati e ogni azione pagina record di un singolo record.

Se un’azione non è disponibile o non si apre, utilizza i seguenti controlli:

| Problema | Cosa controllare |
| --- | --- |
| Pulsante mancante in una vista a elenco | Verificare che il pulsante elenco sia in **[!UICONTROL Pulsanti selezionati]** nel **[!UICONTROL layout pulsante visualizzazione elenco]** dell&#39;oggetto corretto e salvare il layout. |
| Pulsante mancante in una pagina record | Conferma che il pulsante Dettaglio si trovi in **[!UICONTROL Salesforce Mobile e Lightning Experience Actions]** sul layout assegnato all&#39;utente. Se l&#39;organizzazione utilizza azioni dinamiche, controllare anche la visibilità delle azioni della pagina del record. |
| Opzione di pagina prevista non disponibile durante la creazione di un pulsante | Verificare che il tipo di visualizzazione sia **[!UICONTROL Pulsante elenco]** per una visualizzazione elenco o **[!UICONTROL Pulsante pagina dettagli]** per una pagina record. |
| L’azione non si apre o mostra un errore di accesso | Conferma che l’utente abbia accesso a Marketo Qualifier e ai record selezionati. |

## Installazione in Microsoft Dynamics 365

Importa il pacchetto del plug-in nell’ambiente in cui lavorano i rappresentanti.

1. Apri la [pagina di installazione di Microsoft Dynamics 365](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics) e scarica il file ZIP del pacchetto.
1. Accedere a [Power Apps](https://make.powerapps.com/) come amministratore e selezionare l&#39;ambiente di destinazione.
1. Apri **[!UICONTROL Soluzioni]** e seleziona **[!UICONTROL Importa soluzione]**.
1. Seleziona **[!UICONTROL Sfoglia]**, scegli il file ZIP scaricato e seleziona **[!UICONTROL Successivo]**.
1. Rivedi i dettagli del pacchetto e seleziona **[!UICONTROL Avanti]**.
1. Mantieni il valore della variabile di ambiente precompilata e seleziona **[!UICONTROL Importa]**.
1. Attendi il messaggio di conferma nella parte superiore della pagina che indica che la soluzione è stata importata correttamente.

L’importazione richiede alcuni minuti.

>[!MORELIKETHIS]
>
>* [Assegna priorità ai lead nel plug-in CRM](admin-settings.md#prioritize-leads-in-the-crm-plugin)
>* [Integrazioni](integrations.md)
>* [Introduzione](getting-started.md)
