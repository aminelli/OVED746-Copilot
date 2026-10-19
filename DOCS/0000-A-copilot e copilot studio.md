# Copilot e Copilot Studio

Nel mondo Microsoft, **Copilot** e **Copilot Studio** sono due prodotti complementari ma con scopi molto diversi.

## In sintesi

- **Microsoft Copilot** = l'assistente AI che gli utenti finali utilizzano.
- **Microsoft Copilot Studio** = la piattaforma con cui amministratori, analisti e sviluppatori creano, personalizzano ed estendono i Copilot.

Un paragone semplice:

| Concetto | Esempio |
|-----------|----------|
| Copilot | L'auto che guidi |
| Copilot Studio | L'officina con cui costruisci e modifichi l'auto |

---

### 1. Microsoft Copilot

Microsoft Copilot è l'assistente AI basato su LLM che aiuta gli utenti nelle attività quotidiane.

Può essere utilizzato in:

- Microsoft 365
- Teams
- Outlook
- Word
- Excel
- PowerPoint
- OneNote
- Power Platform
- Dynamics 365
- Azure
- Security Copilot

L'utente interagisce tramite linguaggio naturale:

Esempi:

- "Riassumi questa riunione Teams"
- "Genera una presentazione PowerPoint"
- "Analizza questo foglio Excel"
- "Scrivi una risposta a questa email"
- "Crea una tabella pivot"

In questo caso l'utente **consuma** funzionalità AI già pronte.

---

### 2. Copilot Studio

Copilot Studio è la piattaforma low-code Microsoft utilizzata per:

- creare Copilot personalizzati
- estendere Microsoft 365 Copilot
- creare chatbot aziendali
- collegare sistemi esterni
- implementare automazioni
- orchestrare processi business

In pratica permette di costruire il comportamento del Copilot.

---

## Architettura concettuale

```text
Utente
   │
   ▼
Microsoft 365 Copilot
   │
   ├── Dati Microsoft 365
   │
   ├── Copilot Studio
   │      │
   │      ├── Knowledge Base
   │      ├── Prompt
   │      ├── Actions
   │      ├── Plugins
   │      └── Agent
   │
   ▼
Sistemi Aziendali
(SAP, Salesforce, Dynamics, API, Database)
```


Cosa posso fare con Copilot Studio?
- Aggiungere conoscenza aziendale

Ad esempio:

- SharePoint
- OneDrive
- PDF
- Siti Web
- Database
- Documentazione tecnica

Domanda:

- Qual è la procedura per aprire un ticket interno?

Il Copilot risponde utilizzando i documenti aziendali.

- Creare azioni

Il Copilot non si limita a rispondere ma può eseguire operazioni.

Esempio:

```text
Utente:

Apri un ticket per il PC guasto.

Copilot:

raccoglie le informazioni
invoca un workflow
apre il ticket in ServiceNow
restituisce il numero pratica
Collegare API
```

Puoi integrare:

- REST API
- SOAP API
- Azure Functions
- Logic Apps
- Power Automate
- Custom Connector

Esempio:

```text
Copilot
   │
   ▼
Action
   │
   ▼
API ERP
   │
   ▼
Restituisce saldo cliente
```

Orchestrare processi

Esempio HR:

```text
Utente:

Assumi Mario Rossi.

Copilot può:

- creare l'utente Entra ID
- assegnare licenze Microsoft 365
- creare la mailbox
- creare il profilo HR
- inviare email di onboarding
- Differenza fondamentale
- Copilot
```

Lavora principalmente come assistente.

```text
Domanda
   ▼
Risposta
```

Copilot Studio permette di trasformare il Copilot in un agente operativo.

```text
Domanda
   ▼
Ragionamento
   ▼
Azioni
   ▼
Sistemi Aziendali
   ▼
Risultato
```


L'uso di Microsoft 365 Copilot + Copilot Studio è lo scenario ad oggi più interessante.

Senza Copilot Studio:

```text
Microsoft 365 Copilot
      │
      └─ Microsoft Graph
```

Il Copilot conosce principalmente:

- email
- calendari
- Teams
- SharePoint
- OneDrive

Con Copilot Studio:

```text
Microsoft 365 Copilot
       │
       ▼
Copilot Studio
       │
       ├─ SAP
       ├─ Dynamics 365
       ├─ Salesforce
       ├─ Database
       ├─ API custom
       └─ Sistemi legacy
```

Si estende l'intelligenza del Copilot all'intero ecosistema aziendale.

Nei casi d'uso che prevedono Power Platform, ad esempio:

```text
Copilot per Microsoft 365 → l'utente usa l'assistente.

Copilot Studio → il maker crea agenti personalizzati all'interno di un environment Power Platform.
```

Gli agenti possono usare:

- Dataverse
- Power Automate
- Connector
- API custom
- Knowledge base SharePoint

## Conclusioni 

Se l'obiettivo è:

"Voglio che gli utenti aziendali interroghino processi e dati della mia organizzazione"

allora ti serve Copilot Studio.

Se invece:

"Voglio che gli utenti usino l'AI in Word, Excel, Outlook e Teams"

allora serve Microsoft 365 Copilot.

Regola pratica:

- Copilot = utilizzo dell'AI.
- Copilot Studio = sviluppo e personalizzazione dell'AI.
- Copilot + Copilot Studio = piattaforma completa per creare agenti aziendali integrati con processi e dati enterprise.