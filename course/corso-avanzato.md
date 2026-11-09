# Corso Claude · Avanzato
### Versione 1.0 · UX Boutique · per designer, sviluppatori, marketing e PM esperti

> Il corso base insegna a usare Claude bene. Questo insegna fin dove ci si può spingere: integrazioni con Figma, Adobe e GitHub, agenti, automazioni, sistemi ripetibili.
> **Premessa:** conoscete già il flusso Delega → Descrivi → Valuta → Rispondi e il metodo BRIEF (corso base).

---

## Indice

**A · Fondamenta avanzate (tutti i ruoli)**
1. Context engineering: cosa vede Claude, e quando
2. Prompt da produzione: specifiche, versioni, test
3. Agenti: subagent, lavori in parallelo, automazioni
4. Sicurezza: permessi, contenuti esterni, segreti

**B · Design**
5. Figma MCP: leggere e scrivere sul canvas
6. Code Connect e design system
7. Adobe: il connettore Adobe for creativity
8. Loghi e identità: fin dove arriva Claude
9. Cosa sì, cosa no: la mappa dei limiti

**C · Sviluppo**
10. Claude Code avanzato: CLAUDE.md, comandi, subagent
11. Hook: le regole che scattano sempre
12. Lavori paralleli con i worktree
13. Automazione: headless e GitHub Action
14. Dal design al codice, senza perdite

**D · Marketing**
15. Un sistema di contenuti, non singoli testi
16. Campagne multicanale con Adobe e Claude Design
17. Ricerca, dati e contenuti in scala

**E · Project management**
18. Il PM con i connettori
19. Report, rischi e stime automatici

**F · Il flusso integrato e la governance**
20. Dal brief al lancio: tutti i ruoli insieme
21. Governance: Skill, plugin e costi del team
22. Esercizi avanzati per ruolo
23. Fonti

---

# A · Fondamenta avanzate

## 1 · Context engineering

A livello avanzato il problema non è più il prompt: è **il contesto**. Claude lavora bene quando ha le informazioni giuste, nel momento giusto, senza rumore.

### I livelli del contesto

| Livello | Quando viene letto | Cosa ci metti | Dove |
|---|---|---|---|
| **Istruzioni di progetto** | A ogni chat o sessione | Regole stabili: brand, stack, divieti | Project (chat), `CLAUDE.md` (Code) |
| **Descrizioni delle Skill** | Sempre, in breve | Nome e quando usarla | `SKILL.md` |
| **Corpo delle Skill** | Solo quando serve | Procedure, criteri, esempi | `SKILL.md` e file collegati |
| **Strumenti (MCP, connettori)** | Quando Claude li usa | Dati vivi: Figma, Drive, GitHub, Adobe | Connettori, `claude mcp add` |
| **Conversazione** | Fino a quando c'è spazio | Il lavoro in corso | La chat o la sessione |

### Regole pratiche
- **Regole stabili in alto, dettagli in basso.** Le regole che valgono sempre vanno nelle istruzioni di progetto. Le procedure lunghe vanno nelle Skill, che si caricano solo quando servono.
- **Il contesto si consuma.** Ogni file letto, ogni risposta di uno strumento occupa spazio. Quando si riempie, la qualità cala. In Claude Code: `/clear` tra un compito e l'altro, `/compact` per riassumere senza perdere il filo.
- **Dai riferimenti, non copie.** "Leggi `design/tokens.json`" è meglio che incollare i token nel prompt: il file resta la fonte unica.
- **Un compito, una sessione.** Due compiti nella stessa sessione si contaminano a vicenda.

---

## 2 · Prompt da produzione

Un prompt che usate ogni settimana non è un messaggio: è una **specifica**. Va trattato come codice.

