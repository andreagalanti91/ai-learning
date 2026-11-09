# Claude AI — Dal prompting al building
### Corso approfondito · Bozza v0.3 · UX Boutique

> Versione estesa dell'indice (`indice.md`). Per ogni capitolo: **concetto** (cosa è e perché conta), **spiegazione** (come funziona davvero), **demo** (passi da fare in aula), **esercizio** (da fare a casa o in coppia).
>
> **Nota di verifica.** Le descrizioni generali sono stabili. I nomi dei menu e i passaggi dell'interfaccia cambiano spesso: prima di ogni sessione, rifate le demo nel vostro account Team e aggiornate i passi.

---

## 00 — Apertura

### Concetto
Il corso porta l'AI da uno strumento usato "ogni tanto" a una parte del vostro metodo di lavoro. Il percorso ha cinque livelli: **Prompt → Contesto → Metodo → Connessioni → Agente**. Ogni livello rende il lavoro più ripetibile e più condiviso.

### Spiegazione
- **Prompt**: la richiesta singola, scritta bene.
- **Contesto**: le informazioni che Claude deve avere sempre (brand, clienti, documenti).
- **Metodo**: un processo ripetuto, trasformato in istruzioni riutilizzabili (Skill).
- **Connessioni**: Claude che legge e scrive nei vostri strumenti (Drive, Notion, Figma, GitHub).
- **Agente**: Claude che lavora in più passaggi su file e repository (Claude Code).

### Demo
1. Ogni partecipante descrive in due frasi come usa l'AI oggi (giro di tavolo, 0.3).
2. Il docente mostra una stessa richiesta fatta in due modi: prima "scrivimi un post" e poi con contesto e obiettivo. Si confrontano i risultati.

### Esercizio
Scrivete su un foglio: quale dei cinque livelli usate oggi? Quale vorreste padroneggiare entro il corso?

---

## 01 — Fondamenti: come funziona Claude

### 1.1 Cos'è un modello linguistico
**Concetto.** Claude è un modello linguistico: produce testo rispondendo a un input. Non "cerca" in un database e non "sa" le cose come una persona: genera la risposta più plausibile dato ciò che vede.

**Spiegazione.** Da questo deriva tutto il resto: Claude è molto bravo con testo, struttura, ragionamento e codice, ma può sbagliare fatti, e le sue risposte dipendono da quanto contesto gli date.

### 1.2 I modelli: Opus, Sonnet, Haiku
**Concetto.** Sono tre modelli della stessa famiglia, con compromessi diversi tra profondità e velocità.
- **Opus**: il più capace, per ragionamenti complessi, analisi lunghe, lavori delicati.
- **Sonnet**: il bilanciato, per la maggior parte del lavoro quotidiano.
- **Haiku**: il più veloce e leggero, per compiti semplici e ripetitivi in grande volume.

**Regola pratica.** Partite con il modello bilanciato. Passate a Opus quando la qualità della risposta è il problema; passate a Haiku quando la velocità conta più della profondità.

### 1.3 Effort e ragionamento
**Concetto.** Alcune impostazioni fanno sì che Claude "pensi" più a lungo prima di rispondere.
**Spiegazione.** Più effort significa risposte più accurate su problemi complessi, ma più lente e più costose in termini di utilizzo. Per una riscrittura di un paragrafo non serve; per una strategia o un bug difficile sì.

### 1.4 La finestra di contesto
**Concetto.** Claude lavora su una quantità limitata di testo alla volta: la finestra di contesto. Tutto ciò che è dentro la finestra è "visto"; tutto il resto no.
**Spiegazione.** In una chat molto lunga, le informazioni all'inizio possono perdere peso o essere riassunte. Per questo esistono i Project (cap. 03) e il riassunto di chat (cap. 03.6).

### 1.5 Limiti, allucinazioni e verifica
**Concetto.** Un'allucinazione è una risposta sicura di sé ma sbagliata: un numero, una citazione, un nome inventato.
**Spiegazione.** Le allucinazioni non si eliminano del tutto, ma si riducono e si individuano. Regole: chiedete le fonti, verificate i numeri, date a Claude i documenti veri invece di chiedergli di ricordarli.

### 1.6 Dove si usa Claude
Web, app desktop, app mobile, estensioni per browser e IDE, e Claude Code da terminale. Stesso account, esperienze diverse: il web per la chat e i file, Claude Code per il lavoro su cartelle e repository.

