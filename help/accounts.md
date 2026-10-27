---
title: Account in Adobe Marketo Qualifier
description: Scopri come rivedere le informazioni sull’account in Adobe Marketo Qualifier, incluse ricerche sull’intelligenza artificiale, notizie recenti, opportunità e contatti principali coinvolti, per dare priorità all’estensione.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
autotag-review: '2026-10-08T17:56:44.977Z'
TQID: 'https://experienceleague.adobe.com/MQxeaEGw7q8rv57xKg1f-3LahWx1laiawyvaY3n6Ri8'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: ace0d1fc-8e69-4e6a-a442-37fc40985eea
    internal-label: Account Qualification Agent
  - id: 1e0ea71a-a210-5748-9b0f-c02c2ef6a746
    internal-label: Workflows
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
subfeature_v2:
  - id: 0513c3f7-eb4d-5712-8de6-0397686096c8
    internal-label: Accounts
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%
---

# Account

La visualizzazione account combina ricerca generata dall’intelligenza artificiale, notizie recenti, opportunità aperte, valore della pipeline e contatti coinvolti. Utilizza queste informazioni per comprendere e assegnare la priorità a un account prima di contattarlo.

Per trovare e assegnare priorità a più account contemporaneamente, utilizza [Pubblico avanzato (Beta)](smart-audience.md). Crea un elenco di account, perfezionalo con i dati CRM e i segnali di crescita e trova i lead da aggiungere a un flusso di lavoro in uscita.

## Apri un account

Apri un account dal profilo di un potenziale cliente associato.

1. Seleziona **[!UICONTROL Prospect]** nella barra di navigazione a sinistra e apri un prospect. Vedi [Potenziali clienti](prospects.md).
1. Nella pagina dei dettagli del prospect, selezionare la scheda **[!UICONTROL Account]**.

![Pagina dettagli prospect con schede Persona e Account](./assets/account-home.png){width="800" zoomable="yes"}

Adobe Marketo Qualifier identifica l’account dal record CRM del prospect. La stessa visualizzazione account è disponibile da ogni prospect associato a tale account. Se Marketo Qualifier non riesce a trovare un account, nella scheda viene visualizzato _Nessun account trovato_.

>[!NOTE]
>
>Le sezioni e le metriche disponibili dipendono dal CRM in uso, dalla configurazione dell’organizzazione e dai dati dell’account. Se una sezione qui descritta non viene visualizzata, i dati o la funzione richiesti non sono configurati.

La visualizzazione account ha due schede: **[!UICONTROL Dettagli]** e **[!UICONTROL Ricerche account]**.

## Rivedi i dettagli dell’account

La scheda **[!UICONTROL Dettagli]** fornisce un&#39;istantanea dell&#39;account e della relativa pipeline.

### Panoramica dell’account

La scheda panoramica nella parte superiore della scheda identifica l’account e ne riepiloga il valore:

* Il nome e l&#39;area geografica del conto
* **Ricavi ricorrenti annuali (ARR)**: i ricavi ricorrenti annuali per tutti gli abbonamenti attivi. Per esaminare ARR per prodotto nella finestra di dialogo **[!UICONTROL Ricavi ricorrenti annuali]**, seleziona **[!UICONTROL Visualizza tutto]**.
* Statistiche sui conti, inclusi i conteggi di opportunità aperte e contatti e il valore della pipeline

### Riepilogo panoramica account

Il pannello **[!UICONTROL Panoramica account]** riepiloga l&#39;account in base ai dati CRM e alla ricerca Account Qualification Agent. Se la ricerca è in corso, il pannello mostra uno stato di caricamento. Se la ricerca non è disponibile, il pannello mostra un messaggio.

### Informazioni sull’account

Utilizza i pulsanti sotto la panoramica per passare da una visualizzazione all’altra. Le visualizzazioni disponibili dipendono dal CRM e dalla configurazione:

| Visualizzazione | Cosa mostra |
| --- | --- |
| **[!UICONTROL Opportunità]** | Opportunità aperte collegate all’account, con campi chiave per ciascuna. Per visualizzare l&#39;elenco completo in una tabella, selezionare **[!UICONTROL Visualizza tutto]**. I dettagli dell&#39;opportunità, quali l&#39;area di visualizzazione, il tipo e la data di chiusura, possono essere utilizzati anche per filtrare i contatti dell&#39;account in **[!UICONTROL Contatti opportunità personali]** quando un amministratore rende tali campi filtrabili. |
| **[!UICONTROL Membri principali]** | Contatti principali coinvolti dell’account, classificati per coinvolgimento. Ogni contatto mostra la propria qualifica, l’indirizzo e-mail, il punteggio di coinvolgimento e l’indicatore di urgenza. |
| **[!UICONTROL Dati intento]** | Segnali di intento di acquisto per l’account, ad esempio i prodotti e gli argomenti di ricerca dell’account. |
| **[!UICONTROL Membri team account]** | Persone assegnate all’account, con e-mail, qualifica, territorio e gruppo di prodotti. |
| **[!UICONTROL Campi CRM]** | Campi account importati dal CRM, come configurato nella mappatura in entrata. |

I campi che un amministratore rende filtrabili possono essere utilizzati anche per filtrare i contatti in base all’account associato e definire i criteri di targeting per i flussi di lavoro in uscita. Consulta [Integrazioni](integrations.md#map-crm-fields-inbound-mapping).

Dalla visualizzazione **[!UICONTROL Membri principali]**, eseguire una delle azioni seguenti per un contatto:

* **[!UICONTROL Aggiungi al flusso di lavoro in uscita]** - Registra il contatto in un [flusso di lavoro in uscita](outbound-workflows.md).
* **[!UICONTROL Aggiungi a Marketo campaign]** - Attiva una campagna [!DNL Marketo] per il contatto.

## Ricercare l’account

La scheda **[!UICONTROL Ricerca account]** contiene tre aree:

* **[!UICONTROL Categorie di ricerca]**—Argomenti di ricerca. Per visualizzare la ricerca di una categoria nel riquadro centrale, selezionare la categoria.
* **Contenuto ricerca**: schede di ricerca generate dall&#39;intelligenza artificiale raggruppate per categoria. Una scheda può includere il dominio di origine e le date in cui il segnale è stato rilevato per la prima volta e per l’ultima volta.
* **[!UICONTROL Notizie recenti]** - Notizie aggiornate sull&#39;account, incluse date, tag e collegamenti di origine.

![Scheda Ricerca account](./assets/account-detail.png){width="800" zoomable="yes"}

Se non è possibile caricare la ricerca o le notizie, ogni area offre un&#39;azione **[!UICONTROL Ricarica]** per riprovare.

## Utilizzare le informazioni sull’account in outreach

L’intelligenza dell’account è più utile quando determina ciò che invii:

* Fai riferimento a una notizia recente o a un segnale di ricerca per rendere l’apertura rilevante invece di utilizzare un pitch generico.
* Controlla le opportunità aperte e il valore della pipeline per decidere se assegnare la priorità all’account.
* Utilizza **[!UICONTROL Membri principali]** per identificare chi contattare, quindi iscriverli in un flusso di lavoro in uscita.
* Chiedi a [Chat AI](ai-assistant.md) di sviluppare il posizionamento per l&#39;account prima di una chiamata.

>[!MORELIKETHIS]
>
>* [Potenziali clienti](prospects.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
