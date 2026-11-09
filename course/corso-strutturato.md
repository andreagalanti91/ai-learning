# Claude AI — Corso strutturato
### Dal prompt al building · Versione 1.0 · UX Boutique

---

## Come leggere questo corso

Questo è il documento di riferimento. Sostituisce `corso-approfondito.md` e `guida-operativa.md`, che restano come archivio.

**Ogni modulo ha la stessa struttura:**

| Sezione | A cosa serve |
|---|---|
| **Obiettivo** | Cosa saprete fare alla fine del modulo |
| **Prerequisiti** | Cosa dovete avere già pronto |
| **Concetto** | Cos'è la funzione e a cosa serve |
| **Come si imposta** | Passi di configurazione, una sola volta |
| **Come si usa** | Passi di utilizzo, ogni giorno |
| **Esempio completo** | Un caso reale dall'inizio alla fine |
| **Errori comuni** | Cosa va storto più spesso e come si corregge |
| **Verifica** | Domande per capire se avete capito |
| **Esercizio** | Lavoro pratico da fare in aula o a casa |

**Convenzioni.**
- **⚠ Da verificare** segna un passaggio che non ho confermato nella documentazione ufficiale. Nomi di menu e percorsi cambiano spesso: prima di ogni sessione, rifate il passaggio nel vostro account.
- I comandi da terminale sono in blocchi di codice. Si copiano così come sono.
- Gli esempi usano il contesto di UX Boutique. Sostituite i dettagli con quelli del vostro lavoro.

**Mappa del corso.**

| Parte | Moduli | Tema |
|---|---|---|
| A | 1–2 | Fondamenti e prompt |
| B | 3–4 | Contesto e output |
| C | 5–7 | Metodo e connessioni |
| D | 8–9 | Design e Figma |
| E | 10–11 | Claude Code |
| F | 12–13 | Operatività, qualità e privacy |
| G | 14–15 | Applicazione: ruoli e workshop finale |

---

## Parte A — Fondamenti

### Modulo 1 — Come funziona Claude

**Obiettivo.** Scegliere il modello giusto per un compito e riconoscere i limiti del sistema.

**Prerequisiti.** Un account Claude attivo con il piano Team.

**Concetto.** Claude è un modello linguistico: genera risposte a partire da ciò che vede nella conversazione. Non consulta un database e non ha memoria delle cose che non gli avete fornito. Da questo derivano tre conseguenze pratiche:
- è molto bravo con testo, struttura, ragionamento e codice;
- può sbagliare fatti, numeri e citazioni, e lo fa con sicurezza;
- la qualità dipende da quanto contesto gli date.

**Come si imposta.** Non c'è configurazione. Verificate il modello attivo nel selettore della chat *(⚠ da verificare: il nome del selettore cambia tra interfacce)*.

**Come si usa.**

*Tre modelli, tre scopi.*

| Modello | Quando usarlo | Esempio |
|---|---|---|
| **Haiku** | Compiti semplici, ripetitivi, in volume | Correggere 50 descrizioni prodotto |
| **Sonnet** | Lavoro quotidiano, il default consigliato | Scrivere un post, riassumere un verbale |
| **Opus** | Ragionamenti complessi e lavori delicati | Analizzare una strategia, un contratto, un bug difficile |

*Effort.* Alcune impostazioni fanno ragionare Claude più a lungo prima di rispondere. Più effort significa risposte più accurate su problemi complessi, ma tempi e utilizzo più alti. Per riscrivere un paragrafo non serve; per una decisione di design sì.

*Finestra di contesto.* Claude lavora su una quantità limitata di testo. In una chat molto lunga, le informazioni all'inizio possono perdere peso. Soluzioni: Project (modulo 3) e riassunti di chat.

*Verifica.* Ogni fatto, numero o citazione va controllato sulla fonte originale.

**Esempio completo.** Stessa domanda, tre modelli: "Riassumi questo verbale in cinque punti con responsabili e scadenze." Confrontate tempi, precisione e formato. Scegliete il modello più economico che rispetta la qualità richiesta.

**Errori comuni.**
- Usare sempre il modello più potente per tutto: lento e costoso.
- Fidarsi di una citazione senza aprire la fonte.
- Continuare una chat di tre giorni su un argomento nuovo: meglio aprirne una nuova.

**Verifica.**
1. Quale modello sceglieresti per 200 descrizioni prodotto da correggere? Perché?
2. Perché una chat molto lunga può dare risposte peggiori?

**Esercizio.** Scegliete un compito della vostra settimana. Eseguitelo con due modelli diversi e annotate differenza di qualità e tempo.

---

### Modulo 2 — Prompt con il metodo BRIEF

**Obiettivo.** Scrivere un prompt che produce un risultato utilizzabile al primo o secondo tentativo.

**Prerequisiti.** Un compito reale da svolgere.

**Concetto.** Un prompt semplice lascia a Claude tutte le decisioni: pubblico, tono, lunghezza, formato. Il metodo BRIEF rende esplicite queste scelte.

| Lettera | Parte | Domanda guida | Esempio |
|---|---|---|---|
| **B** | Background | Qual è il contesto? | "UX Boutique offre audit di usabilità per e-commerce medi." |
| **R** | Ruolo | Chi risponde, con quale competenza? | "Sei un copywriter senior, tono sobrio." |
| **I** | Intento | Cosa deve ottenere chi legge? | "Far richiedere un audit gratuito." |
| **E** | Esempi | Come deve essere il risultato? | "Tono come in questo esempio: …" |
| **F** | Formato | Lunghezza, struttura, cosa escludere? | "120 parole, due hashtag, niente emoji." |
| **+** | Verifica | Come controllo il risultato? | "Elenca le affermazioni che un cliente potrebbe contestare." |

**Come si imposta.** Nessuna configurazione. Salvate il BRIEF come modello in un documento, da riusare per ogni compito.

**Come si usa.**
1. Scrivete le sei parti, anche in forma breve.
2. Inviate la richiesta.
3. Leggete l'output e annotate cosa manca.
4. Correggete una cosa per volta: "Il titolo è troppo generico; proponi tre alternative con un numero."

**Tecniche utili.**
- **Tag XML** per separare istruzioni e materiali, ad esempio `<istruzioni>…</istruzioni>` e `<testo>…</testo>`. Claude distingue meglio cosa fare da cosa analizzare.
- **Few-shot**: due o tre esempi di output desiderato valgono più di una lunga descrizione.
- **Prompt a catena**: dividete un compito grande in passaggi (estrai i fatti → scrivi la bozza → rivedi con i criteri).
- **Autocritica**: "Rileggi la bozza rispetto a questi criteri e segnala cosa non rispetta."

**Esempio completo.**

*Prima (debole):* "Scrivi un post Instagram sul nostro servizio di audit."