### Demo
1. Stessa domanda con Haiku, Sonnet e Opus: confrontate tempi e profondità.
2. Chiedete a Claude una citazione precisa e poi verificatela: mostrate il caso in cui sbaglia.

### Esercizio
Prendete un testo che avete scritto voi, chiedete a Claude di verificarne i fatti e segnate quali affermazioni controllare a mano.

---

## 02 — Livello 1 · Prompt: il framework BRIEF

### 2.1 Dal prompt al brief
**Concetto.** Un prompt semplice ("scrivi un post") lascia a Claude tutte le decisioni. Un brief le rende esplicite. Il framework BRIEF ha cinque parti più una verifica:

| Lettera | Parte | Domanda guida | Esempio |
|---|---|---|---|
| **B** | Background | Qual è il contesto? | "Siamo un'agenzia UX; il cliente è una cantina." |
| **R** | Ruolo | Chi deve rispondere? | "Sei un copywriter senior con tono sobrio." |
| **I** | Intento | Cosa deve ottenere il lettore? | "Convincere a prenotare una visita." |
| **E** | Esempi | Come deve essere? | "Tono come nell'esempio allegato." |
| **F** | Formato | In che forma? | "3 varianti, max 280 caratteri, senza emoji." |
| + | Verifica | Come controlliamo? | "Elenca i punti che non sei sicuro di aver rispettato." |

**Spiegazione.** Non serve sempre compilare tutte le lettere. Un compito semplice ne richiede due o tre. Il valore è nel rendere esplicite le scelte che altrimenti Claude farebbe da solo.

### 2.2 Prima e dopo
**Demo.** Lo stesso compito in due versioni:
- *Prima*: "Scrivi un post per Instagram sul nostro nuovo servizio."
- *Dopo*: BRIEF completo, con cliente, tono, lunghezza, call to action.
Si confrontano le due risposte e si discute quale parte del brief ha cambiato di più il risultato.

### 2.3 Tecniche avanzate
- **Tag XML per separare istruzioni e materiali.** Mettete istruzioni e documenti in blocchi distinti, ad esempio `<istruzioni>…</istruzioni>` e `<testo>…</testo>`. Claude distingue meglio cosa fare da cosa analizzare.
- **Few-shot: insegnare con gli esempi.** Due o tre esempi di output desiderato valgono più di una lunga descrizione. Usatele quando il formato è difficile da spiegare a parole.
- **Prompt a catena.** Dividete un compito grande in passaggi: prima estrarre i fatti, poi scrivere la bozza, poi revisionarla. Ogni passaggio ha un output che il successivo usa.
- **Autocritica e criteri di qualità.** Dategli criteri espliciti ("ogni frase deve avere un numero o un esempio") e chiedete di rivedere la propria bozza rispetto a quei criteri.
- **Motivazioni e fonti verificabili.** Chiedete perché ha scelto una cosa e da quale documento viene un'affermazione. Le risposte con fonti sono più facili da controllare.

### 2.4 Iterare: come dare feedback
**Concetto.** Il primo output è una bozza. Il feedback efficace indica cosa cambiare, perché e come.
**Spiegazione.** "Non mi piace" non serve. "Il tono è troppo tecnico per un pubblico non esperto: riscrivi il secondo paragrafo con esempi concreti" sì.

### 2.5 Debug del prompt
**Concetto.** Se un prompt non funziona, quasi sempre manca una delle cinque parti del brief o il formato non è chiaro.
**Procedura.**
1. Leggete l'output e chiedete: cosa mi aspettavo che non c'è?
2. Trovate la lettera del BRIEF che manca (o che è ambigua).
3. Aggiungetela e rilanciate. Se non cambia nulla, cambiate gli esempi.

### Esercizio
Prendete un compito reale della vostra settimana. Scrivete il prompt semplice, poi il BRIEF. Confrontate i due output e annotate la differenza.

---

## 03 — Livello 2 · Contesto: Projects e memoria

### 3.1 Perché il contesto conta più del prompt
**Concetto.** Un buon prompt in un contesto vuoto dà risultati generici. Un prompt medio in un contesto ricco (brand, clienti, documenti) dà risultati specifici.
**Spiegazione.** Il contesto è ciò che Claude sa già prima che voi scriviate. Va costruito una volta sola e riutilizzato.

