# Nyktifaes — Quickstart Guide

Guida rapida per lavorare efficacemente sul completamento del romanzo Nyktifaes.

---

## 🎯 Panoramica

Questo documento ti guida attraverso il flusso di lavoro completo, distinguendo tra:
- **Setup** → attività preliminari da fare una volta sola
- **Scrittura** → ciclo iterativo per produrre nuovi contenuti

---

## 📦 SETUP (Da fare una volta)

Questi step creano la **base di conoscenza** necessaria per scrivere in modo coerente e fedele. 

**Stato attuale**: ✅ **STEP 1–3 completati (stile, indice, cap_01)**

---

### STEP 1: Studio dello Stile (CRITICO)

**Obiettivo**: Estrarre e documentare le caratteristiche stilistiche del testo originale.

**Input necessario**:
- File `original/Nyktifaes.pdf` (pagine 1-180)

**Come eseguire**:
```
@nyktifaes #prompt:analizza-stile #file:original/Nyktifaes.pdf

Analizza le prime 180 pagine del testo originale.
Concentrati su: tono, ritmo, struttura frasi, descrizioni, dialoghi.
```

**Output**: File `stile_nyktifaes.md` nella root del progetto

**Verifica**: Il file deve contenere esempi concreti (citazioni) e regole stilistiche estratte, NON giudizi o proposte di miglioramento.

---

### STEP 2: Indice dell'Opera Esistente

**Obiettivo**: Catalogare i capitoli già scritti con contenuti e personaggi.

**Input necessario**:
- File `original/Nyktifaes.pdf` (pagine 1-180)

**Come eseguire**:
```
@nyktifaes 

Analizza le pagine 1-180 e crea indice_opera.md con:
- Numero capitolo
- Range pagine
- Contenuto principale
- Personaggi coinvoltiai
```

**Output**: File `indice_opera.md` nella root del progetto

**Verifica**: L'indice deve coprire tutti i capitoli esistenti in modo schematico.

---

### STEP 3: File per Capitoli Esistenti

**Obiettivo**: Creare struttura organizzata per ogni capitolo già scritto.

**Input necessario**:
- File `indice_opera.md` (creato nello step 2)
- File `converted/Nyktifaes.md`

**Come eseguire**:
```
@nyktifaes

Basandoti su #file:indice_opera.md, per ogni capitolo esistente:
1. Crea cartella capitoli/cap_XX/
2. Genera riassunto.md (narrativo, 1-2 paragrafi)
3. Genera eventi.md (schematico, bullet points)

Inizia dal capitolo 1.
```

**Output**: 
```
capitoli/
├─ cap_01/
│  ├─ riassunto.md
│  └─ eventi.md
├─ cap_02/
│  ├─ riassunto.md
│  └─ eventi.md
└─ ...
```

**Verifica**: Ogni cartella deve avere entrambi i file, fedeli al testo originale.

---

### STEP 4: Timeline Originale (Appunti Grezzi)

**Obiettivo**: Estrarre cronologia eventi dagli appunti senza interpretarli.

**Input necessario**:
- File `converted/Nyktifaes.md` (pagine 180+, appunti grezzi)

**Come eseguire**:
```
@nyktifaes #prompt:estrai-timeline #file:original/Nyktifaes.pdf

Estrai timeline dagli appunti dopo pagina 180.
NON razionalizzare, NON risolvere ambiguità.
Evidenzia contraddizioni ma non proporre soluzioni.
```

**Output**: File `timeline_originale.md` nella root del progetto

**Verifica**: Il file deve preservare il linguaggio grezzo degli appunti, segnalando dubbi e incongruenze **senza risolverle**.

---

### STEP 5: Mappatura Personaggi

**Obiettivo**: Creare schede dettagliate per tutti i personaggi.

**Input necessario**:
- File `original/Nyktifaes.pdf` (completo)
- File `capitoli/*/riassunto.md` (creati nello step 3)

