---
title: Pubblico avanzato (Beta)
description: Scopri come utilizzare Smart audience (Beta) per creare elenchi di account, aggiungere dati CRM e segnali di crescita, assegnare priorità ai lead e aggiungerli a un flusso di lavoro in uscita.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
badgeBeta: label="Beta" type="Informative"
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%
---

# Pubblico avanzato (Beta)

Smart audience (Beta) consente di trovare gli account e le persone che lavoreranno successivamente in [!DNL Adobe Marketo Qualifier]. Descrivi il pubblico in un linguaggio semplice, perfeziona l’elenco degli account con dati CRM e segnali di crescita, trova lead rilevanti e aggiungi lead selezionati a un flusso di lavoro in uscita.

Utilizza la vista a elenco con la relativa griglia, i filtri e i pulsanti, oppure usa la chat per descrivere cosa desideri. Entrambi lavorano sullo stesso elenco: le modifiche in uno vengono visualizzate nell’altro. Se una modifica non viene visualizzata immediatamente, selezionare **[!UICONTROL Aggiorna]**.

Il tracciatore dell&#39;avanzamento nella parte superiore di ogni elenco mostra tre fasi: **[!UICONTROL Crea elenco smart audience]**, **[!UICONTROL Assegna priorità ai lead]** e **[!UICONTROL Aggiungi al flusso di lavoro in uscita]**.

## Prima di iniziare

