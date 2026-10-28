---
title: Potenziali clienti in [!DNL Adobe Marketo Qualifier]
description: Scopri come creare l'elenco di potenziali clienti da CRM, da origini importate e aggiunte manualmente, filtrare i potenziali clienti ed esaminare i dettagli in [!DNL Adobe Marketo Qualifier].
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da87d43a-78d4-4b1e-bb4a-743cbd343472
    internal-label: Prospects
subfeature_v2:
  - id: 6aa13f53-6e49-5228-b98a-64c9ebe5af74
    internal-label: Contacts
  - id: 4143255e-1853-5eb6-a189-dece7126669f
    internal-label: Leads
  - id: 78e1f6f5-7122-5e4d-81c3-d3a90e954414
    internal-label: People lists
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 1%
---

# Potenziali clienti

Per visualizzare i lead e i contatti a cui puoi accedere, seleziona **[!UICONTROL Prospect]** nell&#39;area di navigazione a sinistra. Utilizza l’elenco per rivedere lo stato di ogni prospect e l’ultima attività.

![Tabella dei potenziali clienti con lo stato del lead e l&#39;ultima attività per la gestione dei potenziali clienti](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Lead]** Lead assegnati a te nel CRM connesso.
* **[!UICONTROL Contatti]** Contatti assegnati all&#39;utente nel CRM connesso, con il relativo account associato. I dettagli di contatto includono anche il nome del proprietario. Questi dettagli sono disponibili per Salesforce e Microsoft Dynamics 365.
* **[!UICONTROL Dati di rilievo sul marketing]** potenziali clienti con attività Marketo live, ad esempio aperture di e-mail o clic.
* **[!UICONTROL Elenco persone]** Potenziali importati o aggiunti manualmente.

## Esamina il contesto del prospect ed esporta l’elenco

L’elenco dei potenziali clienti riepiloga se è disponibile un contesto aggiuntivo per la sensibilizzazione personalizzata. Un riepilogo sopra l&#39;elenco mostra il numero di potenziali clienti in ogni stato e la colonna di contesto visualizza lo stato di ogni potenziale cliente:

* **[!UICONTROL Applicato]** Contesto disponibile applicato al prospect.
* **[!UICONTROL Parziale]** È stato applicato solo parte del contesto disponibile.
* **[!UICONTROL Mancante]** Nessun contesto aggiuntivo disponibile.

Per scaricare l&#39;elenco di prospect corrente come file CSV, selezionare **[!UICONTROL Esporta CSV]**.

## Crea il tuo elenco di potenziali clienti

L’elenco dei potenziali clienti combina persone provenienti da più origini:

* **Prospettive CRM**—[!DNL Adobe Marketo Qualifier] importa automaticamente i lead e i contatti assegnati all&#39;utente connesso. Consulta [Integrazioni](integrations.md).
* **Prospect importati** - Prospect importati da un file CSV.
* **Potenziali aggiunti manualmente** - Singoli potenziali aggiunti in Marketo Qualifier.

Per aggiungere potenziali clienti non provenienti dal CRM:

1. Nella pagina **[!UICONTROL Potenziali]**, seleziona **[!UICONTROL Elenco persone]**.

   ![Elenco persone](assets/prospects-people-list.png){width="800" zoomable="yes"}

1. Seleziona **[!UICONTROL + Aggiungi persone]**, quindi seleziona **[!UICONTROL Importa CSV]** o **[!UICONTROL Aggiungi persona]**.

   * Per un&#39;importazione CSV, carica un file CSV nel formato `firstname,email`.
     È necessario specificare il nome e l’indirizzo e-mail. Il cognome è facoltativo. Il modello CSV non include la colonna ID lead CRM, ma puoi aggiungere la colonna e i relativi valori al file prima dell’importazione. Se l’importazione non riesce, controlla il messaggio di errore per individuare i campi o i valori da correggere, quindi carica di nuovo il file.
     Mappa qualsiasi campo CSV personalizzato o aggiuntivo, non solo quelli standard. Marketo Qualifier salva questi valori in ogni prospect e li rende disponibili in un secondo momento, anche per la [generazione e-mail](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
   * Per aggiungere manualmente una persona, inserisci i relativi dettagli nel modulo.

1. Seleziona **[!UICONTROL Salva]**.

## Filtrare e trovare potenziali clienti

Per limitare l&#39;elenco, selezionare **[!UICONTROL Filtro]**. Puoi filtrare per:

* Stato del flusso di lavoro in uscita
* Creato da
* Posizione lavorativa
* Account
* Origine
* Ultimo aggiornamento

Gli amministratori possono anche rendere disponibili come filtri i campi CRM mappati. In **[!UICONTROL Impostazioni amministratore]**, attiva **[!UICONTROL Filtrabile]** per ogni campo utilizzato dagli utenti per trovare potenziali clienti. Vedi [Mappa campi CRM](integrations.md#map-crm-fields-inbound-mapping).

In **[!UICONTROL Contatti opportunità personali]** è inoltre possibile filtrare i contatti in base ai campi dalle opportunità associate, ad esempio area di visualizzazione, tipo e data di chiusura. I campi dell&#39;opportunità hanno etichette come **[!UICONTROL Stage (Opportunità)]**, che li distingue dai campi del contatto. L’amministratore controlla quali campi dell’opportunità sono disponibili come filtri.

Puoi anche filtrare i contatti per campi dal loro account associato, ad esempio settore, area geografica o tipo di account. L’amministratore sceglie i campi dell’account filtrabili. Combina i filtri account, contatto e opportunità per trovare, ad esempio, i contatti in un ruolo specifico presso gli account in un settore specifico. Il filtro dei campi account è disponibile per Salesforce e Microsoft Dynamics 365 e gli stessi campi possono essere utilizzati in [Destinazione flusso di lavoro in uscita](outbound-workflows.md#step-2-configure-targeting-filters).

### Filtra per elementi di rilievo sul marketing

Rivedi e assegna la priorità ai potenziali clienti in base al loro coinvolgimento live [!DNL Marketo], ad esempio attività e-mail, visite web e riempimenti di moduli. Il coinvolgimento appare quasi in tempo reale, come accade.

Per filtrare i potenziali clienti in base alle caratteristiche di marketing:

1. Seleziona **[!UICONTROL Filtro]**.
1. Aggiungi un filtro Marketing Highlights e imposta il tipo di attività, la campagna o altri attributi per concentrarti sul coinvolgimento che conta.

Ogni prospect mostra la sua ultima attività [!DNL Marketo] insieme alla cronologia recente.

Marketing Highlights è disponibile in tutte le aree geografiche di produzione. Un amministratore completa una configurazione una tantum che connette [!DNL Marketo] a Marketo Qualifier. Consulta [Configurare le caratteristiche di marketing](integrations.md#turn-on-marketo-engagement-filtering).

## Rivedi dettagli prospect

Per aprire il profilo di un prospect, selezionarlo. Rivedi i segnali importanti prima di contattare:

* **Riepilogo persona IA**: istantanea scritta da IA del lead o del contatto e del loro impegno recente. Utilizza il riepilogo per comprendere la persona rapidamente prima di rivedere le singole attività. I riepiloghi delle persone di IA sono disponibili nelle istanze che eseguono [!DNL Marketo Optimizer] Prime o Ultimate.
* **Elenco attività**: elenco cronologico che mostra gli ultimi 90 giorni di attività di marketing.
* **Visualizzazione sequenza temporale**: sequenza temporale visiva che mostra gli ultimi 90 giorni di coinvolgimento marketing tra i canali.
* **Contenuto visualizzato**: pagine Web e risorse visualizzate dal prospect. Per aprire un elemento, selezionarlo.

### Genera preparazione riunione

Oltre al riepilogo permanente della persona di intelligenza artificiale, puoi generare una preparazione della riunione personalizzata per una chiamata specifica in arrivo dalla scheda **[!UICONTROL Ricerca riunione]**, accanto a **[!UICONTROL Ricerca account]**.

La preparazione degli incontri combina ricerche sul Web relative al potenziale cliente e alla sua azienda con le evidenze provenienti da casi aziendali sui clienti peer che utilizzano il prodotto che stai vendendo. I punti di discussione dei casi di studio possono includere risultati misurabili per i clienti. Le fonti sono riunite in un&#39;unica sintesi, con punti di discussione classificati per rilevanza. Ogni punto di discussione identifica se proviene da studi di casi, ricerche web, o entrambi. Se non è disponibile alcuna evidenza rilevante di un caso di studio, la preparazione della riunione utilizza la ricerca web.

* **Basato su obiettivo** - Se il prospect è iscritto a un flusso di lavoro in uscita in esecuzione, selezionarlo. La preparazione è allineata all’obiettivo del flusso di lavoro in uscita, ad esempio la prenotazione di una riunione o il coinvolgimento del potenziale cliente.
* **Prompt personalizzato**: immettere gli elementi per cui si desidera prepararsi, ad esempio `Focus on renewal risk` o `Prepare for a technical deep dive with their IT lead`. La preparazione corrisponde al prompt. L’opzione di richiesta personalizzata è disponibile ogni volta che il prospect non si trova in un flusso di lavoro in uscita in esecuzione.

La descrizione continua a seguire l’obiettivo del flusso di lavoro in uscita o il prompt personalizzato scelto. La modalità di generazione della preparazione delle riunioni non viene modificata.

>[!MORELIKETHIS]
>
>* [Account](accounts.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