### Il prompt come specifica
1. **Versione nel repository.** I prompt importanti vivono in file `.md` (o dentro una Skill), con storia Git.
2. **Casi di test.** Per ogni prompt, 5–10 input reali con il risultato atteso o i criteri di accettazione. È la tecnica delle *valutazioni empiriche* del tutorial di Anthropic.
3. **Criteri misurabili.** "Tono giusto" non si misura. "Nessun superlativo, frasi sotto le 25 parole, un solo invito all'azione" sì.
4. **Prova prima di cambiare.** Ogni modifica al prompt si rilancia su tutti i casi di test. Se migliora un caso e ne peggiora due, non è un miglioramento.

### Esempio: file di test per una Skill di copy
```markdown
# Test: post-linkedin-ux-boutique

## Caso 1 · lancio servizio
Input: "Post per il lancio dell'audit di accessibilità"
Criteri: apre con un problema; max 120 parole; nessuna emoji;
nessun numero inventato; elenco "Da verificare" presente.

## Caso 2 · fuori scopo
Input: "Riassumi il verbale interno di ieri"
Criteri: la Skill NON si attiva.
```

### Far lavorare Claude sul prompt
```
<prompt>[prompt attuale]</prompt>
<casi>[i 5 casi di test con gli output ottenuti]</casi>
Analizza dove gli output non rispettano i criteri.
Proponi la modifica minima al prompt che risolve i problemi
senza peggiorare i casi già corretti. Spiega il perché.
```

---

## 3 · Agenti: subagent, lavori in parallelo, automazioni

Un **agente** esegue compiti in più passaggi usando strumenti. Claude Code, Cowork e i connettori sono già agenti. A livello avanzato si combinano.

| Tecnica | Cosa fa | Quando usarla |
|---|---|---|
| **Subagent** | Un aiutante con istruzioni proprie, per un sotto-compito | Ricerche nel codice, revisioni, controlli specialistici |
| **Worktree** | Più copie del repository, ognuna con il suo agente | Lavori lunghi e indipendenti in parallelo |
| **Headless** (`claude -p`) | Claude Code senza interfaccia, dentro uno script | Automazioni e pipeline |
| **GitHub Action** | Claude che lavora su issue e pull request | Revisioni automatiche, issue → pull request |
| **Attività programmate** | Compiti che partono a orari fissi | Report settimanali, controlli periodici |

**Regola d'oro.** Più l'agente è autonomo, più la verifica deve essere automatica: test, controlli, revisione umana prima del merge o della pubblicazione.

---

## 4 · Sicurezza: permessi, contenuti esterni, segreti

Con connettori e agenti, Claude legge contenuti scritti da altri: pagine web, file Figma condivisi, issue, email. Questi contenuti possono contenere istruzioni nascoste (**prompt injection**).

**Regole.**
- **Permessi minimi.** Connettori in sola lettura quando basta. In Claude Code, consenti solo i comandi che servono.
- **Approvazione sulle scritture.** Per i file Figma condivisi e i repository, tieni attiva la conferma prima di ogni modifica.
- **Contenuti esterni = dati, non ordini.** Se un file o una pagina "chiede" a Claude di fare qualcosa, non è una tua istruzione.
- **Segreti fuori dal contesto.** Mai chiavi o password in prompt, file del repository o Skill. Usa variabili d'ambiente e gestori di segreti.
- **Skill e plugin di terzi: leggili prima.** Possono eseguire comandi.

---

# B · Design

## 5 · Figma MCP: leggere e scrivere sul canvas

Il server MCP di Figma collega Claude ai vostri file. A livello avanzato conta una cosa: **ora può anche scrivere**.

### Cosa può fare
| Direzione | Strumento | Cosa fa |
|---|---|---|
| **Lettura** | contesto di design, variabili, screenshot | Legge frame, componenti, token, struttura |
| **Scrittura** | `use_figma` | Crea e modifica contenuti nativi: componenti, variabili, schermate intere, riusando le vostre librerie |

Secondo la documentazione Figma, l'agente lavora con **elementi veri di Figma** (componenti, variabili, auto layout), non immagini piatte.

### Setup in Claude Code
```bash
claude mcp add --transport http figma https://mcp.figma.com/mcp
```
Figma consiglia il server remoto: molti strumenti di scrittura esistono solo lì. Con il connettore Figma di Claude (chat e desktop) l'accesso si attiva dalle impostazioni.

