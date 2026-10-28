---
title: Note sulla versione di [!DNL Adobe Marketo Qualifier]
description: Scopri le novità di [!DNL Adobe Marketo Qualifier].
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 11%
---
# Note sulla versione di [!DNL Adobe Marketo Qualifier]

## Prossima versione

* Con Smart audience (Beta) puoi trovare e assegnare la priorità agli account e ai lead giusti. Descrivi gli account desiderati in linguaggio semplice, aggiungi dati CRM e segnali di crescita, rivedi i lead con punteggio e aggiungili a un flusso di lavoro in uscita. [Ulteriori informazioni](smart-audience.md).
* Filtra i contatti in base ai campi account, insieme ai campi contatto e opportunità, per trovare i contatti giusti ed eseguire il targeting dei flussi di lavoro in uscita in modo più preciso. [Ulteriori informazioni](prospects.md#filter-and-find-prospects).
* I contatti mostrano il nome dell’account e del proprietario associati; nella pagina di un potenziale cliente sono ora visualizzati 90 giorni di attività di marketing, rispetto ai 30 di prima. [Ulteriori informazioni](prospects.md#review-prospect-details).

## 10-08-2026

Questa versione include:

* Riutilizzare un flusso di lavoro in uscita o modificare i punti di contatto di un flusso di lavoro in esecuzione, duplicarlo e modificare la copia. La copia viene avviata come bozza privata senza prospettive e il flusso di lavoro originale rimane invariato. [Ulteriori informazioni](outbound-workflows.md#duplicate-an-outbound-workflow).
* Configura i flussi di lavoro in uscita in un layout compatto con la navigazione tra obiettivo, targeting, punti di contatto e impostazioni. [Ulteriori informazioni](outbound-workflows.md#create-an-outbound-workflow).
* Le richieste di rinuncia chiare nelle risposte e-mail vengono riconosciute automaticamente. Il prospect è contrassegnato come rinuncia e non vengono inviati ulteriori punti di contatto. [Ulteriori informazioni](outbound-workflows.md#opt-out-requests-in-replies).
* Preparati per le riunioni con un unico resoconto che combina ricerche web e casi di studio di clienti specifici per prodotto, con punti di discussione classificati in base alla rilevanza e alle fonti identificate. [Ulteriori informazioni](prospects.md#generate-meeting-prep).
* Le e-mail generate vengono verificate in base alle linee guida sulla qualità e riscritte quando necessario prima di rivederle. Puoi comunque rivedere, modificare e approvare ogni e-mail prima che venga inviata. [Ulteriori informazioni](outbound-workflows.md#review-and-refine-generated-emails).

## 09-22-2026

Questa versione include:

* Visualizzare [!DNL Marketo Sales Insights] e i dati agente nel plug-in CRM incorporato e aggiungere potenziali clienti a [!DNL Marketo Qualifier]. [Ulteriori informazioni](admin-settings.md#crm-mcp-and-the-embedded-plugin).
* Dai priorità ai lead di gestione delle relazioni con i clienti con gli elementi di maggiore rilevanza, il mio elenco di controllo, l’attività web, il coinvolgimento nelle e-mail e l’attività del webinar. [Ulteriori informazioni](admin-settings.md#prioritize-leads-in-the-crm-plugin).
* Registra automaticamente i potenziali clienti nei flussi di lavoro in uscita quando l&#39;attività live [!DNL Marketo] corrisponde ai criteri del flusso di lavoro. [Ulteriori informazioni](home.md#automatically-enroll-prospects-from-marketing-highlights).
* Rivedi il contesto del prospect, esporta l’elenco dei prospect e visualizza i riepiloghi delle persone di IA per l’analisi nelle istanze di Prime e Ultimate [!DNL Marketo Optimizer]. [Ulteriori informazioni](prospects.md#review-prospect-context-and-export-the-list).
* Rivedi e approva le e-mail dei potenziali clienti generate dalla coda delle attività e rispondi con i suggerimenti degli agenti durante un flusso di lavoro in uscita. [Ulteriori informazioni](tasks.md).

## 09-08-2026

Questa versione include:

* Nelle impostazioni del profilo, imposta il tuo stile di bozza delle e-mail una volta e ogni e-mail generata lo segue. [Ulteriori informazioni](profile-settings.md#email-drafting-context).
* Genera una preparazione riunione personalizzata o basata su obiettivo dalla pagina di un prospect, in una nuova scheda Ricerca riunione. [Ulteriori informazioni](prospects.md#generate-meeting-prep).
* Gli amministratori possono assegnare un flusso di lavoro in uscita a un team e ripristinare le impostazioni predefinite del flusso di lavoro. [Ulteriori informazioni](outbound-workflows.md#create-an-outbound-workflow).
* Mappa i campi personalizzati durante l’importazione di prospect da un CSV e utilizza tali valori nelle e-mail generate. [Ulteriori informazioni](prospects.md#build-your-prospect-list).
* Le e-mail generate utilizzano qualsiasi dato di prospettiva aggiuntivo che importi e possono essere scritte in modo nativo nel linguaggio del potenziale cliente. [Ulteriori informazioni](outbound-workflows.md#step-5-add-prospects-and-start-email-generation).
* Prestazioni in uscita mostra il tasso di apertura e il tasso di clic per impostazione predefinita, con un&#39;opzione per i conteggi non elaborati e i potenziali totali a livello di organizzazione. [Ulteriori informazioni](performance.md).
* Le regole di sincronizzazione CRM aggiornano automaticamente lo stato di CRM quando un potenziale cliente si sposta attraverso un flusso di lavoro in uscita. [Ulteriori informazioni](admin-settings.md#configure-crm-sync-rules).
* Fai domande su Chat AI nei tuoi dati di [!DNL Marketo Qualifier], CRM, [!DNL Marketo] e [!DNL Marketo Optimizer]. [Ulteriori informazioni](ai-assistant.md#ask-ai-chat-across-your-connected-data).

## 08-17-2026

[!DNL Marketo Qualifier] è ora disponibile come app autonoma. Supporta [!DNL Marketo Engage] e [!DNL Marketo Optimizer].

Questa versione include:

* Assegnazione di priorità a potenziali clienti e account con riepiloghi di attività generati dall’intelligenza artificiale e punteggi basati su segnali. [Ulteriori informazioni](prospects.md#review-prospect-details) sui potenziali clienti o [account](accounts.md#account-insights).
* Flussi di lavoro in uscita basati sugli obiettivi con cadenze proposte dall’intelligenza artificiale e bozze di e-mail. [Ulteriori informazioni](outbound-workflows.md).
* Una coda di attività unificata per le telefonate, le e-mail LinkedIn e le revisioni e-mail. [Ulteriori informazioni](tasks.md).
* Prenotazione automatica delle riunioni tramite integrazione del calendario. [Ulteriori informazioni](outbound-workflows.md#meeting-booking).
* Un centro di conoscenza per la messa a terra dell’attività di intelligenza artificiale nei tuoi materiali per il playbook. [Ulteriori informazioni](admin-settings.md#knowledge-center).
* Chat basata su IA per domande in lingua naturale basate sui dati del CRM, del coinvolgimento e del Knowledge Center. [Ulteriori informazioni](ai-assistant.md).
* Rapporti sulle prestazioni di prenotazione di e-mail e riunioni. [Ulteriori informazioni](performance.md).
* Plug-in per browser ed e-mail per l’accesso in CRM o Outlook. [Ulteriori informazioni](admin-settings.md#crm-mcp-and-the-embedded-plugin).
* Supporto per le integrazioni Salesforce e Microsoft Dynamics 365. [Ulteriori informazioni](integrations.md).