### 3.2 Creare un Project
**Concetto.** Un Project è uno spazio con **istruzioni** permanenti e una **knowledge base** di documenti. Ogni chat aperta dentro il Project usa entrambi.
**Demo.**
1. Create un Project con nome chiaro (es. "UX Boutique — Brand & Tone").
2. Scrivete le istruzioni: chi siete, a chi parlate, cosa non fate mai.
3. Caricate i documenti di riferimento.
4. Aprite una chat nel Project e chiedete una bozza. Confrontatela con una chat fuori dal Project.

### 3.3 Quali documenti caricare
- Documenti **aggiornati e approvati**, non bozze.
- Documenti **brevi e focalizzati**: una guida di tono di 3 pagine è più utile di 40 pagine di presentazioni.
- Preparate i file: testo selezionabile (non scansioni), titoli chiari, niente dati sensibili non necessari.

### 3.4 Projects condivisi nel piano Team
**Concetto.** Nel piano Team un Project può essere condiviso: tutto il team usa le stesse istruzioni e gli stessi documenti.
**Spiegazione.** È il modo per evitare che ognuno reinventi il tono di voce. Chi modifica le istruzioni deve saperlo dire agli altri.

### 3.5 Memoria e ricerca nelle chat passate
**Concetto.** Claude può ritrovare conversazioni precedenti e riusarne il contenuto.
**Attenzione.** Non tutto ciò che è stato detto in passato è aggiornato. Verificate sempre le informazioni riprese da una vecchia chat.

### 3.6 Chat lunghe
**Concetto.** Una chat molto lunga diventa lenta e perde precisione all'inizio.
**Procedura.**
- Quando il lavoro cambia obiettivo, aprite una nuova chat.
- Prima di ripartire, chiedete un **riassunto strutturato** (decisioni, documenti, prossimi passi) e incollatelo nella chat nuova.
- Dividete i grandi progetti in chat tematiche.

### 3.7 Esempio completo: Project "UX Boutique — Brand & Tone"
**Istruzioni (esempio).**
> Lavoriamo per UX Boutique. Scriviamo in italiano, tono diretto e concreto, niente superlativi vuoti. Ogni testo per clienti deve indicare il beneficio misurabile. Non citare mai clienti senza loro approvazione scritta. Quando non sei sicuro di un fatto, dichiaralo.

**Knowledge base (esempio).** Guida al tono di voce; tre testi approvati come esempio; glossario dei termini da usare e da evitare.

**Test.** Chiedete: "Scrivi un'intro di 60 parole per la pagina servizi." Il risultato deve rispettare tono, glossario e regole senza che voi le ripetiate.

### Esercizio
Create il Project del vostro ruolo. Scrivete le istruzioni in 5 righe e caricate 2 documenti. Testate con una richiesta reale.

---

## 04 — Output: dalla risposta al deliverable

### 4.1 Artifacts
**Concetto.** Un Artifact è un output autonomo: un documento, una presentazione, un foglio di calcolo, una pagina interattiva. Si modifica e si riscarica, invece di restare dentro la chat.
**Demo.** Chiedete un documento di sintesi di un'intervista e poi chiedete una modifica di sezione. Mostrate che l'artifact si aggiorna senza ricominciare.

### 4.2 Ricerca web e ricerca approfondita
**Concetto.** La ricerca web porta informazioni recenti. La ricerca approfondita fa più passaggi di ricerca e produce un rapporto con fonti.
**Regola.** Ogni dato da ricerca va verificato sulla fonte originale prima di essere pubblicato.

### 4.3 Analisi di file
Caricate PDF, Excel, immagini e screenshot e chiedete analisi mirate: "estrai le date dei contratti in scadenza", "trova le incongruenze tra questi due fogli", "descrivi i problemi di accessibilità in questo screenshot".

### 4.4 Grafici e analisi dei dati
**Concetto.** Claude può analizzare un CSV o un Excel e produrre grafici.
**Procedura.** Caricate il file, descrivete la domanda ("quali canali hanno il costo per lead più alto?"), chiedete il grafico, poi verificate i numeri su un campione a mano.

### 4.5 Lavori lunghi in autonomia
**Concetto.** Alcuni compiti hanno più passaggi e possono essere fatti in autonomia o programmati.
**Esempio.** Un report settimanale: ogni lunedì Claude legge i dati, produce il riassunto e lo salva. Prima di automatizzare, fate il compito a mano una volta.

### Esercizio
Caricate un file reale (report, intervista, foglio). Chiedete un output in forma di artifact con tre domande precise. Annotate cosa avete dovuto correggere.

---

## 05 — Livelli 3 e 4: Metodo e connessioni