*Dopo (BRIEF):*
```
Background: UX Boutique offre audit di usabilità per e-commerce di medie
dimensioni. Il pubblico sono responsabili marketing, non designer.

Ruolo: copywriter senior. Tono sobrio, concreto, senza superlativi.

Intento: far richiedere l'audit gratuito di 30 minuti.

Esempio di tono: "Il checkout perde utenti? Di solito il problema è in tre passaggi."

Formato: post di massimo 120 parole, italiano, due hashtag, nessuna emoji.
Chiudi con l'invito a prenotare.

Verifica: alla fine elenca le affermazioni che un cliente potrebbe contestare.
```

**Errori comuni.**
- Descrivere il compito ma non il pubblico.
- Chiedere "un tono professionale" senza esempio.
- Cambiare tre cose insieme nella revisione: non capite quale ha funzionato.
- Non dire cosa escludere: appaiono emoji, superlativi, citazioni inventate.

**Verifica.**
1. Quale lettera del BRIEF manca in "Scrivi una descrizione per il nostro prodotto"?
2. Perché conviene fare una revisione per volta?

**Esercizio.** Prendete un compito reale. Scrivete il prompt semplice, poi il BRIEF. Confrontate i due output e annotate la differenza.

---

## Parte B — Contesto e output

### Modulo 3 — Projects

**Obiettivo.** Creare un Project con istruzioni e documenti che rendono Claude coerente con il vostro lavoro senza ripetere il contesto ogni volta.

**Prerequisiti.** Almeno due documenti di riferimento approvati (guida al tono, testi di esempio, glossario).

**Concetto.** Un Project è uno spazio con tre parti:
- **Nome**: chiaro e riconoscibile.
- **Istruzioni**: regole permanenti che valgono per ogni chat del Project.
- **Knowledge base**: documenti che Claude può consultare.

Ogni chat aperta dentro il Project usa istruzioni e documenti senza che li ripetiate.

**Come si imposta.**
1. Nella barra laterale aprite **Projects** *(⚠ da verificare il nome della voce)* e scegliete **Nuovo Project**.
2. Assegnate un nome preciso: "UX Boutique — Brand & Tone".
3. Scrivete le istruzioni (template sotto).
4. Caricate i documenti nella knowledge base.
5. Nel piano Team, decidete se condividere il Project con il team *(⚠ da verificare: chi può condividere e con quali permessi)*.

*Template di istruzioni:*
```
Lavoriamo per UX Boutique, agenzia di UX e design digitale.
Lingua: italiano. Tono diretto e concreto, senza superlativi vuoti.
Ogni testo per clienti indica un beneficio misurabile.
Non citare mai clienti senza approvazione scritta.
Quando non sei sicuro di un fatto, dichiaralo.
Usa il glossario caricato; evita i termini segnati come "da non usare".
```

*Knowledge base: cosa caricare.*
- **Sì**: guida al tono, testi approvati come esempio, glossario, offerta ufficiale.
- **No**: bozze, duplicati, documenti con dati personali non necessari.
- **Formato**: file con testo selezionabile (non scansioni), titoli chiari, documenti brevi e focalizzati.

**Come si usa.**
1. Aprite una **nuova chat dentro il Project** (non fuori).
2. Chiedete il compito con un BRIEF più corto: il contesto c'è già.
3. Se il risultato ignora le istruzioni, verificate che la chat sia nel Project giusto.

**Esempio completo.** Nel Project "UX Boutique — Brand & Tone" chiedete: "Scrivi un'intro di 60 parole per la pagina servizi, audit di usabilità." Il risultato deve rispettare tono e glossario senza che li ripetiate. Confrontate con una chat fuori dal Project: la differenza mostra il valore del contesto.

**Errori comuni.**
- Istruzioni troppo lunghe e vaghe ("sii bravo e creativo"): Claude non ha regole da seguire.
- Documenti vecchi nella knowledge base: il risultato riflette la versione sbagliata.
- Modificare le istruzioni senza avvisare il team: i risultati cambiano senza spiegazione.

**Verifica.**
1. Cosa deve contenere una buona istruzione di Project? Fate due esempi.
2. Perché il test "intro di 60 parole" è utile?

**Esercizio.** Create il Project del vostro ruolo: istruzioni in cinque righe, due documenti di riferimento, un compito di test.

---

### Modulo 4 — Artifacts, ricerca web e analisi di file

**Obiettivo.** Ottenere documenti modificabili, informazioni recenti verificate e analisi di file affidabili.

**Prerequisiti.** Modulo 2 (BRIEF).

**Concetto.**
- **Artifact**: un output autonomo (documento, presentazione, foglio, pagina) che si apre accanto alla chat e si modifica senza ricominciare.
- **Ricerca web**: porta informazioni recenti. Va sempre verificata sulla fonte.
- **Analisi di file**: PDF, Excel/CSV, immagini e screenshot caricati nella chat.

**Come si imposta.** Nessuna configurazione. Verificate che la ricerca web sia attiva nel selettore degli strumenti *(⚠ da verificare il nome e la posizione)*.

**Come si usa.**

*Artifact.*
1. Chiedete esplicitamente il formato: "Crea un documento Artifact con…".
2. Per modificare una parte, indicatela: "Nella sezione *Metodo*, riduci a tre punti."
3. Esportate quando è pronto (copia, download; i formati disponibili dipendono dal tipo di output).

*Ricerca web.*
1. Definite la domanda in una frase, con periodo e pubblico.
2. Chiedete le fonti per ogni affermazione: "Indica fonte e data."
3. Aprite le fonti e verificate almeno le affermazioni che userete.

*Analisi di file.*
- **PDF**: "Estrai le date di scadenza dei contratti."
- **Excel/CSV**: "Calcola il costo per lead per canale e segnala gli anomali."
- **Screenshot**: "Individua problemi di contrasto e accessibilità."
- Caricate il file (icona di allegato), descrivete la domanda, chiedete un output strutturato, verificate un campione a mano.

**Esempio completo.** Caricate un CSV di campagne. Chiedete: "Calcola il costo per lead per canale, ordina dal più alto, segnala i canali con meno di 10 lead." Verificate il calcolo di un canale a mano. Solo dopo, usate la tabella nel report.

**Errori comuni.**
- Chiedere "migliora tutto" su un Artifact: cambia troppo.
- Fidarsi di un numero senza ricalcolarlo.
- Caricare una scansione di PDF: il testo non si legge bene.

**Verifica.**
1. Come si chiede una modifica precisa a un Artifact?
2. Quale verifica minima fate su un calcolo ricevuto da Claude?

**Esercizio.** Caricate un file reale. Chiedete un Artifact con tre domande precise. Annotate cosa avete dovuto correggere.