**Condizioni** *(⚠ verifica prima del corso)*:
- La scrittura sul canvas è gratuita durante la beta, poi diventerà a consumo.
- Per modificare un file serve il permesso di modifica su quel file. Alcune fonti indicano che per i file di produzione serve un seat Full.
- I seat Dev bastano per la sola lettura.

### Cosa chiedere: prompt avanzati
**Varianti dal design system:**
```
Nel file [link], pagina "Esplorazioni": crea tre varianti della card
prodotto usando SOLO i componenti e le variabili della libreria
"UXB Core". Variante A densa, B editoriale, C con immagine dominante.
Auto layout ovunque, nessun valore fuori dalle variabili.
Poi elenca i componenti usati e quelli che mancavano.
```

**Audit del design system:**
```
Analizza le pagine del file [link]. Trova: colori e font non collegati
a variabili, componenti staccati dalla libreria, spaziature fuori scala.
Rispondi con una tabella Frame | Problema | Correzione. Non modificare nulla.
```

**Variabili da un brand:**
```
Da questa palette e scala tipografica <brand>…</brand>, crea in una
pagina di prova le collezioni di variabili "Color" (modi Light e Dark)
e "Spacing". Usa nomi semantici (surface, text, accent), non nomi di colore.
```

### Regole
- Scrivi **su una pagina di prova o una copia**, poi sposta tu nel file del team.
- Un compito per richiesta: "crea tre varianti" sì, "rifai tutto il file" no.
- Controlla sempre le variabili usate: un valore staccato rompe il design system.

---

## 6 · Code Connect e design system

**Code Connect** collega i componenti Figma ai componenti nel codice. Senza, il server MCP restituisce dati di layout generici. Con Code Connect restituisce **il vostro componente reale**, gli import e la mappatura delle proprietà.

**Perché conta.** È la differenza tra "Claude ricostruisce un bottone che somiglia al vostro" e "Claude usa il vostro `<Button variant="primary">`".

**Passi.**
1. Lo sviluppo collega i componenti principali (bottone, input, card) con Code Connect.
2. Il design usa solo componenti della libreria collegata.
3. Claude Code legge il frame tramite MCP e produce codice con i componenti reali.

**Note.** Le variabili di Figma diventano token solo se il design le usa davvero: colori incollati a mano non vengono letti come token.

---

## 7 · Adobe: il connettore Adobe for creativity

Dal **28 aprile 2026** Claude ha un connettore ufficiale Adobe: **oltre 50 strumenti** di Photoshop, Illustrator, Express, Firefly, Lightroom, InDesign, Premiere e Stock.

**Come funziona.** Descrivi il risultato, Claude orchestra gli strumenti in più passaggi. Il lavoro può poi tornare nelle app Adobe (Photoshop, Premiere) o in Firefly Boards ed Express per la rifinitura.

**Accesso.** Disponibile per chi usa Claude con un account Adobe. Con l'account Adobe si hanno limiti più alti, più strumenti e il salvataggio tra sessioni. *(⚠ verifica i dettagli del vostro abbonamento)*

**Il limite da conoscere.** Una fonte indica che il connettore lavora a livello **Express e Firefly**, non con tutte le funzioni professionali di Photoshop o Premiere desktop. *(⚠ verifica)* Usalo per produzione e varianti, non per il ritocco di precisione.

### Dove rende
| Compito | Esempio di richiesta |
|---|---|
| **Adattamenti per canale** | "Da questa key visual, crea le versioni 1:1, 4:5 e 9:16 per Instagram e LinkedIn, mantenendo il logo nell'area sicura." |
| **Varianti di campagna** | "Genera quattro sfondi con Firefly in stile [riferimento], palette del brand, senza testo." |
| **Pulizia in serie** | "Rimuovi lo sfondo da queste 20 foto prodotto ed esportale su bianco." |
| **Impaginati veloci** | "Crea un volantino A5 in Express con questo testo e la nostra palette." |

**Diritti.** Per uso commerciale verificate le condizioni di licenza delle immagini generate e degli asset Stock.