### 5.1 La mappa
- **Skills**: il **metodo**. Istruzioni e procedure riutilizzabili per un compito ripetuto.
- **Connectors**: i **dati**. Collegamenti a Google Drive, Notion, Slack, Gmail, GitHub, Figma.
- **Plugins**: **pacchetti** che combinano skill e connettori per un ambito preciso.

### 5.2 Skills
**Concetto.** Una Skill è un metodo scritto una volta e usato da chiunque nel team. Non è un prompt lungo: ha una descrizione (quando usarla), passaggi, criteri di qualità ed eventuali esempi.
**Come si riconosce un buon candidato.** Un compito fatto più di tre volte al mese, con lo stesso schema, e con un output che si può giudicare.

### 5.3 Creare e condividere una Skill
**Procedura.**
1. Prendete un Project che funziona bene e scrivete il processo come passaggi numerati.
2. Definite l'input (cosa serve) e l'output atteso (come deve essere).
3. Aggiungete criteri di qualità e un esempio.
4. Testate su tre casi diversi. Correggete dove il risultato devia.
5. Condividete con il team e raccogliete feedback per una versione successiva.

### 5.4 Connectors
**Concetto.** Un connettore permette a Claude di leggere (e in alcuni casi scrivere) nei vostri strumenti. Esempio: "trova il brief nel Drive del cliente X e riassumilo".
**Attenzione.** Un connettore dà accesso ai dati reali. Usate il minimo permesso necessario e verificate cosa può leggere e scrivere.

### 5.5 MCP: la presa USB dell'AI
**Concetto.** MCP (Model Context Protocol) è uno standard con cui uno strumento espone le sue funzioni a Claude. Come una presa USB: lo strumento ha una presa standard, Claude ha una presa standard, e la connessione funziona senza adattatori su misura.
**Spiegazione.** Figma, GitHub o un database interno possono esporre un server MCP. Claude vede le operazioni disponibili e le usa su richiesta.

### 5.6 Piano Team
**Cosa abilita l'admin.** Quali connettori sono disponibili, quali Project sono condivisi, chi può creare Skill.
**Autenticazione e permessi.** Ogni persona accede con il proprio account; i permessi sui file restano quelli dello strumento di origine.

### 5.7 Workflow integrati
**Concetto.** Connettore + Skill + output: il flusso completo.
**Esempio.** Un PM chiede a Claude di leggere le note di una riunione (Notion), applicare la Skill "status report", e produrre un documento da condividere (artifact).

### Demo
1. Collegate un connettore (es. Drive) e fate una ricerca reale.
2. Create una Skill semplice ("riassumi un verbale in 5 punti: decisioni, responsabili, scadenze, rischi, prossimi passi") e usatela su un verbale.

### Esercizio
Scegliete un compito ripetuto del vostro ruolo. Trasformatelo in una Skill di non più di una pagina. Testatela su due casi reali.

---

## 06 — Claude Design e Figma

Questo è il capitolo più pratico per art direction, grafica, design e marketing. Lo sviluppiamo in dettaglio.

### 6.1 Claude Design: cos'è e cosa produce

**Concetto.** Claude Design è lo strumento per creare **visual e prototipi** a partire da un brief. Non è un generatore di immagini: produce strutture di pagina, layout, testi e stili che si possono rivedere, modificare ed esportare.

**Cosa produce (tipico):**
- **Prototipi** di interfacce e flussi, navigabili.
- **Slide** per presentazioni.
- **One-pager**: una pagina di sintesi o di proposta.
- **Landing page**: una pagina di campagna o di prodotto.

**Cosa non produce.** Foto, illustrazioni originali e video. Per quelli servono altri strumenti (vedi cap. 09).

> Nota: le voci del menu cambiano. Verificate nel vostro account quali tipi di output sono attivi nel piano Team.

### 6.2 Da un brief a un prototipo

Questo è il flusso base. Lo facciamo con un esempio reale: una landing per un servizio.

**Passo 1 — Scrivere il brief.** Usate il BRIEF del cap. 02, con questi dettagli:
- **B (Background)**: "UX Boutique offre audit di usabilità per e-commerce di medie dimensioni."
- **R (Ruolo)**: "Sei un designer UX senior, sobrio e concreto."
- **I (Intento)**: "Convertire un responsabile marketing a richiedere un audit gratuito."
- **E (Esempi)**: allegate una landing che vi piace (screenshot) e spiegate cosa vi piace.
- **F (Formato)**: "Landing con: hero, tre benefici misurabili, un caso studio, una call to action, footer. Mobile first."