---

### Modulo 4b — Lavorare per file: il metodo markdown-first

**Obiettivo.** Preparare contenuti in file di testo nel repository, modificarli per parti e produrre l'artefatto visivo solo alla fine.

**Prerequisiti.** Modulo 4. Un repository Git (modulo 10 per la parte Git; può essere letto anche prima).

**Concetto.** Ci sono due modi di lavorare su un contenuto.
- **Su artefatto**: ogni modifica ripubblica la pagina intera. Il contenuto passa di nuovo per la chat e per lo strumento di pubblicazione.
- **Su file**: il contenuto vive in un file `.md` nel repository. Si modifica per sezioni, si verifica con Git e si trasforma in artefatto o presentazione solo quando è pronto.

Il secondo metodo è più economico in termini di token, perché le modifiche riguardano solo le parti toccate e non l'intero documento. Non è una misura precisa: il vantaggio è pratico e si vede soprattutto nei documenti lunghi e nelle revisioni frequenti. Ha anche altri vantaggi: la storia delle versioni, la possibilità di lavorare in parallelo sulle sezioni e un testo che resta leggibile e riutilizzabile.

**Quando usare quale.**

| Fase | Strumento | Perché |
|---|---|---|
| Bozza e struttura | File `.md` | Veloce da modificare, tracciato in Git |
| Revisione per sezioni | File `.md` | Modifiche piccole, verificabili |
| Versione per il team | Artefatto o presentazione | Leggibile, condivisibile |
| Versione finale | Export (HTML, PDF, PPTX) | Pronto per il cliente |

**Come si imposta.**
1. Create una cartella nel repository, ad esempio `contenuti/nome-progetto/`.
2. Dentro, un file per ogni sezione (`01-intro.md`, `02-servizi.md`) e un `indice.md` che le elenca nell'ordine.
3. Nel `CLAUDE.md` (modulo 11) scrivete la regola: "I contenuti di progetto si modificano nei file `.md`; gli artefatti si generano solo a fine lavoro."

**Come si usa.**
1. Chiedete a Claude di lavorare su un file specifico: "Modifica solo `02-servizi.md`: riduci a tre punti."
2. Verificate con `git diff`, che mostra esattamente cosa è cambiato.
3. Fate commit per ogni sezione approvata.
4. Quando l'insieme è pronto, chiedete l'artefatto o la presentazione a partire dai file.

**Esempio completo.** Presentazione di un progetto:
1. Struttura in `indice.md` con otto sezioni.
2. Ogni sezione scritta e revisionata come file, con un commit per sezione.
3. Revisione del cliente su una sezione alla volta, senza rigenerare tutto.
4. Generazione della presentazione finale dai file approvati.

**Errori comuni.**
- Creare l'artefatto presto: ogni modifica successiva lo rigenera per intero.
- File senza ordine: senza un `indice.md`, la struttura si perde.
- Modifiche non tracciate: senza commit non si capisce cosa è cambiato.

**Verifica.**
1. Perché conviene lavorare per file nelle prime fasi?
2. Quando passate dal file all'artefatto?

**Esercizio.** Prendete un contenuto reale di quattro sezioni. Scrivetelo in file `.md` con un `indice.md`. Fate tre revisioni su singole sezioni con un commit ciascuna, poi generate l'artefatto dai file.

---

## Parte C — Metodo e connessioni

### Modulo 5 — Skills

**Obiettivo.** Creare una Skill, installarla e farla attivare in modo affidabile, poi migliorarla con test ripetibili.

**Prerequisiti.** Un processo ripetuto con output giudicabile. Piano Team con Skills abilitate dall'admin (già confermato per il vostro team).

**Concetto.** Una Skill è un metodo scritto una volta e riutilizzabile. Si distingue dal prompt così:

| | Prompt | Skill |
|---|---|---|
| Quando si usa | Una volta | Ogni volta che il compito si ripete |
| Dove vive | Nella chat | In una cartella con `SKILL.md` |
| Chi la usa | Chi scrive | Chi ha la Skill disponibile (anche il team) |
| Come si attiva | Si scrive | Claude la sceglie dalla sua descrizione |

**Struttura della cartella.**
```
tono-ux-boutique/
├── SKILL.md
└── esempi/
    ├── post-buono.md
    └── post-da-evitare.md
```

**Regole della struttura** *(fonte: documentazione Anthropic sulle Skills; il nome della cartella deve coincidere con il campo `name`)*:
- la cartella ha il nome della Skill, in minuscolo con trattini;
- `SKILL.md` è obbligatorio e inizia con un frontmatter YAML con `name` e `description`;
- sono opzionali le cartelle di supporto (`scripts/`, `references/`, `assets/`).

**Template di SKILL.md.**
```markdown
---
name: tono-ux-boutique
description: Scrive o revisiona testi per UX Boutique secondo il tono di voce del brand. Usala quando l'utente chiede copy, post, claim, intro o revisione di testi per clienti o per il sito.
---

# Tono di voce UX Boutique

## Quando usarla
Testi per clienti, post social, pagine del sito, email commerciali.
Non usarla per documenti interni o codice.

## Procedura
1. Se mancano, chiedi pubblico, obiettivo e lunghezza.
2. Scrivi la bozza in italiano, tono diretto e concreto.
3. Ogni affermazione deve avere un beneficio misurabile, oppure va marcata "da verificare".
4. Applica il glossario: usa i termini "da usare", evita quelli "da non usare".
5. Rileggi la bozza rispetto ai criteri e segnala le violazioni.

## Criteri di qualità
- Nessun superlativo vuoto.
- Una sola call to action per testo.
- Frasi sotto le 25 parole.
- Nessun cliente citato senza approvazione.

## Esempi
Leggi prima `esempi/post-buono.md`, poi `esempi/post-da-evitare.md`.

## Formato di output
Testo finale, poi "Da verificare:" con le affermazioni da confermare.
```

**Come si imposta — claude.ai.**
1. Preparate la cartella `tono-ux-boutique/` con `SKILL.md`.
2. Comprimete la cartella in un file `.zip`. La cartella deve essere la radice dell'archivio, non i suoi file sparsi.
3. Nelle impostazioni dell'account, cercate la sezione **Skills** e scegliete di caricare la Skill dallo zip. *(⚠ da verificare: fonti diverse indicano percorsi diversi, ad esempio "Customize → Skills" oppure "Settings → Capabilities → Skills". Seguite il percorso del vostro account.)*
4. Attivate la Skill per il vostro account. Con il piano Team l'admin l'ha già abilitata: verificate che sia visibile a voi.