---

## 8 · Loghi e identità: fin dove arriva Claude

### Cosa sa fare davvero
Claude **scrive SVG**: codice vettoriale vero, apribile e modificabile in Illustrator o Figma. Funziona bene per:
- marchi geometrici, monogrammi, pittogrammi;
- esplorazione rapida di molte direzioni;
- sistemi di icone coerenti;
- varianti di un marchio esistente (monocromo, versione ridotta, favicon).

Non sostituisce il designer su:
- marchi con forme organiche complesse e curve di precisione;
- lettering su misura e correzioni ottiche fini;
- la scelta finale: originalità, pertinenza, memorabilità.

### Il flusso consigliato
1. **Brief di marca** con il BRIEF: valori, pubblico, concorrenti, cosa evitare.
2. **Concept verbali:** "Proponi 20 direzioni di marchio in una riga ciascuna, raggruppate per metafora."
3. **Schizzi SVG:** sulle 5 direzioni scelte, "Disegna ogni marchio in SVG su griglia 64×64, solo forme geometriche, un colore, nessun testo."
4. **Selezione e costruzione:** "Ridisegna il marchio 3 con una griglia di costruzione visibile e proporzioni basate su un modulo."
5. **Rifinitura in Illustrator:** curve, pesi ottici, kerning del logotipo.
6. **Test:** a 16 px, in monocromo, in negativo, come favicon e accanto ai concorrenti.

### Prompt per lo schizzo SVG
```
Disegna 4 varianti del marchio "nodo" per UX Boutique in SVG.
Vincoli: viewBox 0 0 64 64, solo path e cerchi, tratto pieno,
un solo colore (currentColor), nessun testo, leggibile a 16 px.
Per ogni variante: il codice SVG e una riga sull'idea.
```

### Attenzione
- **Originalità:** verificate che il marchio non somigli a marchi registrati. È una vostra responsabilità.
- **Raster ≠ vettoriale:** le immagini di Firefly sono raster. Per un logo serve sempre il vettoriale.
- Esistono **Skill dedicate al design di loghi in SVG**: leggetele prima di installarle.

---

## 9 · Cosa sì, cosa no: la mappa dei limiti

| Compito | Claude da solo | Claude + strumenti | Resta al designer |
|---|---|---|---|
| Esplorare 20 direzioni di marchio | ✅ | | La scelta |
| Marchio geometrico in SVG | ✅ bozza | Illustrator per rifinire | Pesi ottici, finale |
| Logotipo e lettering | ⚠ solo idee | Illustrator | Disegno delle lettere |
| Schermate dal design system | | ✅ Figma MCP | Revisione e coerenza |
| Varianti e adattamenti di campagna | | ✅ Adobe, Claude Design | Direzione artistica |
| Foto e illustrazioni originali | ❌ | ✅ Firefly via Adobe | Selezione, ritocco |
| Ritocco fotografico di precisione | ❌ | ⚠ limitato | ✅ Photoshop |
| Prototipi interattivi on-brand | | ✅ Claude Design | Test con utenti |
| Analisi euristica e accessibilità | ✅ | | Test reali |

---

# C · Sviluppo

## 10 · Claude Code avanzato: CLAUDE.md, comandi, subagent

### CLAUDE.md su più livelli
- `~/.claude/CLAUDE.md`: le tue preferenze personali, per tutti i progetti.
- `CLAUDE.md` nella radice: le regole del repository, condivise con il team.
- `CLAUDE.md` nelle sottocartelle: regole specifiche, per esempio solo per `apps/web/`.

Tenetelo corto e operativo: comandi esatti, convenzioni, cosa non toccare, come verificare.

```markdown
## Verifica (obbligatoria prima di dire "fatto")
- npm run lint && npm run typecheck && npm test
- Per modifiche UI: avvia il server e controlla la pagina a 390 e 1280 px.
## Non toccare
- packages/legacy/, file .env, migrazioni già applicate.
```