**Passo 2 — Chiedere la prima versione.** Chiedete la struttura prima dello stile: "Proponi tre strutture diverse di landing con le sezioni e il contenuto di ciascuna. Non applicare ancora colori e font."
Perché: se chiedete subito stile e struttura insieme, è difficile capire quale parte non funziona.

**Passo 3 — Scegliere e raffinare.** Scegliete una struttura e chiedete il prototipo. Poi fate revisioni mirate: "Il titolo dell'hero è troppo generico: proponi tre alternative con un numero nel testo." Una revisione per volta.

**Passo 4 — Verificare.** Controllate: il contenuto è vero? I numeri sono approvati? Il tono rispetta il Project? Il layout funziona su mobile?

**Passo 5 — Esportare.** Vedi 6.4.

**Errori frequenti.**
- Brief troppo vago ("fammi una bella landing"): il risultato è generico.
- Chiedere troppo in una volta: il risultato è mediocre su tutto.
- Non fornire un esempio visivo: il design dipende dai gusti, e Claude non conosce i vostri.
- Accettare numeri o claim non verificati.

### 6.3 Brand e design system come contesto

**Concetto.** Se il brand è già definito, Claude deve conoscerlo. Il modo giusto è metterlo nel Project come contesto, non ripeterlo in ogni richiesta.

**Cosa caricare.**
- **Brand kit**: colori (con valori HEX), font, logo in uso, spaziature.
- **Tono di voce**: il documento del cap. 03.
- **Design system**: componenti base (bottoni, card, form), con le regole d'uso.

**Verifica.** Chiedete "descrivi il brand che stai usando" prima di generare. Se la descrizione non corrisponde al brand reale, correggete il contesto prima di procedere.

### 6.4 Export: HTML, PDF, PPTX, Canva

Scegliete il formato in base all'uso:

| Formato | Quando usarlo | Attenzione |
|---|---|---|
| **HTML** | Prototipo navigabile, da condividere o da passare allo sviluppo | Richiede un browser; controllate il mobile |
| **PDF** | Documento da inviare o stampare, one-pager | Il testo non è modificabile facilmente |
| **PPTX** | Presentazione da modificare in PowerPoint o Keynote | Verificate i font: possono non corrispondere |
| **Canva** | Lavoro da completare o adattare in Canva | Dipende dai connettori attivi |

**Regola pratica.** Esportate la versione definitiva solo dopo la verifica del passo 4 del cap. 6.2. Gli export sono più difficili da correggere che la bozza.

### 6.5 Figma MCP: leggere e scrivere

**Concetto.** Il server MCP di Figma permette a Claude di interagire con i file Figma del team. Ha due direzioni.

**Leggere da Figma.**
- Estrarre **token** (colori, spaziature, font) da un file.
- Leggere **componenti** e la loro struttura.
- Ottenere uno screenshot di un frame.

**Scrivere su Figma.**
- Creare o modificare elementi sul canvas.
- Applicare token e componenti esistenti.

**Attenzione.** Scrivere sul canvas modifica il file del team. Fate le scritture su una copia o su una pagina di prova, e verificate prima di confermare.

### 6.6 Il flusso Design ↔ Figma ↔ Code

Il flusso completo:
1. **Design**: il brief diventa un prototipo in Claude Design.
2. **Figma**: il prototipo viene portato o rifinito in Figma; i token vengono estratti dal design system.
3. **Code**: Claude Code usa i token e i componenti per generare il codice dell'interfaccia.

**Vantaggio.** I token sono la fonte unica: se cambia un colore nel design system, cambia nel codice. Senza token, ogni passaggio ricrea le decisioni da capo.

### 6.7 Cosa è nativo e cosa richiede MCP o strumenti esterni

| Funzione | Nativa in Claude | Richiede MCP / strumenti esterni |
|---|---|---|
| Brief → prototipo | Sì | No |
| Export HTML e PDF | Sì | No |
| Export PPTX | Sì | No |
| Lettura token da Figma | No | Sì (Figma MCP) |
| Scrittura su canvas Figma | No | Sì (Figma MCP) |
| Immagini generative | No | Sì (altri strumenti, cap. 09) |

*Verificate la colonna "nativa" nel vostro account: le funzioni cambiano più in fretta del corso.*