Il pubblico avanzato richiede un Salesforce o un CRM Microsoft Dynamics 365 connesso. Legge i dati CRM in tempo reale e non scrive nel CRM. Per istruzioni sulla connessione, vedere [Introduzione](getting-started.md#connect-your-crm).

Puoi creare fino a 100 elenchi. Ogni elenco contiene fino a 500 account e 2.000 lead. Gli account o i lead che superano tali limiti non vengono aggiunti. Restringi i criteri o dividi il pubblico in diversi elenchi, ad esempio per regione o segmento.

## Descrivere e visualizzare in anteprima gli account

Inizia con una descrizione degli account che desideri raggiungere. L’anteprima non salva un elenco.

1. Apri **[!UICONTROL Pubblico avanzato]** e seleziona **[!UICONTROL Nuovo pubblico avanzato]** o **[!UICONTROL Crea elenco]**.
1. In chat, descrivi gli account desiderati. Immettere ad esempio `Find healthcare accounts with revenue over $50M`.
1. Esamina il numero di account corrispondenti e il campione nell’anteprima.

La richiesta può includere i seguenti criteri:

| Criteri | Esempi |
| --- | --- |
| Firmografica | Settore, numero di dipendenti, ricavi annui, tipo di conto e valutazione |
| Posizione | Area geografica, paese, stato o città |
| Proprietà | Account o account assegnati a un proprietario con nome |
| Pipeline | Account con o senza opportunità aperta, soggetti ai [limiti Salesforce](#current-scope-and-limits) |
| Dettagli dell’account | Nome, sito Web o dominio e numero di account |

Altre richieste di esempio includono:

* `Accounts in the US with more than 1000 employees`
* `My accounts in Germany or France`
* `Accounts with no open opportunity`

Se parte di una richiesta non può essere applicata ai dati CRM, la chat identifica la condizione saltata. L’anteprima riflette solo le condizioni applicate. Esamina queste omissioni prima di salvare.

## Salvare o perfezionare l’anteprima

Salva l’anteprima quando corrisponde al pubblico previsto.

1. Per modificare l’anteprima, invia una nuova richiesta con le condizioni desiderate. Non viene salvato nulla finché non si conferma.
1. Quando l’anteprima è pronta, chiedi a chat di salvarla come elenco e assegna un nome all’elenco.
1. Esaminare gli account salvati nella scheda **[!UICONTROL Account]**.

È possibile rinominare un elenco dalla relativa pagina. Per eliminare un elenco, aprirlo e selezionare **[!UICONTROL Elimina elenco smart audience]**.

>[!CAUTION]
>
>L’eliminazione di un elenco rimuove definitivamente i relativi account, lead e colonne da Smart audience. Non elimina i record CRM.

## Arricchire e selezionare gli account

Aggiungi colonne di informazioni per aiutarti a decidere quali account utilizzare. Richiedi una colonna o un segnale per richiesta.

Per aggiungere informazioni CRM, immettere una richiesta quale `Add a column showing which accounts have an open opportunity`. Vedi [Limiti e ambito correnti](#current-scope-and-limits) per le restrizioni di Salesforce.

Per aggiungere segnali di crescita, selezionare **[!UICONTROL Arricchisci account]** nella visualizzazione elenco o Chiedi in chat. I segnali disponibili includono:

| Segnale | Cosa mostra |
| --- | --- |
| Finanziamento | Finanziamenti ed eventi di finanziamento recenti |
| Assunzione | Aperture di nuovi lavori e domanda di assunzione recenti |
| Segnali di espansione | Nuovi uffici, nuovi mercati e annunci di espansione |
| Modifiche tecnologiche | Aggiunte e modifiche allo stack tecnologico di un&#39;azienda |
| Licenziamenti | Informazioni sul licenziamento richieste tramite chat |

Immettere ad esempio `Which of these accounts have raised funding recently?` o `Which of these accounts have had layoffs?`.

Negli elenchi di grandi dimensioni, l’aggiunta di un segnale può richiedere alcuni minuti. Segui l’avanzamento mostrato nell’elenco, controlla ogni nuova colonna e mantienila o eliminala.

Per limitare e assegnare la priorità agli account:

1. Nella scheda **[!UICONTROL Account]** aprire **[!UICONTROL Filtri]**.
1. Filtra per account, dominio, settore, proprietario, dipendenti minimi o massimi, ricavi minimi o massimi o colonne personalizzate. Le colonne personalizzate sono le colonne CRM e di segnale aggiunte. Ad esempio, filtrare gli account in cui la colonna Assunzione è impostata su `Yes`.
1. Facoltativamente, selezionare **[!UICONTROL Assegna priorità agli account]** per classificare gli account in base al punteggio.
1. Rimuovere gli account che non si desidera utilizzare.

I filtri vengono salvati con l’elenco. I lead vengono trovati solo per gli account filtrati, pertanto imposta i filtri account prima di assegnare la priorità ai lead.

## Trovare e assegnare la priorità ai lead

Trova le persone pertinenti agli account che hai selezionato. In **[!UICONTROL Assegna priorità ai lead]**, scegli un predefinito o descrivi le persone che desideri nella chat.

| Predefinito | Contatti trovati |
| --- | --- |
| **[!UICONTROL Contatti commerciali]** | Responsabile vendite e contatti responsabile vendite |
| **[!UICONTROL Contatti marketing]** | Vicepresidente dei contatti del Marketing and Marketing Manager |
| **[!UICONTROL Contatti prodotto]** | SVP Contatti per Product Manager |
| **[!UICONTROL Contatti per la tecnologia]** | Direttore IT e vicepresidente Contatti tecnici |
| **[!UICONTROL Tutti i contatti CRM]** | Ogni contatto disponibile presso gli account, fino al limite di 2.000 contatti |

Per una richiesta di chat, immettere `Find VP and Director level people at these accounts`, `Find C-level executives (CEO, CTO, CFO) at these accounts` o `Find managers at these accounts`.

Esamina i risultati nella scheda **[!UICONTROL Lead]**. Ogni lead mostra il proprio nome, titolo, account, e-mail, proprietario e punteggio. Filtra per anzianità, se è disponibile un indirizzo e-mail, punteggio minimo o massimo o se il lead si trova in un flusso di lavoro. La colonna **[!UICONTROL Motivazione]** spiega perché ogni lead è classificato nella posizione in cui si trova.

### Funzionamento dei punteggi

I punteggi variano da 0 a 100. Un punteggio più alto indica una migliore adesione e una maggiore prontezza al coinvolgimento. Gli stessi dati producono lo stesso punteggio.

Un punteggio combina:

* **Adatta**: l&#39;account corrisponde al profilo cliente ideale, ad esempio il settore e le dimensioni.
* **Segnali di acquisto e crescita**: segnali quali assunzione, finanziamenti e cambiamenti di leadership. I segnali recenti contano di più.
* **Contesto di vendita**: contesto quale un cliente esistente con opportunità di espansione.

Rivedi il ragionamento e i dati disponibili prima di decidere chi contattare.

## Aggiungere lead a un flusso di lavoro in uscita

Dopo aver esaminato i lead, aggiungi quelli desiderati a un flusso di lavoro in uscita esistente.

1. Nella scheda **[!UICONTROL Lead]**, filtra e seleziona i lead desiderati. Ad esempio, seleziona i lead con un indirizzo e-mail e un punteggio minimo di 70.
1. Seleziona **[!UICONTROL Aggiungi al flusso di lavoro in uscita]**.
1. Scegli il flusso di lavoro e conferma.
1. Rivedi la conferma. La colonna **[!UICONTROL Flusso di lavoro]** mostra **[!UICONTROL Assegnato]** per i lead aggiunti.

Puoi anche chiedere a chat di aggiungere i lead a un flusso di lavoro per nome. Se non conosci il nome, chiedi alla chat di elencare i flussi di lavoro disponibili. Controlla il nome del flusso di lavoro e il numero di lead nella risposta.

L’aggiunta di lead non sostituisce la revisione e l’approvazione delle e-mail. Segui i passaggi per [esaminare le e-mail generate](outbound-workflows.md#review-and-refine-generated-emails) e [approvare e iscrivere i potenziali clienti](outbound-workflows.md#approve-and-enroll-prospects) prima dell&#39;invio dell&#39;estensione.

## Ambito di applicazione e limiti attuali

Durante il Beta, tieni presente i seguenti limiti:

* Richiedi una colonna o un segnale per richiesta.
* Il pubblico avanzato utilizza i campi dell’account CRM standard. I campi CRM personalizzati non sono supportati.
* Il filtro in base ai prodotti di cui è proprietario un account non è supportato.
* Per Salesforce, non è disponibile la ricerca di account con un’opportunità aperta. Trovare account senza opportunità aperta funziona con entrambi i CRM.
* Per Salesforce, non sono disponibili richieste di assunzione per un ruolo specifico, ad esempio rappresentanti commerciali.

>[!MORELIKETHIS]
>
>* [Account](accounts.md)
>* [Potenziali clienti](prospects.md)
>* [Flussi di lavoro in uscita](outbound-workflows.md)
>* [Chat IA](ai-assistant.md)