**Come eseguire**:
```
@nyktifaes #prompt:mappa-personaggi #file:original/Nyktifaes.pdf

Crea personaggi.md con scheda per ogni personaggio (anche minori).
Includi: ruolo, relazioni, arco narrativo, citazioni significative.
```

**Output**: File `personaggi.md` nella root del progetto

**Verifica**: Ogni personaggio deve avere sezioni complete, con segnalazione esplicita di informazioni mancanti o ambigue.

---

### STEP 6: Timeline Estesa (Interpretata)

**Obiettivo**: Creare versione strutturata e interpretata della timeline.

**Input necessario**:
- File `timeline_originale.md` (creato nello step 4)
- File `personaggi.md` (creato nello step 5)

**Come eseguire**:
```
@nyktifaes

Basandoti su #file:timeline_originale.md, crea timeline_estesa.md.

Organizza gli eventi in:
- Eventi certi (espliciti negli appunti)
- Eventi probabili (inferibili dal contesto)
- Eventi incerti (ambigui o contraddittori)

Mantieni riferimenti agli appunti originali.
```

**Output**: File `timeline_estesa.md` nella root del progetto

**Verifica**: La distinzione certi/probabili/incerti deve essere chiara. Nessuna invenzione narrativa.

---

### STEP 7: Inizializza Progresso

**Obiettivo**: Creare file di tracciamento del lavoro.

**Come eseguire**:
```
@nyktifaes

Crea _agent_progress.md con:
- Data inizio progetto
- Step completati
- File generati
- Stato attuale: "Setup completato, pronto per scrittura"
- Prossimi step: "Identificare primo capitolo da scrivere"
```

**Output**: File `_agent_progress.md` nella root del progetto

**Verifica**: Il file deve essere aggiornato dopo ogni sessione di lavoro.

---

## ✍️ SCRITTURA (Ciclo iterativo)

Questi step vanno ripetuti **per ogni capitolo o sezione da scrivere**.

**Prerequisiti**: Tutti gli step di setup devono essere completati.

---

### PRE-SCRITTURA: Identifica il Capitolo

**Obiettivo**: Decidere quale capitolo scrivere e verificare prerequisiti.

**Come eseguire**:
```
@nyktifaes

Basandoti su #file:timeline_estesa.md e #file:indice_opera.md:
- Qual è il prossimo capitolo logico da scrivere?
- Quali capitoli precedenti sono prerequisiti?
- Quali personaggi sono coinvolti?
- Quali eventi devono accadere secondo gli appunti?
```

**Output**: Proposta di capitolo con analisi preliminare

**Decisione**: L'utente conferma quale capitolo scrivere.

---

### STEP 1: Preparazione Contesto

**Obiettivo**: Raccogliere tutto il materiale di riferimento necessario.

**Come eseguire**:
```
@nyktifaes

Prima di scrivere il capitolo [XX]:

1. Riassumi i capitoli precedenti rilevanti
2. Elenca gli eventi da includere (da timeline_estesa.md)
3. Mostra le schede dei personaggi coinvolti (da personaggi.md)
4. Evidenzia caratteristiche stilistiche da preservare (da stile_nyktifaes.md)
```

**Output**: Documento di contesto per il capitolo

**Verifica**: Tutto il materiale necessario è presente e non ci sono contraddizioni evidenti.

---

### STEP 2: Scrittura Bozza

**Obiettivo**: Scrivere il testo del capitolo.

**Come eseguire**:
```
@nyktifaes

Scrivi una bozza del capitolo [XX] seguendo:
- Eventi da #file:timeline_estesa.md
- Stile da #file:stile_nyktifaes.md
- Personaggi da #file:personaggi.md
- Riassunti capitoli precedenti

Lunghezza: [specificare, es. 3-5 pagine]

Principio guida: fedeltà > qualità tecnica.
```

**Output**: Testo proposto per il capitolo

**Nota**: L'agente propone, tu rivedi e decidi.

---

### STEP 3: Verifica Coerenza

**Obiettivo**: Controllare che la bozza sia coerente con l'opera esistente.