### Demo completa (60 minuti)
1. (10 min) Il docente presenta il brief di un progetto reale del team.
2. (15 min) Si chiedono tre strutture di landing, senza stile.
3. (15 min) Si sceglie una struttura e si chiede il prototipo con le revisioni.
4. (10 min) Verifica: contenuto, numeri, tono, mobile.
5. (10 min) Export in HTML e PDF e discussione.

### Esercizio
Ogni coppia prende un progetto reale (una pagina, una slide o un one-pager). Scrive il BRIEF, produce tre strutture, sceglie la migliore, fa tre revisioni mirate e lo esporta. Consegna: il file esportato e il brief usato.

---

## 07 — Livello 5 · Agente: Claude Code

### 7.1 Cos'è Claude Code
**Concetto.** Claude Code è un agente che lavora dentro una cartella o un repository: legge file, modifica file, esegue comandi, con la vostra supervisione.
**Non è solo per sviluppatori.** Chi lavora su documenti in cartelle (brief, testi, asset, report) ne trae vantaggio quanto chi scrive codice.

### 7.2 Installazione
Installazione tramite app desktop o terminale. Verificate nella documentazione aggiornata i requisiti e il login con il piano Team.

### 7.3 Cartelle, file e repository
- **Cartella**: un insieme di file. Claude Code lavora nella cartella in cui è stato avviato.
- **Repository**: una cartella con storia delle modifiche (Git). Ogni modifica è tracciata.
**Regola.** Lavorate su un repository, non su cartelle senza versioni, così potete sempre tornare indietro.

### 7.4 CLAUDE.md
**Concetto.** Un file `CLAUDE.md` nella radice del progetto contiene le istruzioni permanenti: come è organizzato il progetto, le regole di stile, i comandi da usare, cosa non toccare. Claude Code lo legge all'inizio di ogni sessione.
**Esempio.**
```markdown
# Progetto: sito UX Boutique
- Stack: HTML + CSS, nessun framework.
- Tono dei testi: vedi docs/tono-di-voce.md.
- Non modificare mai la cartella /legacy.
- Prima di ogni modifica, mostra il piano.
```

### 7.5 Plan mode
**Concetto.** In plan mode Claude propone un piano e aspetta la vostra approvazione prima di modificare i file.
**Quando usarlo.** Sempre per modifiche che toccano più file o che non si annullano facilmente.

### 7.6 Permessi e sicurezza
- Claude Code chiede il permesso per le azioni sensibili (modificare file, eseguire comandi).
- Non concedete permessi generici ("approva tutto") senza sapere cosa fanno.
- Non mettete segreti (password, chiavi API) nei file del repository.

### 7.7 Skills, subagent e MCP in Claude Code
- **Skills**: stesso concetto del cap. 05, ma usabili direttamente nel repository.
- **Subagent**: agenti secondari che lavorano su un sotto-compito e riportano il risultato.
- **MCP**: collegamenti agli strumenti esterni, come nel cap. 05.

### 7.8 Git e GitHub in breve
- **Commit**: una versione salvata con una descrizione.
- **Branch**: una linea di lavoro separata, per non toccare la versione principale.
- **Push**: invio delle modifiche al repository remoto (GitHub).
- **Pull request**: richiesta di unire un branch nel principale, con revisione.

### 7.9 Demo: da `.md` a presentazione HTML
**Passi.**
1. Partite da un file `.md` con i contenuti (es. questo corso).
2. Scrivete nel `CLAUDE.md` il brand e lo stile da usare.
3. Chiedete un piano in plan mode: struttura delle slide, cosa va in ciascuna.
4. Approvate il piano e lasciate generare l'HTML.
5. Aprite il file nel browser, verificate testi, navigazione e mobile.
6. Fate commit e push.

### Esercizio
Create un repository di prova con un `CLAUDE.md` di 10 righe. Chiedete una piccola modifica in plan mode. Leggete il piano prima di approvarlo.

---

## 08 — Percorsi per ruolo

Per ogni ruolo: **Base** → **Intermedio** → **Avanzato**. Il livello si raggiunge quando il lavoro è ripetibile senza di voi.

### 8.1 Marketing
- **Base**: testi, post, varianti di copy. *Esercizio*: 5 varianti di un claim con tre tono diversi.
- **Intermedio**: Project con brand e tono; piano editoriale mensile; analisi competitor con ricerca web. *Esercizio*: un piano editoriale di un mese, con fonti.
- **Avanzato**: Skill del tono di voce; campagne complete con Claude Design; report da CSV. *Esercizio*: una Skill "revisione copy" applicata a 10 testi reali.