**Come si imposta — Claude Code.**
1. Nel repository, create `.claude/skills/tono-ux-boutique/SKILL.md`.
2. Fate commit: così la Skill è condivisa con chi lavora sul repository.
3. Per una Skill solo personale, usate la cartella dell'utente invece del repository *(⚠ da verificare il percorso personale nella documentazione di Claude Code)*.

**Come si usa.**
- Chiedete un compito che la Skill copre. Claude la sceglie e segue i passi.
- Per forzarne l'uso: "Usa la Skill tono-ux-boutique per questo testo."
- Per verificare quali Skill sono disponibili: "Quali Skill hai per questo compito?"

**Come si testa.** Preparate tre casi:
1. **Tipico**: il compito per cui è stata scritta. Deve attivarsi e rispettare i criteri.
2. **Al limite**: un compito simile ma non identico. Deve adattarsi o chiedere.
3. **Fuori scopo**: un documento interno. Non deve attivarsi.

Per ogni caso annotate: si è attivata? Ha seguito i passi? L'output rispetta i criteri?

**Esempio completo.** Skill "tono-ux-boutique".
- Caso tipico: "Scrivi un post per il servizio di audit." → si attiva, rispetta il glossario, chiede il pubblico se manca.
- Caso al limite: "Scrivi una mail commerciale." → si adatta, usa gli stessi criteri.
- Caso fuori scopo: "Riassumi il verbale della riunione interna." → non si attiva.

**Come si corregge.**

| Sintomo | Causa probabile | Correzione |
|---|---|---|
| Non si attiva mai | Descrizione vaga | Riscrivete la descrizione con le parole dell'utente |
| Si attiva sempre | Descrizione troppo ampia | Aggiungete "non usarla per…" |
| Si attiva ma sbaglia | Istruzioni ambigue o mancanti | Aggiungete un passo, un esempio "da evitare" |
| Non compare nella lista | Nome file o struttura errati | Controllate `SKILL.md` maiuscolo e frontmatter |
| Upload rifiutato | Zip con cartella annidata, nome non valido | Ricomprimete con la cartella come radice |

**Errori comuni.**
- Descrizione scritta per voi, non per Claude: "Strumento interno del reparto marketing" non dice quando usarla.
- Istruzioni lunghe senza gerarchia: dividete in passi numerati.
- Nessun test: la prima versione è sempre da correggere.

**Verifica.**
1. Quali due campi servono nel frontmatter e a cosa servono?
2. Perché la descrizione conta più del resto della Skill?
3. Quali tre casi di test servono e perché?

**Esercizio.** Trasformate un compito ripetuto del vostro ruolo in una Skill. Testatela sui tre casi e portate il risultato in aula.

---

### Modulo 6 — Connettori: Google Drive, Figma, Miro

**Obiettivo.** Collegare i tre strumenti del team, verificare i permessi concessi e usare i connettori in modo preciso.

**Prerequisiti.** Account personale per ciascuno strumento. Per il piano Team, l'owner o l'admin deve abilitare il connettore prima che i membri possano collegarlo *(fonte: guide di terze parti, da verificare nella documentazione ufficiale)*.

**Concetto.** Un connettore permette a Claude di leggere, e in alcuni casi scrivere, nei vostri strumenti. Il collegamento appartiene al vostro account Claude: una volta collegato, lo usate in chat, in Claude Code e nelle altre superfici dove il connettore è disponibile *(⚠ da verificare per superficie)*.

**Come si imposta.**

*Passaggio comune.*
1. Aprite le impostazioni e cercate **Connectors** *(⚠ da verificare il nome della voce)*.
2. Cercate lo strumento nel catalogo, scegliete **Connect** e accedete con il vostro account.
3. Verificate i permessi concessi: solo lettura o anche scrittura.
4. Se il pulsante dice **Request** invece di **Connect**, serve che l'admin abiliti il connettore per il team.

*Google Drive.* Accedete con l'account Google aziendale. Claude può leggere documenti, fogli, presentazioni e PDF secondo i permessi del vostro account *(fonte: guide di terze parti)*.

*Figma.* Servono un account Figma e un accesso ai team o ai file. Il connettore Figma è disponibile su qualsiasi piano Figma *(fonte: help center Figma)*. Se l'accesso è a livello di team, Claude vede solo i team autorizzati.

*Miro.* Collegate il vostro account Miro. Il connettore può risultare "connesso" ma va verificato in ogni conversazione: chiedete esplicitamente di usarlo *(fonte: guida di terze parti)*.

**Come si usa.** Le richieste precise funzionano meglio.
- Drive: "Cerca nel Drive la cartella del cliente X e riassumi l'ultimo brief caricato."
- Figma: "Dal file [nome o link], estrai i colori e i font del design system in JSON."
- Miro: "Nella board [nome], elenca le note del workshop raggruppate per tema."

**Esempio completo.** Workflow di un PM: Miro (note del workshop) → Skill "status report" → Drive (documento di progetto) → Artifact con lo status report. Ogni passaggio ha un controllo umano: verificate le note estratte prima di produrre il documento.

**Errori comuni.**
- Concedere più permessi del necessario (scrittura quando basta la lettura).
- Richieste vaghe: Claude trova il file sbagliato o una versione vecchia.
- Collegare strumenti con dati riservati senza verificare con l'admin.
- Scambiare "connesso" per "funzionante": testate con una domanda semplice.

**Verifica.**
1. Cosa fate se il pulsante dice "Request"?
2. Perché conviene chiedere il permesso minimo?
3. Come verificate che un connettore funzioni davvero?

**Esercizio.** Collegate Drive e Miro. Fate tre richieste reali (una per strumento) e annotate i risultati.

---

### Modulo 7 — MCP e Plugin

**Obiettivo.** Capire cosa sono MCP e i plugin, quando servono e quali rischi comportano.

**Prerequisiti.** Modulo 6.

**Concetto.**
- **MCP (Model Context Protocol)**: uno standard con cui uno strumento espone le sue funzioni a Claude. È la "presa USB": strumenti e Claude si collegano senza adattatori su misura.
- **Plugin**: un pacchetto che combina Skill, connettori e impostazioni per un ambito preciso (es. "project management").

**Come si imposta.**
- Per uno strumento con connettore già pronto (Drive, Figma, Miro): usate il connettore (modulo 6).
- Per un server MCP non presente nel catalogo, in Claude Code: `claude mcp add nome-server -- comando-del-server`. Per la lista: `claude mcp list`. *(⚠ da verificare la sintassi nella documentazione aggiornata di Claude Code.)*
- Per i plugin: cercate tra quelli disponibili nel vostro account e leggete cosa includono e quali permessi richiedono *(⚠ da verificare la sezione)*.

**Come si usa.** Installate solo ciò che potete spiegare. Un server MCP può fare azioni reali: scrivere su un file, inviare un messaggio. Controllate le azioni che Claude propone prima di confermarle, soprattutto se scrivono.