### Skill e comandi del team
Le procedure ripetute diventano Skill in `.claude/skills/` (versionate con il repo): checklist di rilascio, review con le regole del team, creazione di un componente con test e storia.

### Subagent personalizzati
Un subagent è un file Markdown con istruzioni proprie, per esempio un revisore di accessibilità o di sicurezza. *(⚠ verifica la cartella, di solito `.claude/agents/`)*
```markdown
---
name: revisore-accessibilita
description: Controlla accessibilità di componenti e pagine modificati.
  Usalo dopo ogni modifica alla UI.
---
Controlla contrasto (WCAG AA), etichette dei campi, ordine del focus,
navigazione da tastiera, target touch di almeno 44 px.
Rispondi con una tabella File | Problema | Criterio WCAG | Correzione.
Non modificare i file: solo segnalare.
```

---

## 11 · Hook: le regole che scattano sempre

Le istruzioni in `CLAUDE.md` vengono seguite **quasi sempre**. Gli **hook** sono comandi che scattano **sempre**, in momenti precisi del ciclo di Claude Code: prima o dopo l'uso di uno strumento, alla fine di un compito.

| Esempio | Momento | Effetto |
|---|---|---|
| Formattazione automatica | Dopo ogni modifica a un file | Il codice è sempre formattato |
| Blocco dei segreti | Prima di scrivere un file | Impedisce di salvare chiavi o password |
| Test rapidi | Alla fine del compito | Segnala subito ciò che si è rotto |

Si configurano nelle impostazioni del progetto (`.claude/settings.json`). Gli hook possono riconoscere anche gli strumenti MCP, per esempio quelli di Figma. *(⚠ verifica lo schema esatto nella documentazione degli hook prima di usarli)*

**Attenzione.** Un hook esegue comandi sulla macchina: trattalo come codice, con revisione.

---

## 12 · Lavori paralleli con i worktree

Un **worktree** è una copia di lavoro separata dello stesso repository. Con più worktree potete far lavorare più sessioni di Claude Code in parallelo, senza che le modifiche si scontrino.

**Quando:** compiti lunghi e indipendenti (una nuova pagina, una migrazione, i test di un modulo).
**Quando no:** ricerche e letture, che non modificano file. Per quelle basta un subagent.

```bash
git worktree add ../sito-pagina-audit -b feature/pagina-audit
cd ../sito-pagina-audit && claude
```

Anche i subagent possono lavorare ciascuno nel proprio worktree, isolati dagli altri.

---

## 13 · Automazione: headless e GitHub Action

**Headless.** `claude -p "…"` esegue Claude Code senza interfaccia: utile negli script.
```bash
claude -p "Leggi CHANGELOG.md e scrivi le note di rilascio in italiano per i clienti, max 150 parole" > release-notes.md
```

**GitHub Action ufficiale** (`anthropics/claude-code-action@v1`): Claude lavora nei vostri repository GitHub.
- **Review automatica** delle pull request con le regole del team.
- **Da issue a pull request:** citando Claude in una issue, prepara una proposta di modifica.
- **Manutenzione:** aggiornamenti delle dipendenze con test.