### 8.2 Project Management
- **Base**: verbali, email ai clienti, riassunti. *Esercizio*: verbale → 5 punti con responsabili e scadenze.
- **Intermedio**: Project per cliente; stime; rischi; timeline; status report. *Esercizio*: status report settimanale da note grezze.
- **Avanzato**: connettori Drive e Notion; Skill per gli status report; attività programmate; dashboard. *Esercizio*: un report automatizzato con verifica umana.

### 8.3 UX/UI e Product Design
- **Base**: sintesi di interviste, personas, microcopy. *Esercizio*: 3 interviste → 5 bisogni con citazioni.
- **Intermedio**: user journey; architettura dell'informazione; analisi euristica da screenshot. *Esercizio*: euristica su un flusso reale.
- **Avanzato**: design system e token via Figma MCP; prototipi con Claude Design; handoff a Claude Code; revisione di accessibilità. *Esercizio*: un componente dal design al codice con token condivisi.

### 8.4 Art Direction e Graphic Design
- **Base**: concept, moodboard testuali, naming, claim. *Esercizio*: tre concept per un evento con motivazione.
- **Intermedio**: brief creativi; analisi di riferimenti visivi; varianti di layout. *Esercizio*: un brief creativo completo.
- **Avanzato**: Claude Design per visual e one-pager; brand kit come contesto; export verso Canva; prompt per generatori di immagini. *Esercizio*: un one-pager con brand kit e export.

### 8.5 Sviluppo
- **Base**: spiegare codice, snippet, regex, query. *Esercizio*: spiegare una funzione esistente riga per riga.
- **Intermedio**: debug, test, documentazione, code review. *Esercizio*: scrivere i test per una funzione.
- **Avanzato**: Claude Code con CLAUDE.md; subagent; GitHub; Figma MCP da design a codice; automazioni. *Esercizio*: una feature completa con piano, PR e revisione.

---

## 09 — Claude o un'altra AI?

### 9.1 Punti di forza di Claude
Scrittura, ragionamento su documenti lunghi, lavoro su file e contesto lungo, codice e revisione.

### 9.2 Dove servono altri strumenti
- **Immagini generative** (es. Midjourney, Adobe Firefly): per illustrazioni e fotografia sintetica.
- **Video e voce**: strumenti dedicati.
- **AI integrate** nei tool che già usate (Figma AI, Canva): comode per piccole operazioni nello stesso ambiente.

### 9.3 Confronto con ChatGPT e Gemini
Le differenze pratiche contano più delle classifiche: cambiano l'interfaccia, i connettori disponibili, il modo di gestire i file e i piani. Valutate con un compito reale del vostro lavoro, non con un benchmark.

### 9.4 Combinare più strumenti
Esempio: Claude scrive il brief e la struttura; uno strumento d'immagine genera il visual; Claude Design compone il one-pager; Figma rifinisce; Claude Code porta l'interfaccia nel sito.

### 9.5 Albero decisionale
- Il compito è testo, analisi o codice? → Claude.
- Serve un'immagine originale? → strumento generativo, poi Claude per il brief.
- Serve un file da modificare nel tool di origine? → lo strumento integrato.
- Serve una decisione con dati sensibili? → verificate la policy dello strumento prima (cap. 10).

---

## 10 — Qualità, sicurezza e privacy

### 10.1 Verificare i risultati
Controllate in quest'ordine: **fatti** (chi, cosa, quando), **numeri** (ricalcolateli su un campione), **fonti** (aprite la fonte), **codice** (eseguitelo e leggetelo prima di usarlo).

### 10.2 Dati dei clienti, NDA e cosa non caricare mai
- Non caricate dati personali di clienti senza base legale e senza approvazione.
- Non caricate documenti coperti da NDA se l'NDA non lo consente.
- Non caricate password, chiavi API o credenziali.
**Regola.** Se non siete sicuri, anonimizzate o chiedete al referente privacy.

### 10.3 Impostazioni privacy del piano Team
Verificate con l'admin: uso dei dati per l'addestramento, retention, accesso ai Project condivisi. Documentate le impostazioni scelte.

### 10.4 Diritti d'autore e output generati
Gli output possono somigliare a materiali esistenti. Per il materiale pubblico: verificate loghi, font e immagini usati; non copiate testi protetti senza permesso.