**Esempio completo.** Un team vuole un server per il proprio gestionale. Passi: verificare se esiste un server ufficiale → installarlo in un progetto di prova → chiedere solo letture → solo dopo abilitare le scritture, con revisione.

**Errori comuni.**
- Installare un server di cui non si conosce l'origine.
- Abilitare le scritture prima di aver testato le letture.

**Verifica.**
1. Qual è la differenza tra un connettore e un plugin?
2. Quali due controlli fate prima di installare un server MCP?

**Esercizio.** Elencate tre strumenti del vostro lavoro. Per ciascuno: esiste un connettore? Un server MCP? Cosa cambiereste nel workflow?

---

## Parte D — Design

### Modulo 8 — Claude Design

**Obiettivo.** Produrre un prototipo, una presentazione o un one-pager a partire da un brief, con contesto di brand, revisioni controllate ed export verificato.

**Prerequisiti.**
- Accesso a Claude Design nel vostro account. Claude Design è stato presentato come anteprima di ricerca (research preview) ad aprile 2026, e l'accesso può essere limitato per piano *(⚠ da verificare nel vostro account)*.
- Un brief con pubblico, obiettivo e formato.
- Il brand kit o il design system del progetto (colori in HEX, font, logo, componenti). Se non esiste, il modulo parte da riferimenti visivi.

**Concetto.** Claude Design genera output visivi a partire dalla conversazione: prototipi interattivi, slide, one-pager e landing page. Non è un generatore di immagini: produce strutture, testi e stili che si possono rivedere e modificare.

Cosa produce:
- **Prototipi**: pagine o flussi navigabili.
- **Slide**: presentazioni da topic, pubblico e numero di slide.
- **One-pager**: sintesi o proposte su una pagina.
- **Landing page**: pagine di campagna o di prodotto.

Cosa non produce: fotografie, illustrazioni originali, video. Per quelli servono altri strumenti (modulo 9 e cap. 09 del corso precedente).

**Come si imposta.**

*Passo 1 — Accesso.* Aprite Claude Design dal vostro account. Se non lo vedete, verificate il piano o chiedete all'admin. *(⚠ da verificare: il punto di accesso nell'interfaccia.)*

*Passo 2 — Contesto del brand (una volta sola).* Preparate un documento di brand con:
- palette con valori HEX (es. primario `#C96442`, testo `#1A1A1A`, sfondo `#FBFAF7`);
- font e pesi (es. titoli Space Grotesk 600, testo Inter 400);
- logo in formato vettoriale o PNG trasparente;
- tono di voce: tre aggettivi, un esempio di testo approvato, un elenco di termini da evitare.

Caricate questo documento nel Project del brand (modulo 3) e, se disponibile, collegatelo a Claude Design come riferimento *(⚠ da verificare il modo di collegarlo)*.

*Passo 3 — Verifica del contesto.* Prima di generare, chiedete: "Descrivi il brand che stai usando: colori, font, tono." Se la risposta non corrisponde al documento, correggete il contesto.

*Passo 4 — Brief.* Usate il BRIEF del modulo 2, con questi elementi:
- **Formato**: prototipo, slide, one-pager o landing.
- **Pubblico** e **obiettivo** (es. "far richiedere un audit gratuito").
- **Contenuto**: sezioni in ordine, con il messaggio di ciascuna.
- **Riferimento visivo**: uno screenshot di una pagina che vi piace, con una frase su cosa vi piace.
- **Vincoli**: mobile first, numero di slide, lingua.

*Passo 5 — Struttura prima dello stile.* Primo messaggio: "Proponi tre strutture diverse. Per ciascuna: sezioni in ordine e contenuto. Non applicare ancora colori né font." Scegliete una struttura.

*Passo 6 — Prototipo.* Secondo messaggio: "Procedi con la struttura 2. Applica il brand del contesto. Crea la versione mobile first."

*Passo 7 — Revisioni.* Una modifica per messaggio, con il perché: "Il titolo dell'hero è generico. Proponi tre alternative con un numero concreto. Applica la prima; non cambiare altro."

*Passo 8 — Verifica prima dell'export.*
- [ ] I contenuti e i numeri sono approvati e verificati.
- [ ] Colori e font corrispondono al brand kit.
- [ ] Il layout funziona su mobile.
- [ ] C'è una sola call to action.
- [ ] Nessun cliente è citato senza approvazione.

*Passo 9 — Export.* Le opzioni documentate da fonti di terze parti sono: download in `.zip`, PDF, PPTX, HTML autonomo, invio a Canva, e passaggio a Claude Code. Un export come immagine (PNG, JPEG, SVG) non risulta documentato; un export diretto in formato Figma non è confermato *(⚠ da verificare nel menu di export del vostro account)*.

Regola: esportate solo dopo il passo 8. Gli export sono più difficili da correggere della bozza.

| Formato | Quando | Attenzione |
|---|---|---|
| **HTML** | Prototipo navigabile, da condividere o da passare allo sviluppo | Controllate il mobile |
| **PDF** | One-pager o documento da inviare o stampare | Il testo non è facile da modificare |
| **PPTX** | Presentazione da modificare in PowerPoint o Keynote | Verificate che i font siano disponibili |
| **Canva** | Lavoro da completare in Canva | Dipende dal vostro account Canva |
| **Claude Code** | Passaggio della struttura allo sviluppo | Vedi modulo 11 |

**Come si usa — riepilogo.** Brief → tre strutture → una scelta → prototipo → revisioni singole → verifica → export. Il ciclo si ripete finché il risultato è giusto.

**Esempio completo.** Landing per il servizio di audit.
1. Contesto: Project "UX Boutique — Brand & Tone" con brand kit caricato. Verifica: la descrizione del brand corrisponde.
2. Brief: pubblico responsabili marketing e-commerce, obiettivo richiesta audit gratuito, sezioni hero, tre benefici misurabili, un caso studio, CTA, footer, mobile first.
3. Tre strutture. Scelta: la seconda, con caso studio in alto.
4. Prototipo con brand. Revisione: titolo dell'hero con numero concreto.
5. Verifica: il numero del caso studio è approvato; la CTA è una sola; il mobile è corretto.
6. Export in HTML per la revisione del cliente, PDF per la sintesi interna.

**Errori comuni.**

| Sintomo | Causa | Soluzione |
|---|---|---|
| Risultato generico | Brief vago | Aggiungete pubblico, obiettivo, sezioni con messaggio |
| Brand non riconoscibile | Contesto mancante o vecchio | Caricate il brand kit e verificate la descrizione |
| Claim non verificati | Nessuna regola di verifica | Aggiungete "marca come da verificare" nelle istruzioni |
| Mobile rotto | Non richiesto | Scrivete "mobile first" nel formato |
| Struttura e stile cambiano insieme | Due richieste in un messaggio | Separate struttura e stile |
| Export non come atteso | Non verificato prima | Eseguite il passo 8 prima dell'export |

