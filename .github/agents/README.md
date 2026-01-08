# Nyktifaes Guardian - Custom GitHub Copilot Agent

## Descrizione

**Nyktifaes Guardian** è un agente personalizzato di GitHub Copilot progettato specificamente per assistere nel completamento del romanzo fantasy "Nyktifaes", preservando fedelmente la voce e lo stile originali dell'autore.

## Filosofia

Questo agente non è un editor moderno né un miglioratore di stile. È uno strumento per:
- **Completare** un'opera incompiuta, non riscriverla
- **Preservare** la voce originale, non modernizzarla
- **Rispettare** le imperfezioni come parte dell'identità dell'opera
- **Documentare** ogni decisione in modo tracciabile e reversibile

## Caratteristiche

### Principio Supremo
> Se devi scegliere tra "scrivere meglio" e "scrivere più fedele", scegli **SEMPRE** "più fedele".

### Capacità Principali

1. **Analisi Stilistica**: Estrae e preserva le caratteristiche narrative originali
2. **Gestione Timeline**: Mantiene coerenza cronologica degli eventi
3. **Mappatura Personaggi**: Traccia archi narrativi e relazioni
4. **Verifica Coerenza**: Controlla che nuovi contenuti non introducano contraddizioni
5. **Documentazione**: Mantiene traccia di decisioni e progressi

### Vincoli e Divieti

L'agente è programmato per:
- ❌ NON modernizzare il linguaggio
- ❌ NON introdurre cinismo o ironia meta
- ❌ NON "migliorare" gli appunti grezzi dell'autore
- ❌ NON cambiare eventi già stabiliti
- ❌ NON anticipare rivelazioni future

## Come Usare l'Agente

### 1. Attivazione

In GitHub Copilot Chat, seleziona **"Nyktifaes Guardian"** dal menu degli agenti.

### 2. Workflow Consigliato

L'agente segue un flusso di lavoro strutturato in step:

1. **Studio dello stile** → Analisi delle pagine esistenti
2. **Indice dell'opera** → Catalogazione capitoli esistenti
3. **Estrazione timeline** → Cronologia eventi dagli appunti
4. **Mappatura personaggi** → Schede dettagliate
5. **Timeline estesa** → Interpretazione strutturata
6. **Scrittura incrementale** → Nuovi capitoli con verifica continua

### 3. Handoffs Disponibili

L'agente fornisce transizioni guidate:

- **📖 Analizza Stile**: Per estrarre caratteristiche narrative
- **📅 Rivedi Timeline**: Per esaminare cronologia eventi

### 4. File di Output

L'agente genera e mantiene questi file:

```
/nyktifaes/
├─ _agent_progress.md       # Stato lavoro e decisioni
├─ stile_nyktifaes.md       # Caratteristiche stile
├─ indice_opera.md          # Indice capitoli
├─ timeline_originale.md    # Cronologia grezza
├─ timeline_estesa.md       # Timeline interpretata
├─ personaggi.md            # Schede personaggi
└─ capitoli/
   └─ cap_XX/
      ├─ riassunto.md
      ├─ eventi.md
      └─ testo.md
```

## Prompt File Disponibili

Usa questi prompt per task specifici:

- **#prompt:analizza-stile** → Estrazione caratteristiche stilistiche
- **#prompt:estrai-timeline** → Timeline da appunti grezzi
- **#prompt:mappa-personaggi** → Mappatura completa personaggi
- **#prompt:verifica-coerenza** → Controllo coerenza narrativa

## Esempi di Interazioni

### ✅ Interazione Corretta

```
Tu: "Analizza il capitolo 3 e dimmi quali caratteristiche stilistiche 
     devo preservare quando scrivo il capitolo 14."

Agent: "Ho analizzato il capitolo 3. Ecco le caratteristiche stilistiche 
        da preservare:
        - Periodi medi (15-20 parole)
        - Descrizioni visive e sensoriali
        - Dialoghi diretti senza troppi incisi
        - Aperture di scena evocative
        [...]
        Prima di scrivere il capitolo 14, confermi che..."
```

### ❌ Interazione da Evitare

```
Tu: "Riscrivi il capitolo 3 in modo più moderno e scorrevole."

Agent: "Non posso farlo. Il mio ruolo è preservare la voce originale, 
        non modernizzarla. Posso invece aiutarti a..."
```

## Consigli per Ottenere Risultati Migliori

1. **Fornisci Contesto**: Allega i file rilevanti (#file:stile_nyktifaes.md, ecc.)
2. **Lavora Incrementalmente**: Un capitolo/sezione alla volta
3. **Rivedi Sempre**: L'agente propone, tu decidi
4. **Segnala Ambiguità**: Se trovi contraddizioni negli appunti, discutine
5. **Usa i Prompt File**: Per task ripetitivi e strutturati

## Limitazioni

L'agente:
- Non può leggere direttamente i file originali (.odt, .pdf) senza conversione
- Non prende decisioni narrative importanti senza conferma
- Non risolve autonomamente ambiguità negli appunti
- Richiede materiale di riferimento (stile, timeline) prima di scrivere

## Strumenti Disponibili

L'agente ha accesso a:
- **search**: Ricerca nel workspace
- **fetch**: Recupero contenuti file
- **usages**: Analisi riferimenti e dipendenze

## Supporto e Feedback

Per miglioramenti o segnalazioni:
1. Verifica `_agent_progress.md` per lo stato corrente
2. Usa chat per discutere decisioni narrative
3. Documenta problemi o ambiguità incontrate

---

## Quick Start

```bash
# 1. Seleziona l'agente "Nyktifaes Guardian" in Copilot Chat

# 2. Inizia con lo studio dello stile
"Analizza le pagine 1-50 del testo originale e crea stile_nyktifaes.md"

# 3. Crea l'indice dei capitoli esistenti
"Genera indice_opera.md basandoti sui capitoli già scritti"

# 4. Estrai la timeline dagli appunti
#prompt:estrai-timeline #file:appunti.txt

# 5. Mappa i personaggi
#prompt:mappa-personaggi #file:testo_originale.txt

# 6. Scrivi nuovi capitoli
"Basandoti su #file:stile_nyktifaes.md e #file:timeline_estesa.md, 
 proponi una bozza del capitolo 15"
```

---

**Ricorda**: L'obiettivo non è scrivere meglio, ma scrivere **uguale**. La voce originale è il tesoro da preservare.