**Come eseguire**:
```
@nyktifaes #prompt:verifica-coerenza

Verifica la coerenza della bozza del capitolo [XX]:
#file:capitoli/cap_XX/bozza.md
#file:stile_nyktifaes.md
#file:timeline_estesa.md
#file:personaggi.md
```

**Output**: Report di verifica con eventuali problemi rilevati

**Azione**: Correggi i problemi identificati prima di procedere.

---

### STEP 4: Revisione e Approvazione

**Obiettivo**: Revisione umana e approvazione finale.

**Attività**:
1. Leggi la bozza attentamente
2. Verifica che "suoni uguale" al testo originale
3. Controlla che rispetti gli appunti dell'autore
4. Apporta modifiche manuali se necessario

**Domande guida**:
- Questo pezzo potrebbe essere stato scritto dall'autore originale?
- Ci sono modernismi o espressioni fuori tono?
- Gli eventi seguono la logica degli appunti?
- I personaggi agiscono coerentemente?

---

### STEP 5: Salvataggio Definitivo

**Obiettivo**: Salvare la versione approvata.

**Come eseguire**:
```
[Manuale]

1. Salva la versione finale in capitoli/cap_XX/testo.md
2. Aggiorna capitoli/cap_XX/riassunto.md se necessario
3. Aggiorna capitoli/cap_XX/eventi.md se necessario
```

---

### STEP 6: Aggiornamento Progresso

**Obiettivo**: Documentare il lavoro svolto.

**Come eseguire**:
```
@nyktifaes

Aggiorna #file:_agent_progress.md con:
- Data completamento capitolo [XX]
- Decisioni narrative prese
- Eventuali dubbi o ambiguità rimaste
- Prossimo capitolo previsto
```

**Output**: File `_agent_progress.md` aggiornato

---

### STEP 7: Ciclo Successivo

**Obiettivo**: Passare al prossimo capitolo.

**Azione**: Torna allo step "PRE-SCRITTURA: Identifica il Capitolo" e ripeti il ciclo.

---

## 🛠️ Comandi Rapidi

### Setup Completo (esegui in sequenza)
```bash
# 1. Analisi stile
@nyktifaes #prompt:analizza-stile #file:original/Nyktifaes.pdf

# 2. Indice opera
@nyktifaes [genera indice_opera.md]

# 3. Riassunti capitoli
@nyktifaes [genera struttura capitoli/]

# 4. Timeline originale
@nyktifaes #prompt:estrai-timeline #file:original/Nyktifaes.pdf

# 5. Mappatura personaggi
@nyktifaes #prompt:mappa-personaggi #file:original/Nyktifaes.pdf

# 6. Timeline estesa
@nyktifaes [genera timeline_estesa.md da timeline_originale.md]

# 7. Inizializza progresso
@nyktifaes [crea _agent_progress.md]
```

### Scrittura Capitolo (esegui in sequenza)
```bash
# 1. Identifica capitolo
@nyktifaes "Quale capitolo scrivere dopo?"

# 2. Prepara contesto
@nyktifaes "Prepara contesto per capitolo [XX]"

# 3. Scrivi bozza
@nyktifaes "Scrivi bozza capitolo [XX]"

# 4. Verifica coerenza
@nyktifaes #prompt:verifica-coerenza #file:capitoli/cap_XX/bozza.md

# 5. Revisione manuale
[Leggi, correggi, approva]

# 6. Aggiorna progresso
@nyktifaes "Aggiorna _agent_progress.md: completato capitolo [XX]"
```

---

## 📁 Struttura File Finale

Quando il setup è completato, la struttura del progetto sarà:

```
/nyktifaes/
│
├─ README.md                    # Filosofia del progetto
├─ _agent_progress.md           # 📝 Stato lavoro (aggiornato continuamente)
│
├─ stile_nyktifaes.md           # ✅ SETUP STEP 1
├─ indice_opera.md              # ✅ SETUP STEP 2
├─ timeline_originale.md        # ✅ SETUP STEP 4
├─ timeline_estesa.md           # ✅ SETUP STEP 6
├─ personaggi.md                # ✅ SETUP STEP 5
│
├─ capitoli/                    # ✅ SETUP STEP 3 + SCRITTURA
│  ├─ cap_01/
│  │  ├─ riassunto.md
│  │  ├─ eventi.md
│  │  └─ testo.md              # [già esistente nel PDF originale]
│  ├─ cap_02/
│  │  └─ ...
│  └─ cap_XX/                   # [da scrivere]
│     ├─ riassunto.md
│     ├─ eventi.md
│     └─ testo.md               # ✍️ nuovo contenuto
│
├─ ai/
│  ├─ ai-steps.md               # Metodologia completa
│  └─ quickstart.md             # ← Questo file
│
├─ .github/
│  ├─ copilot-instructions.md
│  ├─ agents/
│  │  └─ nyktifaes.agent.md    # Agente personalizzato
│  └─ prompts/
│     ├─ analizza-stile.prompt.md
│     ├─ estrai-timeline.prompt.md
│     ├─ mappa-personaggi.prompt.md
│     └─ verifica-coerenza.prompt.md
│
└─ original/
   ├─ Nyktifaes.pdf             # Testo originale + appunti
   └─ ...
```

---

## ⚠️ Checklist Prima di Iniziare

### Prima del Setup:
- [ ] Il file `original/Nyktifaes.pdf` è presente e leggibile
- [ ] Hai attivato l'agente **@nyktifaes** in GitHub Copilot
- [ ] Hai letto `README.md` e `ai/ai-steps.md`

### Prima della Scrittura:
- [ ] Tutti i 7 step di setup sono completati
- [ ] I file di riferimento sono nella root del progetto
- [ ] Il file `_agent_progress.md` esiste ed è aggiornato

### Prima di Approvare un Capitolo:
- [ ] Hai letto la bozza almeno due volte
- [ ] Hai eseguito la verifica di coerenza
- [ ] Il testo "suona uguale" all'originale
- [ ] Nessun evento contraddice gli appunti

---

## 🎓 Principi da Ricordare

1. **Fedeltà > Qualità**: Se suona meglio ma diverso, non va bene.
2. **Appunti = Sacri**: Gli appunti grezzi non vanno "migliorati".
3. **Piccoli passi**: Un capitolo alla volta, con verifica continua.
4. **Documenta tutto**: Ogni decisione va tracciata in `_agent_progress.md`.
5. **L'autore sei tu**: L'agente propone, tu decidi sempre.

---

## 🆘 Troubleshooting

### "L'agente @nyktifaes non viene riconosciuto"
- Verifica che il file `.github/agents/nyktifaes.agent.md` esista
- Riavvia VS Code
- Controlla di essere nel workspace corretto

### "Il file generato non è fedele allo stile"
- Verifica che `stile_nyktifaes.md` esista e sia stato allegato
- Richiedi esplicitamente fedeltà: "Scrivi come l'autore originale, NON migliorare"
- Rivedi manualmente e correggi

### "Ci sono contraddizioni tra appunti"
- È normale. Segnalale in `_agent_progress.md`
- Chiedi chiarimenti se necessario
- Non risolvere autonomamente contraddizioni strutturali

### "Un capitolo è troppo lungo/corto"
- Controlla i capitoli originali per avere un riferimento di lunghezza
- Suddividi o espandi mantenendo lo stile
- Non sacrificare la fedeltà per raggiungere una lunghezza target

---

## 📚 Risorse di Riferimento

- **Filosofia del progetto**: `README.md`
- **Metodologia completa**: `ai/ai-steps.md`
- **Agente personalizzato**: `.github/agents/nyktifaes.agent.md`
- **Prompt disponibili**: `.github/prompts/README.md`

---

**Ultima modifica**: 2026-01-08  
**Versione**: 1.0  
**Stato setup**: ❌ Da iniziare

---

> **Ricorda**: Non stai riscrivendo Nyktifaes. Stai permettendole di arrivare alla fine senza distorsioni.