**Verifica.**
1. Perché si chiede la struttura prima dello stile?
2. Quali elementi deve contenere un brief per Claude Design?
3. Quali controlli fate prima di esportare?

**Esercizio.** In coppie: scegliete un progetto reale (una pagina, una slide, un one-pager). Scrivete il brief, proponete tre strutture, scegliete la migliore, fate tre revisioni singole, verificate con la checklist, esportate. Consegnate il file esportato e il brief.

---

### Modulo 9 — Figma MCP e passaggio al codice

**Obiettivo.** Leggere token e componenti da Figma, usarli nel codice e mantenere una fonte unica.

**Prerequisiti.** Account Figma di team. Connettore Figma collegato (modulo 6). Un design system con token.

**Concetto.** Il flusso completo ha tre fasi:
1. **Design**: il brief diventa un prototipo (modulo 8).
2. **Figma**: il design system fornisce token (colori, spaziature, font) e componenti.
3. **Code**: Claude Code usa gli stessi token per generare il componente.

I token sono la fonte unica: se cambia un colore nel design system, cambia nel codice. Senza token, ogni passaggio ricrea le decisioni da capo.

**Come si imposta.**
1. Collegate il connettore Figma (modulo 6).
2. Verificate l'accesso: "Elenca i file Figma a cui hai accesso."
3. Organizzate i token in un file dedicato, ad esempio `design/tokens.json`, e tenetelo nel repository.

**Come si usa.**

*Leggere.* "Dal file [nome o link], estrai i colori e i font del design system in JSON." Verificate i valori sul file originale.

*Scrivere.* Claude può modificare il canvas Figma. Regola: fate le scritture su una copia o su una pagina di prova, e verificate prima di confermare, perché il file è del team.

*Passare al codice.* "Usando i token in `design/tokens.json`, crea il componente card con questo layout. Non introdurre colori fuori dai token." *(Vedi modulo 11 per il flusso in Claude Code.)*

**Esempio completo.** Componente card:
1. Estrazione dei token dal design system Figma → `design/tokens.json`.
2. Richiesta a Claude Code, in plan mode: componente card con i token.
3. Verifica: nessun valore hard-coded; il componente rispetta la spaziatura del design system.
4. Commit e revisione.

**Errori comuni.**
- Valori estratti e mai verificati sul file originale.
- Scritture dirette sul file del team.
- Colori inseriti nel codice invece dei token.

**Verifica.**
1. Perché i token sono una fonte unica?
2. Dove fate le prove di scrittura su Figma e perché?

**Esercizio.** Estraete tre token da un file Figma reale. Usateli per un componente in Claude Code. Verificate che non ci siano valori fuori dai token.

---

## Parte E — Agente

### Modulo 10 — Claude Code: installazione, cartelle, Git

**Obiettivo.** Installare Claude Code, avviarlo su una cartella di lavoro e usare Git per tenere le versioni.

**Prerequisiti.** Account Claude con accesso a Claude Code. Un computer con terminale, oppure l'app desktop.

**Concetto.** Claude Code è un agente che lavora dentro una cartella o un repository: legge, modifica e crea file, esegue comandi, con la vostra supervisione. Non è riservato agli sviluppatori: chi lavora su documenti in cartelle ne trae vantaggio.

- **Cartella**: un insieme di file. Claude Code lavora nella cartella da cui è avviato.
- **Repository**: una cartella con la storia delle modifiche (Git). Ogni modifica è tracciata e reversibile.

**Come si imposta.**

*Installazione.* Scegliete una via: app desktop oppure terminale. Per il terminale, seguite la documentazione ufficiale di installazione *(⚠ da verificare il comando aggiornato)*. Poi accedete con il vostro account.

*Primo avvio.*
```bash
cd percorso/della/cartella
git init                 # solo se la cartella non è già un repository
claude                   # avvia Claude Code nella cartella
```

**Come si usa.**
1. Chiedete una cosa semplice: "Elenca i file di questa cartella e spiega cosa contengono."
2. Verificate la risposta prima di chiedere modifiche.
3. Prima di ogni modifica importante, fate un commit.

*Git in breve.*
- **Commit**: una versione salvata con una descrizione.
- **Branch**: una linea di lavoro separata, per non toccare la versione principale.
- **Push**: invio delle modifiche al repository remoto (es. GitHub).
- **Pull request**: richiesta di unire un branch nel principale, con revisione.

```bash
git status                          # stato delle modifiche
git add percorso/del/file
git commit -m "Descrizione chiara"  # versione salvata
git log --oneline -5                # ultime versioni
```

**Esempio completo.** Cartella "landing-audit".
1. `git init`, primo commit con i file esistenti.
2. `claude` nella cartella; richiesta: "Spiega la struttura del progetto."
3. Richiesta di modifica in plan mode (modulo 11).
4. Verifica, commit con messaggio chiaro.

**Errori comuni.**
- Lavorare in una cartella senza Git: non si torna indietro.
- Commit troppo grandi, con modifiche non correlate: difficili da rivedere.
- Credenziali nei file del repository: non ci vanno mai.

**Verifica.**
1. Che differenza c'è tra cartella e repository?
2. Perché fate un commit prima di una modifica importante?

**Esercizio.** Create una cartella di prova con tre file. Inizializzate Git, fate il primo commit, chiedete a Claude Code di spiegare il contenuto, poi modificate un file e fate il secondo commit.

---

### Modulo 11 — CLAUDE.md, plan mode, permessi, subagent, comandi

**Obiettivo.** Configurare Claude Code per lavorare in modo prevedibile: istruzioni permanenti, piani approvati, permessi controllati.

**Prerequisiti.** Modulo 10.

**Concetto.**

**CLAUDE.md** è il file di istruzioni permanenti del progetto. Claude Code lo legge all'inizio della sessione. Esistono più livelli: un file nella radice del progetto (condiviso con il team), uno personale nella cartella dell'utente, e impostazioni a livello organizzazione *(fonti: guide di terze parti, da verificare nella documentazione ufficiale)*.

**Plan mode** fa sì che Claude proponga un piano e aspetti la vostra approvazione prima di modificare i file.

**Permessi**: Claude Code chiede conferma per modificare file ed eseguire comandi.

**Subagent**: agenti secondari che svolgono un sotto-compito e riportano il risultato. Claude Code include subagent integrati, tra cui Explore (ricerca nel codice) e Plan (usato in plan mode); la documentazione ufficiale indica che Explore e Plan non caricano CLAUDE.md, per restare veloci *(fonte: documentazione ufficiale dei subagent)*.

