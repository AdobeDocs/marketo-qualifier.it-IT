---
title: Impostare gli elementi di rilievo del marketing
description: Scopri come inviare lead da Marketo Engage a Marketo Qualifier con un passaggio di flusso di Campaign intelligente e ottenere consigli sulle caratteristiche di marketing da rivedere.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
subfeature_v2:
  - id: 7b0925d9-0dc0-5c75-a54d-2bcc31c6ebe4
    internal-label: Marketing highlights
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: adcfe279f38ca319589612820351c48af750bad9
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 2%
---

# Configurare gli elementi di rilievo del marketing

Invia lead da [!DNL Adobe Marketo Engage] a [!DNL Adobe Marketo Qualifier] aggiungendo il passaggio di flusso **[!UICONTROL Invia a Marketo Qualifier]** a una campagna avanzata. I rappresentanti visualizzano i lead e l&#39;attività che li ha inviati su **[!UICONTROL Potenziali]** > **[!UICONTROL Marketing Highlights]**.

Il passaggio di flusso funziona con entrambi i tipi di Smart Campaign:

* **Attivare le campagne** invia il coinvolgimento man mano che si verifica, ad esempio aperture e clic delle e-mail, clic sui collegamenti, riempimenti di moduli e visite alle pagine Web.
* **Le campagne batch** inviano i lead qualificati ogni volta che viene eseguita la campagna.

Quando un lead corrisponde ai criteri di targeting di un flusso di lavoro in uscita, Marketo Qualifier consiglia il lead al relativo proprietario nel CRM connesso. Il rappresentante proprietario rivede e approva il lead prima dell’iscrizione e della sensibilizzazione. I lead non vengono iscritti automaticamente.

Marketing Highlights è disponibile in tutte le aree di produzione: Nord America, EMEA e Australia.

## Prima di iniziare {#before-you-begin}

Conferma questi prerequisiti prima di aggiungere il passaggio di flusso:

* Un amministratore di Marketo ha attivato **[!UICONTROL Invia a Marketo Qualifier]** per la tua istanza di Marketo Engage in **[!UICONTROL Amministratore]**.
* Marketo Qualifier è [connesso a Salesforce o Microsoft Dynamics 365](getting-started.md#connect-your-crm), pertanto ogni lead può corrispondere al relativo proprietario CRM.

>[!IMPORTANT]
>
>Il passaggio di flusso **[!UICONTROL Invia a Marketo Qualifier]** non richiede un webhook, un URL di endpoint o credenziali API. Non è necessario accedere al Adobe Developer Console per utilizzarlo. Se il passaggio di flusso non è disponibile, contatta l’amministratore di Marketo.

## Inviare lead con una campagna avanzata {#send-leads-with-a-smart-campaign}

Utilizza una campagna avanzata esistente o creane una per i lead e le attività che desideri inviare.

1. In Marketo Engage, apri una campagna avanzata oppure seleziona **[!UICONTROL Attività di marketing]** > **[!UICONTROL Nuove]** > **[!UICONTROL Campagna avanzata]** per crearne una.
1. Nella scheda **[!UICONTROL Elenco avanzato]**, definisci quali lead sono idonei.

   * Per una campagna trigger, aggiungi i trigger per le attività che desideri inviare, ad esempio **[!UICONTROL Visite alla pagina Web]**, **[!UICONTROL Clic sul collegamento alla pagina Web]** o **[!UICONTROL Clic sul collegamento nell&#39;e-mail]**.
   * Per una campagna batch, aggiungi i filtri per i lead che desideri inviare.

1. Nella scheda **[!UICONTROL Flusso]**, aggiungi il passaggio di flusso **[!UICONTROL Invia a Marketo Qualifier]**.
1. Attiva la campagna trigger oppure esegui o pianifica la campagna batch.
1. In Marketo Qualifier, apri **[!UICONTROL Potenziali]** > **[!UICONTROL Elementi di rilievo marketing]** per esaminare i lead e la loro attività.

   L&#39;attività mostra come è arrivato un lead, ad esempio **[!UICONTROL Aggiunto da una campagna batch]**.

I lead che corrispondono ai criteri di targeting di un flusso di lavoro in uscita sono consigliati solo al proprietario del sistema di gestione delle relazioni con i clienti. Per rivedere i consigli, apri **[!UICONTROL Attività]** > **[!UICONTROL Suggerimenti agente]**. Consulta [Ottieni consigli dagli elementi di rilievo del marketing](outbound-workflows.md#automatically-enroll-prospects-from-marketing-highlights) e [suggerimenti agenti](tasks.md#agent-suggestions).

## Configurazioni del webhook esistenti {#existing-webhook-setups}

Le istruzioni seguenti descrivono la configurazione del webhook precedente. Non sono necessari per il passaggio di flusso **[!UICONTROL Invia a Marketo Qualifier]**. Se la tua organizzazione utilizza già un webhook, collabora con l’amministratore di Marketo e il contatto Adobe prima di modificare tale configurazione.

+++Istruzioni di configurazione del webhook

Queste istruzioni richiedono l&#39;accesso a Adobe Developer Console e a **[!UICONTROL Admin]** in Marketo Engage.

### Parte A: Creare le credenziali API {#part-a-create-api-credentials}

Queste credenziali consentono a [!DNL Marketo] di eseguire l&#39;autenticazione in modo sicuro in Marketo Qualifier.

Per creare le credenziali:

1. Vai a [Adobe Developer Console](https://developer.adobe.com/console/) e accedi con il tuo Adobe ID.
1. Seleziona **[!UICONTROL Crea nuovo progetto]** o apri un progetto esistente.
1. Per rinominare il progetto, selezionare **[!UICONTROL Modifica progetto]**, immettere un nome identificabile come `Marketo Qualifier Marketing Highlights` e selezionare **[!UICONTROL Salva]**.
1. Seleziona **[!UICONTROL Aggiungi API]**, seleziona **[!UICONTROL API Experience Platform]**, quindi seleziona **[!UICONTROL Avanti]**.
1. Scegli **[!UICONTROL OAuth Server-to-Server]** come tipo di autenticazione, quindi seleziona **[!UICONTROL Next]**.

   **[!UICONTROL Server-to-Server OAuth]** consente a [!DNL Marketo] di chiamare l&#39;API Marketo Qualifier direttamente dal server, senza richiedere a una persona di accedere.

1. Immettere un nome di credenziali di almeno 45 caratteri, ad esempio `Marketo Qualifier Marketing Highlights Creds`.
1. Per associare il profilo prodotto, selezionarlo, quindi selezionare **[!UICONTROL Salva API configurata]**.
1. In **[!UICONTROL Credenziali connesse]**, apri le credenziali **[!UICONTROL OAuth Server-to-Server]**. Seleziona **[!UICONTROL Recupera segreto client]**, quindi copia **[!UICONTROL ID client]** e **[!UICONTROL Segreto client]**. Questi valori vengono utilizzati nella [Parte C](#part-c-configure-the-marketo-webhook).

>[!WARNING]
>
>Mantieni il segreto client privato. Considerala come una password e non inviarla tramite e-mail. Utilizza il canale sicuro approvato della tua organizzazione per condividerlo con chiunque configuri il webhook.

### Parte B: Raccogliere endpoint e identificatori {#part-b-gather-your-endpoint-and-identifiers}

Sono necessari tre valori per [Parte C](#part-c-configure-the-marketo-webhook):

* **URL endpoint**: l&#39;indirizzo del webhook Marketo Qualifier della tua area geografica.
* **imsOrg ID** - Identificatore dell&#39;organizzazione nel sistema Adobe Identity Management (IMS), nel formato `{ORG_ID}@AdobeOrg`.
* **Nome sandbox** - Il nome della sandbox AEP esattamente come appare nell&#39;URL di Marketo Qualifier (il valore `sname`), non il nome visualizzato nell&#39;interfaccia utente. Utilizzare il valore URL minuscolo, ad esempio `prod`, non `Prod`.

| Area geografica | URL endpoint webhook |
| --- | --- |
| America del Nord | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC/Australia | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

Se non sei sicuro del tuo paese, ID organizzazione IMS o nome sandbox, il contatto Adobe può confermarli.

### Parte C: Configurare il webhook di Marketo {#part-c-configure-the-marketo-webhook}

Per creare il webhook:

1. In [!DNL Marketo], selezionare **[!UICONTROL Amministratore]** > **[!UICONTROL Webhook]**.
1. Seleziona **[!UICONTROL Nuovo webhook]**.
1. Imposta **[!UICONTROL URL]** sull&#39;URL dell&#39;endpoint per la tua area geografica da [Parte B](#part-b-gather-your-endpoint-and-identifiers).
1. Imposta **[!UICONTROL Tipo di richiesta]** su `POST`.
1. Imposta **[!UICONTROL codifica token richiesta]** su `JSON`. Questa impostazione è obbligatoria.
1. Incolla il modello di payload seguente in **[!UICONTROL Modello]**. Utilizza **[!UICONTROL Inserisci token]** di [!DNL Marketo] per far corrispondere i nomi dei campi nella tua istanza.

   >[!NOTE]
   >
   >Con la codifica JSON, non racchiudere i token di stringa tra virgolette. [!DNL Marketo] li aggiunge automaticamente.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. Seleziona **[!UICONTROL Azioni webhook]** > **[!UICONTROL Imposta intestazione personalizzata]**, quindi aggiungi le intestazioni seguenti, utilizzando i valori di [Parte A](#part-a-create-api-credentials) e [Parte B](#part-b-gather-your-endpoint-and-identifiers):

   | Intestazione | Valore |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | ID client |
   | `x-client-secret` | Segreto client |
   | `x-gw-ims-org-id` | ID della tua organizzazione IMS |
   | `x-sandbox-name` | Nome della sandbox |

   {style="table-layout:auto"}

1. Seleziona **[!UICONTROL Salva]**.

### Parte D: Aggiungere il webhook a un trigger Smart Campaign {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

Aggiungi un passaggio di flusso **[!UICONTROL Chiama webhook]** a un trigger di Smart Campaign, esistente o nuovo. I trigger dell’elenco avanzato per tale campagna determinano le attività da inviare a Marketo Qualifier.

Per aggiungere il webhook:

1. Apri una campagna avanzata attivatore esistente o creane una nuova (**[!UICONTROL Attività di marketing]** > **[!UICONTROL Nuove]** > **[!UICONTROL Campagna avanzata]**).
1. Nella scheda **[!UICONTROL Elenco avanzato]**, aggiungi il trigger o i trigger per le attività che desideri inviare, ad esempio **[!UICONTROL Clic sul collegamento nell&#39;e-mail]**, **[!UICONTROL Compila modulo]** o **[!UICONTROL Pagina Web visite]**.
1. Nella scheda **[!UICONTROL Flusso]**, aggiungi un passaggio **[!UICONTROL Chiama webhook]** e seleziona il webhook creato in [Parte C](#part-c-configure-the-marketo-webhook).
1. Attiva la campagna avanzata.

L’attività di tale campagna avanzata ora scorre in Marketo Qualifier. I rappresentanti visualizzano e filtrano questa attività per **[!UICONTROL Potenziali]** > **[!UICONTROL Elementi di rilievo marketing]**.

+++

>[!MORELIKETHIS]
>
>* [Gestione integrazioni](integrations.md)
>* [Potenziali clienti](prospects.md)
>* [Introduzione](getting-started.md)