### 10.5 Checklist prima della consegna
- [ ] Fatti e numeri verificati su fonte.
- [ ] Nessun dato sensibile o NDA nel materiale.
- [ ] Tono e brand rispettati.
- [ ] Test su mobile e browser diversi (per il digitale).
- [ ] Approvazione del referente.

---

## 11 — Workflow end-to-end

Ogni workflow ha: **obiettivo**, **passi**, **strumenti**, **punto di verifica umana**.

### 11.1 UX research e analisi dei competitor
- **Passi**: raccogliere materiali → sintesi per competitor → confronto su criteri → insight.
- **Strumenti**: ricerca web (con fonti), Project, Claude Design per il one-pager finale.
- **Verifica**: ogni insight deve avere una fonte.

### 11.2 Redesign di un sito
- **Passi**: audit (screenshot e analisi euristica) → brief del redesign → tre strutture → prototipo → revisione → handoff.
- **Strumenti**: Claude (analisi), Claude Design (prototipo), Figma MCP (token), Claude Code (implementazione).
- **Verifica**: test di usabilità con utenti reali; controllo accessibilità.

### 11.3 Nuovo prodotto digitale: dal brief al prototipo
- **Passi**: problema e utenti → user journey → brief → prototipo → test → iterazione.
- **Verifica**: il prototipo è testato con almeno 5 persone.

### 11.4 Campagna marketing: dalla strategia ai contenuti
- **Passi**: obiettivo e pubblico → messaggi chiave → piano dei contenuti → varianti → adattamento per canale → report.
- **Verifica**: approvazione del messaggio chiave prima della produzione.

### 11.5 Automazione di un processo di PM
- **Passi**: mappare il processo a mano → creare una Skill → collegare i connettori → attività programmate → verifica periodica.
- **Verifica**: un controllo umano a ogni report automatico.

### 11.6 Sviluppo software: dalla richiesta al deploy
- **Passi**: richiesta → CLAUDE.md aggiornato → plan mode → implementazione → test → commit → pull request → revisione → deploy.
- **Verifica**: revisione umana della PR e test passati prima del merge.

---

## 12 — Esercitazioni pratiche

### 12.1 Tre livelli, stesso compito
Stesso compito (es. una descrizione di servizio) in tre versioni: prompt semplice → BRIEF → Project con Skill. Confrontate i risultati e annotate cosa cambia a ogni livello.

### 12.2 Debug del prompt
Vi viene dato un prompt che non funziona. Individuate la lettera mancante del BRIEF, correggetelo, misurate il miglioramento su tre esecuzioni.

### 12.3 Il mio Project di ruolo
Costruite un Project completo: istruzioni, knowledge base, un compito di test. Presentate il risultato al team in tre minuti.

### 12.4 Dal Project alla Skill
Prendete un compito ripetuto del Project e trasformatelo in una Skill con passaggi, criteri e un esempio.

### 12.5 Da `.md` a HTML con Claude Code
Come nel cap. 07.9: un file Markdown diventa una presentazione HTML con il brand. Verificate il risultato su mobile.

### 12.6 Workshop finale a coppie miste
Coppie miste (es. design + sviluppo, marketing + PM) scelgono un workflow del cap. 11 e lo eseguono dall'inizio alla fine, con un output consegnabile e la checklist del cap. 10.

---

## 13 — Chiusura

### 13.1 Il playbook AI UX Boutique
Documento vivo: come usiamo l'AI, quali Skill esistono, quali dati non si caricano, chi è il referente per ogni area.

### 13.2 Prompt library per ruolo
Raccolta di BRIEF testati, uno per ruolo, con il risultato atteso e il motivo per cui funziona.

### 13.3 Quick reference
Una pagina: i cinque livelli, il BRIEF, la checklist del cap. 10, i tre modelli e quando usarli.

### 13.4 Repository starter su GitHub
Un repository di partenza con `CLAUDE.md` di esempio, struttura cartelle, Skill di base e template di brief.

### 13.5 Prossimi passi
Scegliete una Skill da creare entro due settimane, un workflow da automatizzare entro un mese, e un referente per il playbook.

---

### Note per la prossima versione
- Distribuzione dei capitoli sulle due giornate: da confermare. Il capitolo 06 (Claude Design) è il più pratico e potrebbe servire un'ora dedicata.
- Verificare in account tutti i passaggi dell'interfaccia (cap. 06 in particolare) prima di ogni sessione.
- Il capitolo 08 è il più lungo: in aula una demo per ruolo, il resto va nella dispensa.