Regola: le modifiche automatiche arrivano **sempre come pull request** con test, mai direttamente sul branch principale. *(⚠ verifica configurazione e permessi nella documentazione dell'Action)*

---

## 14 · Dal design al codice, senza perdite

Il flusso che usa tutto quello che avete:
1. **Figma:** il design usa componenti della libreria e variabili.
2. **Code Connect:** i componenti Figma sono collegati a quelli del codice.
3. **Claude Code + Figma MCP:** legge il frame e genera la pagina con i componenti reali e i token.
4. **Verifica visiva:** Claude avvia il sito, fa screenshot a più larghezze e li confronta con il frame.
5. **Pull request** con screenshot, review umana, merge.

```
Implementa il frame [link Figma] come pagina /servizi/audit.
Usa i componenti collegati con Code Connect e i token di design/tokens.json.
Nessun valore di colore o spaziatura scritto a mano.
Poi avvia il server, fai uno screenshot a 390 e 1280 px e confrontalo
con il frame: elenca le differenze prima di aprire la pull request.
```

---

# D · Marketing

## 15 · Un sistema di contenuti, non singoli testi

A livello avanzato il marketing con Claude è un **sistema**:
- **Project di brand** con posizionamento, personas, tono, claim approvati, divieti.
- **Skill di formato:** post per canale, newsletter, landing, annunci. Nel repository ci sono già 53 Skill di marketing (copywriting, content-strategy, ad-creative, emails, seo-audit…) da adattare al vostro tono.
- **Casi di test** per ogni Skill (cap. 2): il tono resta coerente anche quando cambiano le persone.
- **Libreria di prompt approvati** versionata nel repository.

**Prompt per costruire la Skill di tono:**
```
<testi_approvati>[10 testi che rappresentano il nostro tono]</testi_approvati>
<testi_da_evitare>[5 testi che non ci rappresentano]</testi_da_evitare>
Ricava le regole del nostro tono: lessico, lunghezza delle frasi,
struttura, cosa evitare. Scrivi una Skill con regole verificabili ed esempi.
```

---

## 16 · Campagne multicanale con Adobe e Claude Design

**La catena di una campagna:**
1. **Ricerca approfondita:** mercato, competitor, linguaggio dei clienti, con fonti.
2. **Strategia:** posizionamento della campagna e tre messaggi chiave.
3. **Concept:** tre direzioni creative, una scelta.
4. **Testi per canale** con le Skill di formato.
5. **Visual:** key visual e adattamenti con il connettore Adobe; landing e one-pager in Claude Design.
6. **Revisione:** gioco di ruolo con il cliente scettico, verifica dei claim.
7. **Misura:** report dai dati della campagna.

---

## 17 · Ricerca, dati e contenuti in scala

- **Analisi dei dati:** carica gli export di campagne e chiedi analisi con calcoli verificabili ("mostra i calcoli di un canale").
- **SEO e AI search:** struttura dei contenuti per essere citati anche dagli assistenti AI. Ci sono Skill dedicate (`ai-seo`, `seo-audit`).
- **Contenuti in scala con Claude Code:** da un foglio di dati (prodotti, città, servizi), generare decine di pagine o schede con lo stesso modello. Regola: campione rivisto a mano prima di pubblicare tutto, e nessun contenuto duplicato o di scarso valore.

---

# E · Project management

## 18 · Il PM con i connettori

Il PM avanzato usa Claude come **assistente che legge tutti gli strumenti**:
- **Drive:** brief, contratti, verbali.
- **Miro:** board dei workshop.
- **Figma:** stato dei design.
- **GitHub:** issue, pull request, avanzamento dello sviluppo.
- Altri strumenti del team, se il connettore è disponibile (calendario, email, gestori di progetto). *(⚠ verifica i connettori abilitati)*

**Prompt: stato reale di un progetto**
```
Per il progetto [nome]: leggi l'ultimo verbale su Drive, la board Miro
del workshop e le issue aperte su GitHub con etichetta [cliente].
Dimmi: cosa è stato deciso, cosa è in ritardo rispetto al piano,
quali rischi vedi. Cita la fonte di ogni affermazione.
```

---

## 19 · Report, rischi e stime automatici

| Attività | Come |
|---|---|
| **Status report settimanale** | Skill "status report" + attività programmata ogni lunedì, revisione del PM prima dell'invio |
| **Registro dei rischi** | Dopo ogni verbale: "aggiorna il registro: nuovi rischi, probabilità, impatto, mitigazione, responsabile" |
| **Stime** | Ragionamento esteso + storico dei progetti simili: "stima per fasi con ipotesi esplicite e intervallo minimo–massimo" |
| **Dai verbali alle issue** | Claude Code o connettore GitHub: "crea le issue dalle azioni del verbale, con responsabile e scadenza" |
| **Dashboard** | Un Artifact con i dati del progetto, aggiornato a ogni report |

Per i compiti sui file del computer (cartelle di progetto, documenti da tanti file) c'è **Cowork**, con il plugin ufficiale di project management. *(⚠ verifica la disponibilità)*

---

# F · Il flusso integrato e la governance

## 20 · Dal brief al lancio: tutti i ruoli insieme

| Fase | Chi | Strumento | Output |
|---|---|---|---|
| Brief e piano | PM | Drive, Miro, ragionamento esteso | Brief, piano, rischi |
| Ricerca | Marketing | Ricerca approfondita | Mercato e messaggi |
| Design | Design | Figma MCP, librerie | Schermate dal design system |
| Visual di campagna | Design + Marketing | Adobe, Claude Design | Key visual e adattamenti |
| Sviluppo | Dev | Claude Code, Code Connect, worktree | Pull request con screenshot |
| Qualità | Dev | GitHub Action, hook, subagent | Review e test automatici |
| Lancio | Marketing | Skill di formato | Contenuti per canale |
| Controllo | PM | Attività programmate | Report e rischi aggiornati |

---

## 21 · Governance: Skill, plugin e costi del team

- **Un repository per le Skill del team**, con responsabile, versioni e casi di test.
- **Un marketplace interno di plugin** per installare lo stesso kit a tutti: `/plugin marketplace add` sul vostro repository.
- **Revisione obbligatoria** per Skill, hook e plugin: possono eseguire comandi.
- **Costi:** scegliete il modello per compito (Haiku per i lavori in volume, Sonnet di base, Opus per i compiti difficili). La scrittura sul canvas di Figma diventerà a consumo dopo la beta.
- **Regole sui dati:** cosa si può caricare, quali connettori sono attivi, chi li abilita.

---

## 22 · Esercizi avanzati per ruolo

**Design**
1. Con Figma MCP, crea tre varianti di una schermata usando solo la libreria del team. Misura quanti valori sono rimasti fuori dalle variabili.
2. Esplora un marchio: 20 concept, 5 SVG, 1 rifinito in Illustrator, test a 16 px.

**Sviluppo**
1. Configura un hook che formatta i file dopo ogni modifica e un subagent revisore di accessibilità.
2. Implementa un frame Figma con Code Connect e verifica visiva a due larghezze.

**Marketing**
1. Ricava la Skill di tono da 10 testi approvati e scrivi 5 casi di test.
2. Una campagna completa: ricerca, concept, testi per canale, adattamenti con Adobe.

**Project management**
1. Prompt di stato reale su un progetto vero, con fonti da Drive, Miro e GitHub.
2. Status report automatico con Skill e attività programmata.

---

## 23 · Fonti
- Figma, *Write to canvas*: https://developers.figma.com/docs/figma-mcp-server/write-to-canvas
- Figma, *MCP server FAQs*: https://help.figma.com/hc/en-us/articles/39252411778583-Figma-MCP-server-FAQs
- Adobe, *Adobe for creativity connector*: https://blog.adobe.com/en/publish/2026/04/28/adobe-for-creativity-connector
- PetaPixel, *Claude AI can orchestrate creative workflows across Adobe apps*: https://petapixel.com/2026/04/28/claude-ai-can-orchestrate-creative-workflows-across-adobe-apps/
- Claude Code, *Best practices*: https://code.claude.com/docs/en/best-practices
- Claude Code, *Worktrees*: https://code.claude.com/docs/en/worktrees.md
- Claude Code, *Subagents*: https://code.claude.com/docs/en/sub-agents
- Claude Code, plugin: https://code.claude.com/docs/en/discover-plugins
- Anthropic, *Prompt Engineering Interactive Tutorial* (valutazioni empiriche, catene): https://github.com/anthropics/prompt-eng-interactive-tutorial
- Recraft, *How to generate images in Claude* (SVG e vettoriale): https://www.recraft.ai/blog/how-to-generate-images-in-claude
- Logo designer skill (esempio di Skill per loghi SVG): https://github.com/neonwatty/logo-designer-skill

**Da verificare prima del corso:** seat e costi di Figma MCP in scrittura; limiti e abbonamento del connettore Adobe; schema degli hook; configurazione della GitHub Action; cartella dei subagent; connettori disponibili per il PM.
