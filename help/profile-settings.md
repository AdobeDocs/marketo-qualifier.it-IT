---
title: Configura le impostazioni del profilo
description: Scopri come configurare la connessione e-mail, la firma e la disponibilità del calendario nelle impostazioni del profilo di Adobe Marketo Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/YsrBduYA7jKhgxttexqMBBpgDIq23s6wUb4Wp6y6h3g'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: f8c781b4-253f-436e-b9f1-a71172814e41
    internal-label: Profile Settings
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
    internal-label: Email marketing
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 3%
---

# Impostazioni profilo

Nel menu di navigazione a sinistra, espandi **[!UICONTROL Configurazione]** e seleziona **[!UICONTROL Impostazioni profilo]**. Utilizza queste impostazioni per gestire i tuoi dati personali, la connessione e-mail, il calendario e la disponibilità della chat.

![Impostazioni profilo](assets/profile-email-config.png)

## Impostazioni e-mail

Nella scheda **[!UICONTROL Impostazioni e-mail]**, configura le connessioni e-mail.

* **[!UICONTROL Connessioni e-mail]** - Selezionare Microsoft Outlook o Google e seguire la procedura di accesso. Vedere [Connetti Outlook](integrations.md#connect-outlook) per l&#39;accesso che si approva e il percorso di approvazione dell&#39;amministratore, se necessario.
* **[!UICONTROL Firma e-mail]** - Aggiungi o aggiorna la firma utilizzata nelle e-mail generate. Includi il collegamento [prenotazione riunione](outbound-workflows.md#meeting-booking) per consentire ai potenziali clienti di pianificare il tempo con te.
* **[!UICONTROL Collegamento per la prenotazione della riunione]** - Invia un invito alla riunione tramite e-mail. Accetta l’URL della riunione.

### Contesto di bozza e-mail

![Contesto e-mail](assets/profile-email-instructions.png)

Utilizza **[!UICONTROL Contesto di bozza e-mail]** per impostare il tono, la struttura e lo stile dell&#39;e-mail in modo che le e-mail siano coerenti.

Scrivere il contesto in formato normale nell&#39;area **[!UICONTROL Contesto di bozza delle e-mail]**.
Utilizzala per definire:

* Tono e voce
* Struttura e lunghezza
* Personalization e regole di saluto
* Stile oggetto
* Come vengono utilizzati i segnali di coinvolgimento
* Struttura di metriche, punti bozza e storie di clienti

Per impostazione predefinita, le bozze utilizzano un contesto in stile house, pertanto le bozze esistenti non cambiano finché non si aggiunge un contesto personalizzato.

## Configurazione calendario

Nella scheda **[!UICONTROL Configurazione calendario]**, imposta il tuo fuso orario e la tua disponibilità.

* **[!UICONTROL Connessione calendario]**—Seleziona **[!UICONTROL Connetti]** e segui il processo di accesso a Microsoft.
* **[!UICONTROL E-mail di conferma riunione]**—Definisci l&#39;oggetto e il corpo dell&#39;e-mail di conferma che un potenziale cliente riceve dopo la prenotazione di una riunione.
* **[!UICONTROL Preferenze]** - Imposta la durata predefinita della riunione e il buffer tra le riunioni.

Se si disconnette il calendario:

* I collegamenti di prenotazione attivi non funzionano più.
* Nella pagina di prenotazione viene visualizzato un messaggio di indisponibilità temporanea.
* Le impostazioni vengono mantenute quando ci si riconnette.

## Disponibilità del calendario

La disponibilità del calendario in Adobe Marketo Qualifier si basa su due input:

* Calendario di lavoro connesso, ad esempio Outlook o Gmail
* Regole di disponibilità e di tempo nella **[!UICONTROL configurazione calendario]**

Marketo Qualifier legge lo stato di disponibilità, non i dettagli dell&#39;evento, dal calendario connesso. Combina questo stato con le tue regole per determinare gli intervalli di tempo che i potenziali clienti possono prenotare.

Puoi configurare:

* Ore lavorative per giorno della settimana
* Blocchi multipli al giorno, ad esempio 9:00-mezzogiorno e 13:00-5:00.
* Il tuo fuso orario
* Durata riunione
* Buffer prima e dopo le riunioni
* Avviso minimo
* Finestra di prenotazione

>[!MORELIKETHIS]
>
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Integrazioni](integrations.md)
>* [Attività](tasks.md)