**Comandi slash**: comandi che iniziano con `/`, integrati o personalizzati.

**Come si imposta.**

*CLAUDE.md.* Create `CLAUDE.md` nella radice del repository. Lunghezza consigliata: poche centinaia di righe al massimo *(fonte: guida di terze parti, indicazione orientativa)*.

```markdown
# Progetto: landing audit UX Boutique

## Cos'è
Landing page per il servizio di audit. Lingua italiana.

## Stack
- HTML e CSS, nessun framework.
- Token di design in `design/tokens.json`.

## Regole
- Tono dei testi: `docs/tono-di-voce.md`.
- Non modificare la cartella `legacy/`.
- Non committare file con chiavi o credenziali.

## Come lavorare
- Prima di modifiche che toccano più file, mostra il piano e aspetta approvazione.
- Dopo ogni modifica, elenca i file cambiati.
```

*Plan mode.* Si attiva con Shift+Tab nel terminale, oppure con il comando `/plan`, oppure con il flag di avvio per permission mode plan *(⚠ da verificare nella versione installata)*.

*Permessi.* Quando Claude Code chiede un permesso, leggete cosa vuole fare. Potete concederlo per una singola azione o per la sessione. Non concedete "approva tutto" senza sapere cosa farà.

**Come si usa.**

1. Avviate `claude` nella cartella.
2. Per modifiche su più file: attivate plan mode, chiedete il piano, leggetelo.
3. Se un passo non è chiaro, chiedete di spiegarlo prima di approvare.
4. Approvate, verificate il risultato, fate commit.

*Esempio di richiesta in plan mode:*
```
Aggiungi alla landing una sezione "Caso studio" con tre numeri
da design/tokens.json. Non introdurre colori fuori dai token.
Mostra il piano con i file che tocchi.
```

**Esempio completo.** Sezione "Caso studio" nella landing:
1. Piano: file da modificare, token usati, nessun file nuovo fuori da `sezioni/`.
2. Approvazione dopo la lettura del piano.
3. Modifica, verifica del mobile, commit.

**Errori comuni.**
- Approvare un piano senza leggerlo.
- CLAUDE.md troppo lungo e confuso: le regole importanti si perdono.
- Permessi generici concessi per comodità.
- Subagent senza istruzioni chiare: fanno lavoro diverso dal previsto.

**Verifica.**
1. Cosa deve contenere un buon CLAUDE.md?
2. Cosa fate prima di approvare un piano?
3. Perché non concedere "approva tutto"?

**Esercizio.** Create un CLAUDE.md di dieci righe per un repository di prova. Chiedete una piccola modifica in plan mode. Leggete il piano prima di approvarlo.

---

## Parte F — Operatività

### Modulo 12 — Attività programmate

**Obiettivo.** Automatizzare un compito ripetuto con un controllo umano sull'output.

**Prerequisiti.** Una Skill o un Project già testati.

**Concetto.** Un'attività programmata esegue un compito a intervalli regolari (es. ogni lunedì, il report settimanale). Automatizzate solo ciò che avete già fatto a mano almeno una volta con esito positivo.

**Come si imposta.**
1. Scrivete il compito come lo dareste a un collega: input, passi, output, dove finisce il risultato.
2. Testatelo una volta a mano.
3. Programmate con l'intervallo desiderato *(⚠ da verificare dove si configura nel vostro account)*.
4. Definite il punto di arrivo dell'output (cartella, documento, canale).

**Come si usa.** Ogni output automatico passa da una revisione umana prima di essere inviato a un cliente o pubblicato.

**Esempio completo.** Report settimanale del progetto:
1. Compito a mano: leggere le note della settimana (Drive), riassumere in cinque punti (Skill "status report").
2. Programmazione: ogni lunedì mattina.
3. Output in un documento condiviso, con una riga "Da verificare".
4. Revisione del PM prima della condivisione.

**Errori comuni.**
- Automatizzare un compito mai verificato a mano.
- Inviare direttamente al cliente senza rileggere.
- Non definire dove finisce l'output.

**Verifica.**
1. Quali due condizioni servono prima di programmare un compito?
2. Dove va il controllo umano in un report automatico?

**Esercizio.** Scegliete un report ricorrente del vostro ruolo. Scrivete il compito come per un collega e fatelo una volta a mano.

---

### Modulo 13 — Qualità, privacy e checklist

**Obiettivo.** Verificare gli output, proteggere i dati e consegnare materiali affidabili.

**Prerequisiti.** Nessuno.

**Concetto.** Ogni output di Claude è una bozza da verificare. I rischi principali sono tre: fatti e numeri sbagliati, dati riservati caricati senza permesso, diritti d'autore su materiali generati o copiati.

**Come si imposta.** Verificate con l'admin le impostazioni privacy del piano Team: uso dei dati, conservazione, accesso ai Project condivisi. Documentate le scelte.

**Come si usa — regole.**
- **Verificate i fatti**: chi, cosa, quando. Aprite la fonte.
- **Ricalcolate i numeri** su un campione.
- **Eseguite il codice** e leggetelo prima di usarlo.
- **Non caricate** password, chiavi API, dati personali di clienti senza base legale, documenti coperti da NDA se non lo consentono.
- **Anonimizzate** quando dovete lavorare su casi reali.
- **Controllate gli asset**: loghi, font e immagini usati devono essere utilizzabili.

**Checklist prima della consegna.**
- [ ] Fatti e numeri verificati sulla fonte.
- [ ] Nessun dato sensibile o coperto da NDA.
- [ ] Tono e brand rispettati.
- [ ] Test su mobile e browser diversi (per il digitale).
- [ ] Asset utilizzabili.
- [ ] Approvazione del referente.

**Esempio completo.** Consegna di una landing: checklist completa, verifica dei numeri del caso studio con il cliente, controllo che il font sia licenziato per il web, approvazione del referente prima della pubblicazione.

**Errori comuni.**
- Consegnare senza rileggere perché "l'ha scritto Claude".
- Caricare un contratto reale per un test.
- Usare immagini trovate online senza licenza.

**Verifica.**
1. Quali tre rischi principali deve controllare chi usa Claude per il lavoro?
2. Cosa fate se un dato sensibile è già stato caricato per errore?

**Esercizio.** Prendete un output reale del vostro lavoro. Applicate la checklist e annotate cosa correggereste.

---

## Parte G — Applicazione

### Modulo 14 — Percorsi per ruolo

**Obiettivo.** Applicare il corso al proprio ruolo, con un percorso Base → Intermedio → Avanzato.

**Concetto.** Il livello si raggiunge quando un compito è ripetibile senza di voi. Ogni ruolo ha un percorso e un esercizio per livello.

**Marketing**
- **Base**: testi, post, varianti di copy. *Esercizio*: cinque varianti di un claim con tre toni.
- **Intermedio**: Project con brand e tono; piano editoriale mensile; analisi competitor con fonti. *Esercizio*: piano editoriale di un mese con fonti verificate.
- **Avanzato**: Skill del tono di voce; campagne con Claude Design; report da CSV. *Esercizio*: Skill "revisione copy" testata su dieci testi reali.

**Project Management**
- **Base**: verbali, email ai clienti, riassunti. *Esercizio*: verbale → cinque punti con responsabili e scadenze.
- **Intermedio**: Project per cliente; stime; rischi; status report. *Esercizio*: status report da note grezze.
- **Avanzato**: connettori Drive e Miro; Skill per gli status report; attività programmate. *Esercizio*: report automatizzato con verifica umana.

**UX/UI e Product Design**
- **Base**: sintesi di interviste, personas, microcopy. *Esercizio*: tre interviste → cinque bisogni con citazioni.
- **Intermedio**: user journey; architettura dell'informazione; analisi euristica da screenshot. *Esercizio*: analisi euristica di un flusso reale.
- **Avanzato**: token da Figma; prototipi con Claude Design; handoff a Claude Code; revisione di accessibilità. *Esercizio*: un componente dal design al codice con token condivisi.

**Art Direction e Graphic Design**
- **Base**: concept, moodboard testuali, naming, claim. *Esercizio*: tre concept per un evento con motivazione.
- **Intermedio**: brief creativi; analisi di riferimenti; varianti di layout. *Esercizio*: brief creativo completo.
- **Avanzato**: Claude Design per visual e one-pager; brand kit come contesto; export verso Canva. *Esercizio*: one-pager con brand kit ed export.

**Sviluppo**
- **Base**: spiegare codice, snippet, regex, query. *Esercizio*: spiegare una funzione riga per riga.
- **Intermedio**: debug, test, documentazione, code review. *Esercizio*: test per una funzione esistente.
- **Avanzato**: Claude Code con CLAUDE.md; subagent; GitHub; Figma MCP da design a codice. *Esercizio*: feature completa con piano, commit, revisione.

**Errori comuni.** Saltare al livello avanzato senza aver completato il base. Ogni livello prepara il successivo.

**Verifica.** Per il vostro ruolo: quale livello avete raggiunto? Quale compito è diventato ripetibile senza di voi?

---

### Modulo 15 — Workshop finale

**Obiettivo.** Eseguire un workflow completo dall'inizio alla fine in coppie miste, con un output consegnabile.

**Prerequisiti.** Moduli 1–13.

**Formato.** Coppie miste (es. design + sviluppo, marketing + PM). Ogni coppia sceglie un workflow:
- UX research e analisi dei competitor;
- redesign di una pagina;
- nuovo prodotto digitale dal brief al prototipo;
- campagna marketing dalla strategia ai contenuti;
- automazione di un processo di PM;
- sviluppo software dalla richiesta al commit.

**Passi.**
1. Definire il BRIEF del workflow.
2. Preparare il Project e, se serve, una Skill.
3. Collegare i connettori necessari.
4. Eseguire il workflow con almeno un output in Artifact o Claude Design.
5. Eseguire la checklist del modulo 13.
6. Presentare in tre minuti: cosa avete fatto, cosa avete verificato, cosa non avete fatto.

**Criteri di valutazione.**
- Il BRIEF usa tutte le parti necessarie.
- Il contesto è nel Project, non ripetuto.
- Ogni output ha un controllo umano documentato.
- La checklist è completa.

---

## Appendice A — Glossario

| Termine | Significato |
|---|---|
| **Artifact** | Output autonomo (documento, presentazione, foglio, pagina) modificabile accanto alla chat |
| **BRIEF** | Metodo a sei parti per scrivere un prompt completo |
| **CLAUDE.md** | File di istruzioni permanenti per Claude Code |
| **Connettore** | Collegamento di Claude a uno strumento (Drive, Figma, Miro) |
| **Effort** | Quanto Claude ragiona prima di rispondere |
| **Plan mode** | Modalità in cui Claude propone un piano prima di modificare |
| **MCP** | Standard con cui uno strumento espone funzioni a Claude |
| **Plugin** | Pacchetto di Skill, connettori e impostazioni |
| **Project** | Spazio con istruzioni e documenti condivisi tra le chat |
| **Skill** | Metodo riutilizzabile, in una cartella con `SKILL.md` |
| **Subagent** | Agente secondario che svolge un sotto-compito |
| **Token** | Valore di design (colore, spaziatura, font) usato in modo condiviso |

---

## Appendice B — Risoluzione problemi generale

| Problema | Cosa controllare | Soluzione |
|---|---|---|
| Risposta generica | Il BRIEF ha Background e Intento? | Aggiungete le parti mancanti |
| Contesto ignorato | La chat è nel Project giusto? | Aprite una nuova chat nel Project |
| Chat lenta o confusa | Chat molto lunga | Riassumete e aprite una chat nuova |
| Skill non attiva | Descrizione del frontmatter | Riscrivetela con le parole dell'utente |
| Connettore non trova il file | Nome esatto, permessi | Chiedete il link diretto |
| Connettore dice "Request" | Abilitazione del team | Chiedete all'owner o all'admin |
| Numeri sbagliati | Nessuna verifica | Ricalcolate un campione |
| Claude Code ignora CLAUDE.md | File nella radice? | Spostatelo e chiedete la verifica |

---

## Appendice C — Fonti e stato della verifica

Le informazioni di questo corso provengono da tre tipi di fonti. Ogni modulo indica quando un passaggio non è confermato.

- **Fonti ufficiali** (documentazione Anthropic e Figma): usate per la struttura delle Skill, i subagent di Claude Code, l'help center Figma.
- **Fonti di terze parti** (guide e blog): usate per i percorsi di menu, le scorciatoie, le opzioni di export di Claude Design. Vanno verificate nel vostro account.
- **Verifica interna**: l'indice e le decisioni del team (piano Team, Skills abilitate dall'admin, connettori Drive, Figma e Miro).

**Passaggi da verificare prima della prima sessione:**
1. Percorso di caricamento delle Skill su claude.ai.
2. Punto di accesso e opzioni di export di Claude Design nel vostro piano.
3. Abilitazione dei connettori Miro e Drive da parte dell'owner.
4. Scorciatoie e comandi di plan mode nella versione installata di Claude Code.
5. Sintassi aggiornata di `claude mcp add`.

---

## Note per la prossima versione

- Distribuzione dei moduli sulle due giornate da confermare.
- Il modulo 8 (Claude Design) è il più pratico: prevedete un'ora dedicata in aula.
- Aggiornare i passaggi marcati ⚠ dopo la prima verifica nel vostro account.
