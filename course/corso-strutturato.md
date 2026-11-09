# Claude per il lavoro
### Corso completo · versione 2.0 · UX Boutique

> Un corso per usare Claude nel lavoro di ogni giorno: marketing, design e sviluppo.
> Scritto in modo semplice, con esempi pronti da copiare.

---

## Come usare questo corso

Ogni capitolo ha sempre le stesse parti:

| Parte | Cosa trovi |
|---|---|
| **In breve** | L'idea in tre righe. Se leggi solo questo, hai capito il capitolo. |
| **Come funziona** | La spiegazione, con esempi della vita reale. |
| **Passo per passo** | Cosa fare, in ordine. |
| **Esempio** | Un caso completo, da copiare. |
| **Errori da evitare** | Cosa va storto più spesso. |
| **Prova tu** | Un esercizio di 10–20 minuti. |

**Simboli.**
- **⚠ Da verificare**: passaggio che non ho trovato confermato nella documentazione ufficiale, oppure che cambia spesso. Prima del corso, ricontrollalo nel tuo account.
- Il testo nei blocchi grigi è da copiare così com'è.

**Mappa del corso.**

| Parte | Capitoli | Domanda a cui risponde |
|---|---|---|
| 1 · Capire Claude | 1–3 | Cos'è Claude e quale versione uso? |
| 2 · Parlare con Claude | 4–5 | Come scrivo richieste che funzionano? |
| 3 · Claude nel lavoro | 6–8 | Cosa ci faccio in marketing, design e sviluppo? |
| 4 · Strumenti a fondo | 9–13 | Come uso Claude Design, Claude Code, Skill, Plugin, connettori? |
| 5 · Lavorare bene | 14–15 | Come lavoro in modo ordinato e sicuro? |
| 6 · Pratica | 16 | Da dove comincio? |

---

# Parte 1 · Capire Claude

## 1 · Claude in cinque minuti

### In breve
Claude è un assistente che legge, scrive, ragiona e lavora su file. È molto preparato, ma non conosce la tua azienda finché non gliela racconti. Più contesto gli dai, migliore è il risultato.

### Come funziona
Immagina un collega appena assunto, bravissimo e velocissimo:
- sa scrivere, analizzare, riassumere, programmare, organizzare;
- **non sa** chi sono i vostri clienti, che tono usate, cosa è stato deciso ieri;
- se non è sicuro di qualcosa, a volte **inventa** una risposta plausibile invece di dire "non lo so".

Da qui nascono tre regole d'oro:

1. **Dagli contesto.** Chi siamo, per chi lavoriamo, a cosa serve il lavoro.
2. **Digli cosa vuoi esattamente.** Formato, lunghezza, tono, cosa escludere.
3. **Controlla il risultato.** Fatti, numeri, nomi e citazioni vanno sempre verificati.

### Cosa sa fare bene
- Scrivere e riscrivere testi in molti toni e lingue.
- Riassumere documenti lunghi, verbali, interviste.
- Analizzare file: PDF, fogli Excel, immagini, screenshot.
- Ragionare su problemi: pro e contro, strategie, alternative.
- Scrivere e correggere codice.
- Creare documenti, presentazioni, prototipi.

### Cosa non fa (o fa male)
- Non genera fotografie o illustrazioni originali: per quelle servono altri strumenti.
- Non sa cosa è successo dopo il suo addestramento, a meno che non usi la ricerca web.
- Non ricorda le altre conversazioni, a meno che non usi Project e memoria (cap. 5).

### Prova tu
Chiedi a Claude: "Spiegami cosa fa un'agenzia UX in tre frasi." Poi chiedi la stessa cosa aggiungendo chi è il pubblico (per esempio "per il titolare di un piccolo e-commerce"). Confronta le due risposte.

---

## 2 · Le differenze tra i "Claude"

### In breve
Quando si dice "Claude" si intendono due cose diverse:
- **il modello**, cioè il "cervello": Haiku, Sonnet, Opus (e i nuovi nomi della famiglia);
- **il prodotto**, cioè il "posto di lavoro": la chat, Claude Design, Cowork, Claude Code.

Stesso cervello, posti di lavoro diversi per compiti diversi.

### 2.1 I modelli: il cervello

| Modello | Com'è | Quando usarlo | Esempio |
|---|---|---|---|
| **Haiku** | Il più veloce e leggero | Compiti semplici e ripetitivi | Correggere 50 descrizioni prodotto |
| **Sonnet** | Equilibrato tra velocità e qualità | Il lavoro di tutti i giorni: è la scelta di partenza | Un post, un riassunto, una correzione di codice |
| **Opus** | Il più profondo | Problemi complessi, lavori delicati, ragionamenti lunghi | Una strategia, un contratto, un bug difficile |

Oggi la famiglia più recente è la 5.5 (Opus 5.5, Sonnet 5.5, Haiku 5.5). Nella famiglia compare anche il nome **Fable**. **⚠ Da verificare** il suo posizionamento nel selettore dei modelli del tuo account.

**Regola pratica.** Parti con Sonnet. Passa a Opus quando la qualità non basta. Passa a Haiku quando conta la velocità.

**Ragionamento esteso (effort).** Alcune impostazioni fanno "pensare" Claude più a lungo prima di rispondere. Usalo per problemi complessi; per riscrivere un paragrafo non serve.

### 2.2 I prodotti: il posto di lavoro

| Prodotto | Cos'è | Chi lo usa | Cosa produce |
|---|---|---|---|
| **Chat** (claude.ai, app desktop, app mobile) | La conversazione, con file, ricerca web, Artifacts e Project | Tutti | Testi, analisi, documenti, piccole pagine |
| **Claude Design** | Uno spazio per creare visual parlando | Design, marketing, art direction | Prototipi, slide, one-pager, landing page |
| **Cowork** | Una scheda dell'app desktop in cui Claude lavora sui file del tuo computer | Chi lavora su documenti e cartelle, anche senza saper programmare | Documenti, fogli, file organizzati, compiti in più passaggi |
| **Claude Code** | Un agente che lavora dentro cartelle e repository, da terminale, app desktop, web o editor | Sviluppo, ma anche chi gestisce contenuti in file | Codice, file, siti, automazioni |
| **API** | Il modo per mettere Claude dentro i vostri prodotti | Sviluppatori | Funzioni AI nelle vostre app |

**⚠ Da verificare:** disponibilità di Cowork e Claude Design per il vostro piano Team. Claude Design è un'anteprima di ricerca di Anthropic Labs, disponibile per i piani Pro, Max, Team ed Enterprise.

### 2.3 La differenza che conta: chi fa il lavoro

| | Chat | Cowork | Claude Code |
|---|---|---|---|
| **Chi lavora** | Tu chiedi, Claude risponde | Claude esegue compiti in più passaggi | Claude esegue compiti in più passaggi |
| **Dove lavora** | Nella conversazione | Sui file del tuo computer | In una cartella o repository |
| **Quando usarlo** | Domande, testi, analisi | Lavori su documenti e cartelle | Codice, siti, file con versioni (Git) |
| **Livello tecnico** | Nessuno | Basso | Medio (si impara in un'ora) |

### 2.4 Quale scelgo?

| Voglio… | Uso… |
|---|---|
| Scrivere un post, una mail, un riassunto | Chat |
| Lavorare sempre con lo stesso contesto (cliente, brand) | Chat + Project |
| Creare un prototipo, una slide, una landing | Claude Design |
| Riordinare cartelle, produrre documenti da tanti file | Cowork |
| Scrivere codice, creare un sito, gestire file con versioni | Claude Code |
| Mettere Claude nel nostro prodotto | API |

### Prova tu
Prendi tre compiti della tua settimana. Per ciascuno scrivi quale prodotto useresti e con quale modello.

---

## 3 · I mattoni: Project, Artifact, Skill, Connettori, Plugin

### In breve
Oltre ai prodotti, Claude ha dei "mattoni" che si combinano. Pensa a una cucina:

| Mattone | Nella cucina | Nel lavoro | A cosa serve |
|---|---|---|---|
| **Project** | La cucina con la dispensa | Uno spazio con istruzioni e documenti fissi | Non ripetere il contesto ogni volta |
| **Skill** | La ricetta | Un metodo scritto una volta | Fare un compito sempre allo stesso modo |
| **Connettore** | La porta verso il fornitore | Il collegamento a Drive, Figma, Miro… | Leggere (e a volte scrivere) i vostri dati |
| **MCP** | Lo standard delle porte | Il "linguaggio" con cui uno strumento si collega a Claude | Collegare strumenti senza adattatori |
| **Plugin** | Il kit completo: ricette, attrezzi, fornitori | Un pacchetto di Skill, comandi, agenti, connettori | Installare tutto insieme |
| **Artifact** | Il piatto servito | Un output modificabile: documento, pagina, presentazione | Consegnare il risultato |

### Come si combinano
Esempio per un PM: il **connettore** Drive legge le note della riunione, la **Skill** "status report" le trasforma nel formato del team, dentro il **Project** del cliente, e il risultato esce come **Artifact** da condividere. Un **plugin** "Project Management" potrebbe installare tutto questo in un colpo solo.

### Prova tu
Pensa a un compito che ripeti ogni settimana. Quali mattoni ti servirebbero? Scrivilo in una riga, come nell'esempio.

---

# Parte 2 · Parlare con Claude

## 4 · Costruire un prompt che funziona

### In breve
Un prompt è una richiesta. Funziona quando contiene tutto quello che un collega bravo ti chiederebbe prima di iniziare: contesto, obiettivo, esempio, formato, cosa evitare. Il metodo **BRIEF** ti aiuta a non dimenticare niente.

### 4.1 Perché i prompt falliscono
Claude non legge nel pensiero. Se scrivi "fammi un post", deve indovinare: per chi? Su quale social? Con quale tono? Quanto lungo? Ogni cosa che non dici, la sceglie lui. E di solito sceglie la versione più generica.

### 4.2 Il metodo BRIEF

| Lettera | Parte | Domanda | Esempio |
|---|---|---|---|
| **B** | Background | Qual è il contesto? | "UX Boutique offre audit di usabilità per e-commerce di medie dimensioni." |
| **R** | Ruolo | Chi deve rispondere? | "Sei un copywriter senior, tono sobrio e concreto." |
| **I** | Intento | Cosa deve succedere dopo? | "Il lettore deve prenotare un audit gratuito." |
| **E** | Esempi | Come deve essere? | "Tono come questo: 'Il checkout perde utenti? Spesso il problema è in tre passaggi.'" |
| **F** | Formato | In che forma? | "Post LinkedIn, massimo 120 parole, niente emoji." |
| **+** | Verifica | Come controllo? | "Alla fine elenca le affermazioni da verificare." |

Non servono sempre tutte le lettere. Un compito semplice ne usa due o tre. Ma quando un risultato delude, quasi sempre manca una di queste.

### 4.3 Sette regole pratiche

1. **Prima il contesto, poi il compito.** Claude capisce meglio se sa a cosa serve il lavoro.
2. **Un obiettivo che si può verificare.** "Rendilo più chiaro" è vago. "Il cliente deve capire il prezzo in 5 secondi" si può controllare.
3. **Un esempio vale più di tre aggettivi.** "Professionale e moderno" non dice niente. Un paragrafo di esempio dice tutto.
4. **Il formato, sempre.** Lunghezza, struttura (elenco, tabella, paragrafi), lingua.
5. **Cosa escludere.** "Niente emoji", "non citare clienti", "non usare la parola *innovativo*".
6. **Separa istruzioni e materiali.** Metti il testo da analizzare tra tag: `<testo>…</testo>`. Claude capisce cosa è istruzione e cosa è materiale.
7. **Fatti fare domande.** Per compiti importanti: "Prima di iniziare, fammi le domande che ti servono." Così scopri cosa mancava.

### 4.4 Il modello da copiare

```
CONTESTO
[Chi siamo, per chi lavoriamo, situazione]

RUOLO
Sei [ruolo] con esperienza in [ambito].

OBIETTIVO
Voglio [risultato]. Dopo aver letto, il lettore deve [azione].

ESEMPIO
Ecco un esempio del tono/formato che voglio:
<esempio>
[testo di esempio]
</esempio>

FORMATO
- Lunghezza: [...]
- Struttura: [...]
- Da evitare: [...]

MATERIALI
<materiali>
[testi, dati, note da usare]
</materiali>

VERIFICA
Alla fine, elenca i punti di cui non sei sicuro.
```

### 4.5 Tre esempi completi

**Marketing — post per un servizio**
```
CONTESTO: UX Boutique offre audit di usabilità per e-commerce di medie
dimensioni. Il pubblico sono responsabili marketing, non designer.
RUOLO: copywriter senior, tono sobrio e concreto.
OBIETTIVO: il lettore deve prenotare l'audit gratuito di 30 minuti.
ESEMPIO DI TONO: "Il checkout perde utenti? Spesso il problema è in tre passaggi."
FORMATO: post LinkedIn, massimo 120 parole, due hashtag, niente emoji.
Chiudi con l'invito a prenotare.
VERIFICA: elenca le affermazioni che un cliente potrebbe contestare.
```

**Design — microcopy degli errori di un form**
```
CONTESTO: form di registrazione di un'app di prenotazione per parrucchieri.
Utenti: clienti 25–60 anni, spesso da telefono.
RUOLO: UX writer.
OBIETTIVO: messaggi di errore che spiegano cosa è successo e come risolvere.
FORMATO: tabella con colonne Campo | Errore | Messaggio. Massimo 12 parole
per messaggio. Niente colpe all'utente ("hai sbagliato"), niente punti esclamativi.
MATERIALI: <campi>nome, email, telefono, password, data di nascita</campi>
VERIFICA: segnala i messaggi che potrebbero non essere chiari a un utente anziano.
```

**Sviluppo — capire un bug**
```
CONTESTO: sito in Next.js. Dopo l'aggiornamento, il carrello si svuota
quando l'utente ricarica la pagina.
RUOLO: sviluppatore senior.
OBIETTIVO: capire la causa più probabile e come verificarla, prima di
modificare il codice.
FORMATO: 1) tre ipotesi in ordine di probabilità, 2) per ognuna un test
per confermarla, 3) la correzione solo per l'ipotesi confermata.
MATERIALI:
<codice>[incolla il componente del carrello]</codice>
<errore>[incolla l'errore della console]</errore>
VERIFICA: dimmi cosa non puoi sapere senza vedere altri file.
```

### 4.6 Tecniche avanzate

| Tecnica | Cos'è | Quando usarla |
|---|---|---|
| **Esempi multipli (few-shot)** | Dai 2–3 esempi di output | Quando il formato è difficile da spiegare a parole |
| **Tag** | `<testo>`, `<dati>`, `<esempio>` | Quando incolli materiali lunghi |
| **Catena di prompt** | Dividi il compito in passaggi | Compiti grandi: prima i fatti, poi la bozza, poi la revisione |
| **Criteri e autocritica** | "Rileggi rispetto a questi criteri" | Quando la qualità deve essere costante |
| **Alternative** | "Proponi tre versioni diverse" | Titoli, concept, strutture |
| **Domande prima** | "Fammi le domande che ti servono" | Compiti importanti o poco chiari |
| **Ragionamento esteso** | Più tempo per pensare | Strategie, analisi, bug complessi |

### 4.7 Come dare feedback
Usa la formula **cosa + perché + come**:
- ❌ "Non mi piace."
- ✅ "Il titolo (**cosa**) è troppo generico per un pubblico tecnico (**perché**): proponi tre alternative con un numero concreto (**come**)."

Una correzione per messaggio. Se cambi tre cose insieme, non capisci quale ha funzionato.

### 4.8 Quando non funziona: diagnosi

| Sintomo | Causa probabile | Correzione |
|---|---|---|
| Risposta generica | Manca il contesto o il pubblico | Aggiungi Background e Intento |
| Tono sbagliato | Nessun esempio | Incolla un testo di esempio |
| Troppo lungo | Formato non indicato | Indica parole, righe, struttura |
| Inventa fatti | Nessuna fonte | Dagli i documenti; chiedi di segnalare le incertezze |
| Ignora una regola | Regola sepolta in un testo lungo | Mettila in un elenco "Da evitare" |
| Cambia troppo nella revisione | Feedback vago | Indica la parte precisa e cosa non toccare |

### 4.9 Checklist prima di inviare
- [ ] Ho detto chi siamo e per chi è?
- [ ] Ho detto cosa deve succedere dopo?
- [ ] Ho dato un esempio?
- [ ] Ho indicato lunghezza e formato?
- [ ] Ho detto cosa evitare?
- [ ] Ho chiesto di segnalare le incertezze?

### Prova tu
Prendi un prompt che hai usato questa settimana. Riscrivilo con il modello del 4.4. Confronta i due risultati e annota cosa è cambiato.

---

## 5 · Contesto: Project e memoria

### In breve
Un **Project** è uno spazio con istruzioni e documenti che valgono per tutte le chat al suo interno. Lo prepari una volta e non ripeti più il contesto.

### Passo per passo
1. Nella barra laterale apri **Projects** e crea un nuovo Project. *(⚠ verifica il nome della voce)*
2. Dai un nome chiaro: "UX Boutique — Brand & Tone", oppure "Cliente Rossi — Redesign".
3. Scrivi le **istruzioni** (5–10 righe).
4. Carica i **documenti** di riferimento.
5. Nel piano Team, condividilo con chi lavora sullo stesso cliente. *(⚠ verifica i permessi)*
6. Apri sempre le chat **dentro** il Project.

### Istruzioni: modello
```
Lavoriamo per UX Boutique, agenzia di UX e design digitale.
Lingua: italiano. Tono diretto e concreto, niente superlativi.
Ogni testo per clienti indica un beneficio misurabile.
Non citare mai clienti senza approvazione scritta.
Quando non sei sicuro di un fatto, dichiaralo.
Usa il glossario caricato.
```

### Cosa caricare
- **Sì:** guida al tono, testi approvati, glossario, offerta ufficiale, brief del cliente.
- **No:** bozze vecchie, duplicati, dati personali non necessari.

### Memoria e chat lunghe
- Claude può ritrovare informazioni da chat precedenti. Verifica sempre che siano ancora valide.
- Una chat molto lunga perde precisione. Quando cambi argomento, chiedi un riassunto e apri una chat nuova:
```
Riassumi questa chat in: decisioni prese, file usati, cose da fare.
Lo userò per iniziare una nuova conversazione.
```

### Errori da evitare
- Istruzioni vaghe ("sii creativo") invece di regole precise.
- Documenti vecchi nella knowledge base.
- Cambiare le istruzioni di un Project condiviso senza avvisare.

### Prova tu
Crea il Project del tuo ruolo. Chiedi: "Scrivi un'intro di 60 parole per la pagina servizi." Se rispetta tono e regole senza che tu le ripeta, funziona.

---

# Parte 3 · Claude nel lavoro

## 6 · Marketing

### In breve
Claude aiuta in tutto il ciclo del marketing: dalla strategia ai contenuti, dalle campagne all'analisi dei risultati. Il lavoro più utile non è "scrivimi un post", ma costruire un sistema: Project con brand e tono, Skill per i formati ripetuti, verifica di ogni dato.

### Cosa puoi fare

| Area | Esempi di compiti | Strumento |
|---|---|---|
| **Strategia** | Posizionamento, personas, analisi dei competitor, piano marketing | Chat con ricerca web, Project |
| **Contenuti** | Post, articoli, newsletter, script video, varianti di copy | Chat + Project + Skill |
| **Campagne** | Concept, headline, testi annunci, landing page | Chat, Claude Design |
| **SEO e AI search** | Struttura articoli, domande frequenti, ottimizzazione per motori di ricerca e assistenti AI | Chat con ricerca web |
| **Analisi** | Report da CSV o Excel, confronto canali, sintesi dei risultati | Chat con file, Cowork |
| **Email** | Sequenze di benvenuto, nurturing, riattivazione | Chat + Skill |

### Prompt pronti

**Piano editoriale**
```
CONTESTO: [azienda, prodotto, pubblico].
OBIETTIVO: piano editoriale di 4 settimane per LinkedIn e Instagram.
FORMATO: tabella con Settimana | Canale | Tema | Formato | Titolo | Obiettivo.
3 post a settimana per canale. Alterna contenuti utili, casi studio, dietro le quinte.
DA EVITARE: date di eventi inventate, statistiche senza fonte.
```

**Analisi dei competitor**
```
Analizza questi tre competitor: [link]. Per ciascuno: a chi si rivolge,
promessa principale, prezzi visibili, punti forti, punti deboli.
Formato: tabella, poi tre opportunità per noi.
Indica la fonte di ogni informazione.
```

**Varianti di headline**
```
Scrivi 10 headline per [landing/annuncio]. Pubblico: [chi].
Beneficio principale: [cosa]. 5 orientate al problema, 5 al risultato.
Massimo 8 parole. Poi indica le 3 migliori e perché.
```

**Report dai dati**
```
<dati>[incolla il CSV o carica il file]</dati>
Calcola costo per lead e tasso di conversione per canale.
Ordina dal migliore al peggiore. Segnala i valori anomali.
Formato: tabella + 3 osservazioni + 2 azioni consigliate.
Mostra i calcoli di un canale, così posso verificarli.
```

### Skill di marketing già installate nel repo
Nel repository ci sono 53 Skill di marketing (pacchetto `coreyhaines31/marketingskills`), per esempio `copywriting`, `copy-editing`, `content-strategy`, `social`, `ad-creative`, `emails`, `marketing-plan`, `seo-audit`. In Claude Code si attivano da sole quando il compito corrisponde. Per usarle in chat, vanno caricate nel tuo account (cap. 11). Esiste anche un plugin ufficiale "Marketing" per Cowork. **⚠ Da verificare** la disponibilità nel vostro piano.

### Workflow completo: una campagna
1. **Brief** (chat + Project): obiettivo, pubblico, messaggio chiave, canali.
2. **Concept** (chat): tre direzioni creative, una scelta.
3. **Testi** (chat + Skill `copywriting`): headline, post, testi annunci.
4. **Visual e landing** (Claude Design): prototipo della landing e one-pager.
5. **Revisione** (chat + Skill `copy-editing`): tono, chiarezza, claim.
6. **Verifica umana**: ogni numero e claim controllato, approvazione del cliente.

### Errori da evitare
- Pubblicare statistiche o citazioni senza aver controllato la fonte.
- Chiedere "un post virale": senza pubblico e obiettivo, il risultato è generico.
- Usare lo stesso testo su tutti i canali: chiedi un adattamento per ciascuno.

### Prova tu
Scegli un servizio reale. Chiedi 10 headline con il prompt sopra, scegli le tre migliori e chiedi un post LinkedIn per ciascuna.

---

## 7 · Design: UX, UI e art direction

### In breve
Claude non sostituisce il designer: accelera le parti di analisi, scrittura e prima esplorazione. Sintetizza ricerche, scrive microcopy, valuta schermate, genera prototipi con Claude Design e legge i file Figma tramite connettore.

### Cosa puoi fare

| Area | Esempi di compiti | Strumento |
|---|---|---|
| **Ricerca** | Sintesi di interviste, personas, job to be done, insight | Chat con file |
| **Architettura** | User journey, sitemap, flussi, architettura dell'informazione | Chat, Artifact |
| **Valutazione** | Analisi euristica da screenshot, accessibilità, coerenza | Chat con immagini |
| **Contenuti UI** | Microcopy, messaggi di errore, stati vuoti, onboarding | Chat + Project |
| **Prototipi** | Landing, flussi, slide, one-pager | Claude Design |
| **Design system** | Lettura di token e componenti da Figma | Connettore Figma |
| **Art direction** | Concept, moodboard testuali, naming, brief per generatori di immagini | Chat |

### Prompt pronti

**Sintesi di interviste**
```
<interviste>[incolla trascrizioni o carica i file]</interviste>
Trova i 5 bisogni più ricorrenti. Per ciascuno: descrizione, quante
persone lo citano, due citazioni testuali con il nome dell'intervista.
Poi le 3 contraddizioni più interessanti.
Non inventare citazioni: usa solo testo presente nelle interviste.
```

**Analisi euristica da screenshot**
```
[carica lo screenshot]
Valuta questa schermata con le 10 euristiche di Nielsen.
Per ogni problema: euristica, dove si trova, gravità (1–4), proposta.
Formato: tabella ordinata per gravità. Poi i 3 interventi più rapidi.
```

**Revisione di accessibilità**
```
[carica lo screenshot o incolla l'HTML]
Controlla contrasto, dimensione dei testi, etichette dei campi, ordine
di lettura, dimensione dei target touch. Indica il criterio WCAG
di riferimento per ogni problema. Segnala ciò che non puoi verificare
da un'immagine.
```

**Brief per un generatore di immagini**
```
Scrivi 3 prompt per un generatore di immagini per la campagna [nome].
Concept: [idea]. Stile: [riferimenti]. Formato: 4:5 per Instagram.
Per ogni prompt: soggetto, ambientazione, luce, inquadratura, palette.
```

### Skill di design già installate nel repo
Nel repository ci sono le Skill del pacchetto `emilkowalski/skill`, tra cui `emil-design-eng` (rifinitura delle interfacce), `apple-design` (interfacce fluide in stile Apple), `mobile-native` (esperienza da telefono), `review-animations` e `break-ui` (stress test con dati estremi). Le abbiamo usate per rifinire la presentazione di questo corso.

### Workflow completo: redesign di una pagina
1. **Audit**: screenshot della pagina attuale + analisi euristica.
2. **Ricerca**: sintesi dei feedback degli utenti.
3. **Brief**: obiettivo, pubblico, problemi da risolvere.
4. **Prototipo**: tre strutture in Claude Design, una scelta, revisioni (cap. 9).
5. **Design system**: token da Figma tramite connettore.
6. **Handoff**: passaggio a Claude Code per lo sviluppo (cap. 10).
7. **Verifica**: test con utenti reali e controllo di accessibilità.

### Errori da evitare
- Prendere un'analisi euristica come test con utenti: è un'ipotesi da verificare.
- Lasciar inventare citazioni nella sintesi delle interviste.
- Scrivere direttamente sui file Figma del team: lavora su una copia.

### Prova tu
Fai uno screenshot di una pagina di un cliente. Chiedi l'analisi euristica e confronta i tre interventi proposti con quelli che avresti scelto tu.

---

## 8 · Sviluppo

### In breve
Claude aiuta a capire, scrivere, correggere e documentare codice. Per il lavoro vero, lo strumento è **Claude Code**, che lavora direttamente nel repository: legge i file, propone un piano, modifica, esegue i test, prepara i commit.

### Cosa puoi fare

| Area | Esempi di compiti | Strumento |
|---|---|---|
| **Capire** | Spiegare codice, mappare un progetto, documentare | Claude Code |
| **Scrivere** | Funzioni, componenti, script, query, regex | Chat o Claude Code |
| **Correggere** | Debug, analisi di errori, regressioni | Claude Code |
| **Qualità** | Test, code review, refactoring, sicurezza | Claude Code |
| **Design to code** | Componenti dai token del design system | Claude Code + Figma |
| **Automazione** | Script ripetitivi, migrazioni, attività programmate | Claude Code |

### Prompt pronti (in Claude Code)

**Capire un progetto nuovo**
```
Spiegami questo progetto: a cosa serve, struttura delle cartelle,
come si avvia, come si eseguono i test. Indica i 5 file più importanti.
Non modificare nulla.
```

**Correggere un bug**
```
Il carrello si svuota quando si ricarica la pagina. Trova la causa.
Prima scrivi un test che riproduce il bug, poi correggi, poi esegui
tutti i test. Mostrami il piano prima di modificare.
```

**Code review**
```
Fai una review delle modifiche di questo branch rispetto a main.
Cerca: bug, casi limite non gestiti, problemi di sicurezza, codice
duplicato. Ordina per gravità. Per ognuno: file, riga, problema, proposta.
```

**Componente dai token**
```
Usando i token in design/tokens.json, crea il componente Card come nello
screenshot allegato. Nessun colore o spaziatura fuori dai token.
Aggiungi una pagina di esempio con tre varianti.
```

### Workflow completo: una nuova funzione
1. **Richiesta** chiara: cosa deve fare, per chi, come si verifica.
2. **CLAUDE.md** aggiornato con regole e comandi del progetto.
3. **Plan mode**: Claude propone il piano, tu lo leggi e lo approvi.
4. **Implementazione** su un branch separato.
5. **Test** eseguiti da Claude e verificati da te.
6. **Commit e pull request** con descrizione.
7. **Review umana** prima del merge.

### Errori da evitare
- Approvare un piano senza leggerlo.
- Accettare codice senza eseguirlo e leggerlo.
- Mettere password o chiavi nei file del repository.

### Prova tu
Apri un piccolo progetto con Claude Code. Chiedi la spiegazione del progetto con il primo prompt sopra, senza modifiche.

---

# Parte 4 · Strumenti a fondo

## 9 · Claude Design

### In breve
Claude Design crea **prototipi, slide, one-pager e landing page** parlando, usando il design system della tua organizzazione. Si imposta una volta il design system, poi ogni progetto del team lo usa in automatico. È un'anteprima di ricerca di Anthropic Labs, presentata ad aprile 2026.

### 9.1 Quando usarlo

| Strumento | Ideale per | Non ideale per |
|---|---|---|
| **Claude Design** | Visual coerenti con il brand, prototipi, slide, one-pager, landing | Foto, illustrazioni, video |
| **Artifact in chat** | Documenti e pagine veloci, uso interno | Materiali che devono rispettare il brand |
| **Figma** | Design di dettaglio, collaborazione tra designer, design system | Esplorazioni rapide da un brief |

### 9.2 Chi può usarlo
- Disponibile come anteprima di ricerca per i piani **Pro, Max, Team ed Enterprise**.
- Su **Enterprise** è disattivato di default: l'admin lo attiva in *Organization settings → Capabilities → Anthropic Labs*.
- **⚠ Da verificare** nel vostro account Team: punto di accesso e funzioni attive.

### 9.3 Prima volta: il design system dell'organizzazione
Senza design system, Claude Design produce lavori funzionali ma **non riconoscibili come vostri**. Per questo il primo passo è impostarlo.

**Chi lo fa.** Il designer o il responsabile del brand. Anthropic consiglia di partire con un piccolo gruppo di 2–4 designer di fiducia, che creano e verificano il design system prima di aprirlo al resto del team.

**Passo per passo.**
1. **Crea l'organizzazione** e completa la procedura iniziale.
2. **Carica i materiali del brand e del prodotto**: codice dei siti, presentazioni, file di design, riferimenti visivi. Più sono rappresentativi, meglio è.
3. **Lascia che Claude estragga** colori, tipografia e componenti.
4. **Rivedi** il risultato. Se è debole, carica materiali diversi o aggiuntivi.
5. **Pubblica** il design system per il team.

Da quel momento, nei piani Team ed Enterprise, i progetti di tutti usano automaticamente il design system pubblicato. Quando il brand cambia, si aggiorna in Claude Design.

**Cosa preparare prima.**
- Palette con valori esatti (es. HEX).
- Font e pesi usati.
- Logo in buona qualità.
- 3–5 esempi di lavori approvati (pagine, slide, materiali).
- Tono di voce: tre aggettivi e un testo di esempio.

### 9.4 Creare un progetto, passo per passo

1. **Scegli cosa creare**: prototipo, slide, one-pager o landing.
2. **Scrivi il brief** (BRIEF del cap. 4): pubblico, obiettivo, sezioni con il loro messaggio, vincoli.
3. **Chiedi la struttura prima dello stile.**
4. **Scegli una struttura** e genera la prima versione.
5. **Rivedi una cosa per volta.**
6. **Verifica** contenuti, brand, mobile.
7. **Esporta** o passa il lavoro.

### 9.5 Prompt pronti

**Landing page**
```
Crea una landing per il nostro audit di usabilità gratuito.
Pubblico: responsabili marketing di e-commerce di medie dimensioni.
Obiettivo: prenotazione dell'audit di 30 minuti.
Sezioni: hero con promessa e CTA; tre benefici misurabili; un caso
studio; come funziona in 3 passi; domande frequenti; CTA finale.
Vincoli: mobile first, una sola CTA ripetuta, nessun numero inventato
(usa segnaposto come [X%] dove servono dati).
Prima proponi tre strutture diverse, senza applicare lo stile.
```

**Slide**
```
Crea una presentazione di 8 slide per presentare il redesign al cliente.
Pubblico: direttore marketing, poco tempo.
Struttura: problema, dati attuali, cosa cambiamo, prima/dopo,
impatto atteso, tempi, costi, prossimi passi.
Una idea per slide, testo minimo, grafici dove servono.
```

**One-pager**
```
Crea un one-pager sul nostro servizio di UX research.
Per chi: startup in fase di crescita. Contenuto: problema, cosa facciamo,
come lavoriamo (3 fasi), risultati tipici, contatti.
Deve stare su una pagina A4 ed essere leggibile anche stampato.
```

### 9.6 Revisioni che funzionano
- **Una modifica per messaggio**, con il perché: "Il titolo è generico: proponi tre alternative con un numero. Applica la prima; non cambiare altro."
- **Indica la sezione** precisa, non "migliora tutto".
- **Separa struttura e stile**: prima l'ordine delle sezioni, poi colori e font.
- **Usa i segnaposto** per i dati che non hai: `[X clienti]`, `[Y%]`.

### 9.7 Esportare e passare il lavoro
Opzioni riportate dalle fonti: download `.zip`, **PDF**, **PPTX**, **HTML** autonomo, invio a **Canva**, passaggio a **Claude Code** per lo sviluppo. Export come immagine ed export in formato Figma non risultano confermati. **⚠ Da verificare** nel menu di export.

| Formato | Quando |
|---|---|
| HTML | Prototipo da mostrare o da passare allo sviluppo |
| PDF | One-pager da inviare o stampare |
| PPTX | Presentazione da modificare in PowerPoint o Keynote |
| Canva | Lavoro da completare in Canva |
| Claude Code | Trasformare il prototipo in un sito vero |

### Errori da evitare
- Partire senza design system: il risultato non sembra vostro.
- Brief vago: "fammi una bella landing" dà un risultato generico.
- Chiedere struttura e stile insieme.
- Esportare prima di aver verificato numeri e claim.

### Prova tu
Con un brief reale, chiedi tre strutture di landing, scegline una, fai tre revisioni singole ed esporta in PDF.

---

## 10 · Claude Code

### In breve
Claude Code è un **agente**: non risponde solo, **fa**. Lavora dentro una cartella, legge e modifica file, esegue comandi, propone un piano e aspetta il tuo ok. È nato per lo sviluppo, ma è utile a chiunque lavori con file: testi, contenuti, presentazioni, dati.

### 10.1 Dove si usa
- **Terminale** (la riga di comando).
- **App desktop**.
- **Web** (claude.ai/code), anche su repository GitHub.
- **Editor di codice** (VS Code, JetBrains).

Stesso agente, interfacce diverse. Per chi non programma, l'app desktop o il web sono il punto di partenza più semplice.

### 10.2 Primo avvio
1. Installa Claude Code (app desktop o terminale) seguendo la documentazione ufficiale. *(⚠ verifica il comando aggiornato)*
2. Apri una cartella di lavoro. Meglio se è un **repository Git**, così ogni modifica si può annullare.
3. Prima richiesta, senza modifiche:
```
Spiegami cosa c'è in questa cartella e come è organizzata.
Non modificare nulla.
```
4. Poi una piccola modifica, in plan mode (10.4).

Da terminale:
```bash
cd percorso/della/cartella
git init     # solo se non è già un repository
claude       # avvia Claude Code
```

### 10.3 CLAUDE.md: le istruzioni del progetto
Un file `CLAUDE.md` nella cartella principale contiene le regole del progetto. Claude Code lo legge all'inizio di ogni sessione. È come il Project della chat, ma per una cartella.

```markdown
# Progetto: sito UX Boutique

## Cos'è
Sito vetrina e pagine servizi. Lingua italiana.

## Comandi
- Avvio: npm run dev
- Test: npm test

## Regole
- Tono dei testi: docs/tono-di-voce.md
- Colori e font solo da design/tokens.json
- Non modificare la cartella legacy/
- Mai password o chiavi nei file

## Come lavorare
- Prima di modifiche su più file, mostra il piano e aspetta.
- Dopo ogni modifica, elenca i file cambiati.
```

**Livelli.** Il file nella cartella del progetto vale per tutto il team. Esiste anche un file personale nella cartella dell'utente (`~/.claude/CLAUDE.md`). *(⚠ verifica i livelli nella documentazione)*

### 10.4 Plan mode e permessi
- **Plan mode**: Claude propone un piano e aspetta la tua approvazione prima di toccare i file. Si attiva con **Shift+Tab** o con il comando `/plan`. *(⚠ verifica nella versione installata)* Usalo per ogni modifica che tocca più file.
- **Permessi**: Claude Code chiede conferma prima di modificare file o eseguire comandi. Leggi sempre cosa chiede. Puoi concedere il permesso per una volta o per la sessione. Non concedere "approva tutto" senza sapere cosa farà.

### 10.5 Comandi utili
| Comando | Cosa fa |
|---|---|
| `/help` | Mostra i comandi disponibili |
| `/clear` | Ricomincia con una conversazione pulita |
| `/compact` | Riassume la conversazione per liberare spazio |
| `/plan` | Entra in plan mode |
| `/plugin` | Gestisce i plugin (cap. 12) |

*(⚠ l'elenco cambia tra versioni: usa `/help` per quello aggiornato)*

### 10.6 Subagent
Un **subagent** è un aiutante che Claude Code incarica di un sotto-compito, con istruzioni proprie. Ce ne sono di integrati, per esempio **Explore** (cerca nel codice) e **Plan** (prepara il piano in plan mode). Puoi crearne di tuoi per compiti ricorrenti, ad esempio un revisore di accessibilità. *(⚠ verifica la cartella dei subagent personalizzati nella documentazione)*

### 10.7 Skill, MCP e plugin in Claude Code
- **Skill**: cartelle in `.claude/skills/` nel progetto, o nella cartella personale (cap. 11).
- **MCP**: collegamento a strumenti esterni con `claude mcp add` (cap. 13).
- **Plugin**: pacchetti installati con `/plugin` (cap. 12).

### 10.8 Git in breve
| Parola | Significato |
|---|---|
| **Commit** | Una versione salvata, con una descrizione |
| **Branch** | Una linea di lavoro separata, che non tocca la versione principale |
| **Push** | Invio delle modifiche al repository online (GitHub) |
| **Pull request** | Richiesta di unire un branch al principale, con revisione |

### 10.9 Workflow per ruolo
- **Marketing**: contenuti in file `.md` → revisione per sezioni → generazione di pagine HTML o presentazioni (come questo corso).
- **Design**: prototipo da Claude Design → componenti con i token del design system → pagina di prova.
- **Sviluppo**: richiesta → plan mode → branch → test → commit → pull request → review.

### Errori da evitare
- Lavorare senza Git: non puoi tornare indietro.
- Approvare piani e permessi senza leggerli.
- `CLAUDE.md` lunghissimo e disordinato: le regole importanti si perdono.

### Prova tu
Crea una cartella con un file `testo.md`. Avvia Claude Code e chiedi in plan mode: "Trasforma testo.md in una pagina HTML semplice e leggibile." Leggi il piano prima di approvarlo.

---

## 11 · Skill: usarle e crearle

### In breve
Una **Skill** è un metodo scritto una volta, che Claude usa ogni volta che serve. È una cartella con un file `SKILL.md`: dentro ci sono il nome, una descrizione che dice **quando** usarla, e le istruzioni. Claude legge la descrizione e decide da solo quando attivarla.

### 11.1 Skill, prompt o Project?

| | Prompt | Project | Skill |
|---|---|---|---|
| **Cos'è** | Una richiesta | Un contesto fisso | Un metodo riutilizzabile |
| **Quando** | Una volta | Per un cliente o un tema | Per un compito che si ripete |
| **Dove vive** | Nella chat | Nello spazio del Project | In una cartella con `SKILL.md` |
| **Esempio** | "Scrivi questo post" | "Tutto su cliente Rossi" | "Come scriviamo i post per qualsiasi cliente" |

**Regola pratica.** Se fai lo stesso compito più di tre volte al mese, con lo stesso schema, è un buon candidato per una Skill.

### 11.2 Come funziona: caricamento a strati
Claude non legge tutte le Skill sempre. Funziona a strati:
1. **Sempre**: legge solo **nome e descrizione** di ogni Skill. Poche righe ciascuna.
2. **Quando serve**: se la descrizione corrisponde al compito, legge il **corpo** di `SKILL.md`.
3. **Solo se richiesto**: legge i **file aggiuntivi** (esempi, riferimenti, script) quando il corpo li indica.

Da qui due conseguenze:
- **La descrizione è la parte più importante**: è l'unica cosa che Claude vede per decidere.
- **`SKILL.md` deve essere snello**: i dettagli lunghi vanno in file separati.

### 11.3 Anatomia di una Skill

```
tono-ux-boutique/
├── SKILL.md            ← obbligatorio
├── esempi/             ← opzionale
│   ├── post-buono.md
│   └── post-da-evitare.md
└── riferimenti/        ← opzionale
    └── glossario.md
```

Regole:
- Il nome della cartella è uguale al campo `name`, in minuscolo con trattini.
- `SKILL.md` inizia con un'intestazione (frontmatter) con `name` e `description`.
- La descrizione non supera i 1024 caratteri. *(⚠ limite riportato da fonti di terze parti)*

### 11.4 Il file SKILL.md

```markdown
---
name: tono-ux-boutique
description: Scrive o revisiona testi per UX Boutique secondo il tono di
  voce del brand. Usala quando l'utente chiede post, claim, intro, email
  commerciali o revisione di testi per clienti o per il sito. Non usarla
  per documenti interni o codice.
---

# Tono di voce UX Boutique

## Procedura
1. Se mancano, chiedi pubblico, obiettivo e lunghezza.
2. Scrivi in italiano, tono diretto e concreto.
3. Ogni affermazione ha un beneficio misurabile, oppure va marcata
   "da verificare".
4. Applica il glossario in riferimenti/glossario.md.
5. Rileggi la bozza rispetto ai criteri qui sotto.

## Criteri di qualità
- Nessun superlativo vuoto ("il migliore", "rivoluzionario").
- Una sola call to action.
- Frasi sotto le 25 parole.
- Nessun cliente citato senza approvazione.

## Esempi
Prima di scrivere, leggi esempi/post-buono.md ed esempi/post-da-evitare.md.

## Formato di output
Testo finale, poi "Da verificare:" con le affermazioni da confermare.
```

### 11.5 Scrivere la descrizione giusta
Formula in tre frasi:
> **Cosa fa.** Usala quando **[situazioni, con le parole che userebbe chi chiede]**. Non usarla per **[casi esclusi]**.

| ❌ Debole | ✅ Efficace |
|---|---|
| "Aiuta con i testi." | "Scrive o revisiona post e pagine per clienti UX Boutique. Usala quando l'utente chiede testi commerciali. Non usarla per documenti interni." |
| "Strumento del reparto PM." | "Trasforma note di riunione in uno status report di 5 punti. Usala quando l'utente chiede un report, un aggiornamento per il cliente o un riassunto di avanzamento." |

### 11.6 Tre modi per creare una Skill

**1. Chiedendolo a Claude, in conversazione.** Il modo più semplice. Descrivi il processo e Claude scrive `SKILL.md` per te:
```
Voglio creare una Skill per i nostri status report settimanali.
Ecco come li facciamo oggi: [descrivi i passi].
Ecco due report riusciti: [incolla].
Scrivi la Skill completa: SKILL.md con nome, descrizione, procedura,
criteri di qualità ed esempi. Fammi prima le domande che ti servono.
```

**2. A mano, con il modello del 11.4.** Utile quando il metodo è già scritto da qualche parte.

**3. Da riga di comando.** Il comando `npx skills init nome-skill` crea la struttura di base da completare.

### 11.7 Esempio completo: Skill "status report"
1. **Raccogli** tre status report riusciti e le note grezze da cui sono nati.
2. **Chiedi a Claude** di scrivere la Skill (prompt del 11.6).
3. **Rispondi** alle sue domande: per chi è il report, cosa non deve mai mancare.
4. **Controlla** la descrizione: dice cosa fa e quando usarla?
5. **Testa** con tre casi (11.9).
6. **Installa** e condividi con il team (11.8).

### 11.8 Installare una Skill

**Su claude.ai (chat, Project)**
1. Comprimi la cartella in `.zip`: la cartella della Skill deve essere la radice dell'archivio.
2. Impostazioni → sezione **Skills** → carica lo zip. *(⚠ il percorso cambia: "Customize → Skills" oppure "Settings → Capabilities → Skills")*
3. Attivala e fai una prova.
4. Nel piano Team, per renderla disponibile a tutti serve l'admin. *(⚠ verifica)*

**In Claude Code**
- **Per un progetto**: cartella `.claude/skills/nome-skill/` nel repository, poi commit. Vale per chi lavora su quel repository.
- **Per te, in tutti i progetti**: cartella personale `~/.claude/skills/`.

**Da un pacchetto online**
```bash
npx skills add autore/repository                  # nel progetto
npx skills add autore/repository -g -a claude-code  # per tutti i tuoi progetti
```

**Sicurezza.** Una Skill scaricata può contenere istruzioni e script. Leggila prima di usarla, come abbiamo fatto con i pacchetti installati in questo repository.

### 11.9 Testare e correggere
Prepara tre casi:
1. **Tipico**: il compito per cui è nata. Deve attivarsi e rispettare i criteri.
2. **Al limite**: un compito simile. Deve adattarsi o chiedere.
3. **Fuori scopo**: un compito diverso. Non deve attivarsi.

| Sintomo | Causa | Correzione |
|---|---|---|
| Non si attiva | Descrizione vaga | Riscrivila con le parole dell'utente |
| Si attiva sempre | Descrizione troppo ampia | Aggiungi "Non usarla per…" |
| Si attiva ma sbaglia | Istruzioni ambigue | Aggiungi un passo o un esempio "da evitare" |
| Non compare | Nome del file o intestazione | Controlla `SKILL.md` e i campi `name` e `description` |
| Upload rifiutato | Zip con cartella annidata o nome non valido | Ricomprimi con la cartella come radice |

Per forzare una Skill durante i test: "Usa la Skill tono-ux-boutique per questo testo."

### 11.10 Manutenzione
- Tieni le Skill in un repository Git: ogni modifica ha una versione.
- Ogni Skill ha un responsabile.
- Quando il metodo cambia, aggiorna la Skill e ripeti i tre test.

### 11.11 Idee di Skill per ruolo
| Ruolo | Skill |
|---|---|
| Marketing | Tono di voce, piano editoriale, revisione copy, brief di campagna |
| PM | Status report, verbale riunione, stima di progetto, analisi rischi |
| Design | Sintesi interviste, analisi euristica, microcopy, handoff |
| Art direction | Brief creativo, concept, prompt per immagini |
| Sviluppo | Code review con le regole del team, documentazione, checklist di rilascio |

### Prova tu
Scegli un compito che ripeti. Crea la Skill chiedendolo a Claude (11.6, metodo 1), testala sui tre casi e portala al team.

---

## 12 · Plugin

### In breve
Un **plugin** è un **pacchetto** che installa insieme più pezzi: Skill, comandi, agenti, connettori, automazioni. Invece di configurare tutto a mano, installi un plugin e hai un kit pronto per un ambito (per esempio marketing o project management).

### 12.1 Differenze con gli altri mattoni

| | Skill | Connettore / MCP | Plugin |
|---|---|---|---|
| **Cos'è** | Un metodo | Un collegamento a uno strumento | Un pacchetto di più pezzi |
| **Cosa aggiunge** | Il "come si fa" | I dati e le azioni di uno strumento | Metodi + collegamenti + comandi insieme |
| **Esempio** | Skill "status report" | Connettore Google Drive | Plugin "Project Management" |

### 12.2 Due tipi di plugin
Attenzione: il nome è lo stesso, ma esistono in due posti diversi.

| | Plugin di Claude Code | Plugin di Cowork |
|---|---|---|
| **Dove** | Claude Code (terminale, desktop, web) | Scheda Cowork dell'app desktop |
| **Contengono** | Comandi slash, subagent, Skill, hook (automazioni), server MCP | Skill, connettori, subagent |
| **Per chi** | Sviluppo e chi lavora sui file con Claude Code | Chi lavora su documenti, anche senza programmare |
| **Ufficiali** | Marketplace `claude-plugins-official` | Plugin ufficiali Anthropic per marketing, PM, vendite, supporto e altro |

**⚠ Da verificare** la disponibilità dei plugin di Cowork per il vostro piano.

### 12.3 Installare un plugin in Claude Code
1. **Aggiungi un marketplace** (un catalogo di plugin):
```
/plugin marketplace add autore/repository
```
2. **Installa il plugin**:
```
/plugin install nome-plugin@nome-marketplace
```
3. **Gestisci** i plugin installati con `/plugin`.

Il marketplace ufficiale di Anthropic si chiama `claude-plugins-official`. *(⚠ verifica se è già attivo o va aggiunto)*

### 12.4 Com'è fatto un plugin (Claude Code)
```
plugin-ux-boutique/
├── .claude-plugin/
│   └── plugin.json      ← nome, descrizione, versione
├── commands/            ← comandi slash, es. /status-report
├── agents/              ← subagent
├── skills/              ← Skill
├── hooks/               ← automazioni su eventi
└── .mcp.json            ← server MCP
```
*(⚠ verifica i nomi esatti delle cartelle nella documentazione dei plugin)*

`plugin.json` minimo:
```json
{
  "name": "ux-boutique",
  "description": "Skill e comandi del team UX Boutique",
  "version": "1.0.0"
}
```

**Provare un plugin in locale:**
```bash
claude --plugin-dir ./plugin-ux-boutique
```

### 12.5 Un marketplace per il team
Un marketplace è un repository con un file `.claude-plugin/marketplace.json` che elenca i plugin. Con un marketplace del team, ogni persona installa gli stessi strumenti con due comandi, e gli aggiornamenti arrivano a tutti.

### 12.6 Plugin di Cowork
- Si installano dalla scheda Cowork dell'app desktop.
- Quelli ufficiali di Anthropic sono gratuiti e open source.
- Cowork aiuta anche a creare plugin personalizzati.

### 12.7 Sicurezza
- Un plugin può eseguire comandi e collegarsi a strumenti esterni. **Gli hook in particolare eseguono comandi automaticamente.**
- Installa solo plugin di fonti affidabili.
- Leggi cosa contiene prima di installarlo.
- Nel team, decidete chi può aggiungere plugin al marketplace interno.

### Prova tu
In Claude Code, apri `/plugin` e guarda i plugin disponibili nel marketplace ufficiale. Scegline uno utile al tuo ruolo e leggi cosa contiene prima di installarlo.

---

## 13 · Connettori e MCP

### In breve
I **connettori** collegano Claude ai vostri strumenti: Google Drive, Figma, Miro e altri. **MCP** è lo standard su cui si basano. Con un connettore, Claude può cercare un file, leggere una board, estrarre i token di un design system.

### Passo per passo
1. Impostazioni → **Connectors** → cerca lo strumento. *(⚠ verifica il nome della voce)*
2. **Connect** e accesso con il tuo account. Se vedi **Request**, serve l'abilitazione dell'admin. *(⚠ verifica)*
3. Controlla i permessi: solo lettura o anche scrittura.
4. Fai un test semplice: "Elenca i file a cui hai accesso."

### I nostri tre connettori
| Strumento | Cosa fa | Richiesta di esempio |
|---|---|---|
| **Google Drive** | Legge documenti, fogli, presentazioni, PDF | "Cerca la cartella del cliente X e riassumi l'ultimo brief." |
| **Figma** | Legge token e componenti; può scrivere sul canvas | "Dal file [link], estrai colori e font in JSON." |
| **Miro** | Legge board e note | "Nella board [nome], raggruppa le note per tema." |

Figma è disponibile su qualsiasi piano Figma. Con l'accesso a livello di team, Claude vede solo i team autorizzati. Per Miro, chiedi esplicitamente di usarlo in ogni conversazione.

### MCP in Claude Code
```bash
claude mcp add nome-server -- comando-del-server
claude mcp list
```
*(⚠ verifica la sintassi aggiornata)*

### Errori da evitare
- Dare più permessi del necessario.
- Richieste vaghe che trovano il file sbagliato.
- Scrivere su Figma direttamente sul file del team: usa una copia.

---

# Parte 5 · Lavorare bene

## 14 · Metodo: prima i file, poi l'artefatto

### In breve
Prepara i contenuti in file di testo (`.md`) e trasformali in artefatto, presentazione o pagina solo alla fine. Ogni modifica tocca solo la parte che serve, e la storia resta in Git.

### Perché
- Un artefatto si ripubblica per intero a ogni modifica.
- Un file si modifica per sezioni, si confronta con `git diff`, si recupera se serve.
- Nei documenti lunghi, lavorare per file è più economico anche in termini di token. Il vantaggio è pratico, non l'ho misurato.

### Passo per passo
1. Una cartella `contenuti/progetto/` con un file per sezione e un `indice.md`.
2. "Modifica solo `02-servizi.md`: riduci a tre punti."
3. `git diff` per vedere cosa è cambiato, un commit per sezione approvata.
4. Alla fine: "Crea la presentazione HTML a partire dai file in contenuti/progetto/."

Questo corso è stato costruito così.

---

## 15 · Qualità, privacy e checklist

### In breve
Ogni risultato di Claude è una bozza da verificare. Non caricare dati che non puoi condividere.

### Verificare
- **Fatti**: chi, cosa, quando. Apri la fonte.
- **Numeri**: ricalcola un campione.
- **Codice**: eseguilo e leggilo.
- **Citazioni**: controlla che esistano davvero.

### Non caricare mai
- Password, chiavi API, credenziali.
- Dati personali di clienti senza una base legale.
- Documenti coperti da NDA, se non lo consentono.

Quando lavori su casi reali, **anonimizza**. Verifica con l'admin le impostazioni privacy del piano Team.

### Checklist prima della consegna
- [ ] Fatti e numeri verificati sulla fonte
- [ ] Nessun dato sensibile o coperto da NDA
- [ ] Tono e brand rispettati
- [ ] Test su telefono e su browser diversi (per il digitale)
- [ ] Immagini e font con licenza utilizzabile
- [ ] Approvazione del referente

---

# Parte 6 · Pratica

## 16 · Percorso di esercizi

Otto esercizi in ordine di difficoltà. Ognuno richiede 15–30 minuti.

| # | Esercizio | Capitolo |
|---|---|---|
| 1 | Riscrivi un tuo prompt con il modello BRIEF e confronta i risultati | 4 |
| 2 | Crea il Project del tuo ruolo e testalo | 5 |
| 3 | Fai tre compiti del tuo ruolo con i prompt pronti | 6–8 |
| 4 | Crea una landing in Claude Design: tre strutture, tre revisioni, export | 9 |
| 5 | Con Claude Code, trasforma un file `.md` in pagina HTML in plan mode | 10 |
| 6 | Crea una Skill chiedendola a Claude e testala sui tre casi | 11 |
| 7 | Esplora `/plugin` e valuta un plugin per il tuo ruolo | 12 |
| 8 | Collega Drive o Miro e usa i dati in un report | 13 |

### Workshop finale a coppie miste
Coppie miste (design + sviluppo, marketing + PM). Ogni coppia sceglie un workflow (campagna, redesign, nuovo prodotto, automazione di un report, nuova funzione) e lo porta a termine:
1. BRIEF del lavoro.
2. Project e, se serve, una Skill.
3. Connettori necessari.
4. Output in Artifact, Claude Design o Claude Code.
5. Checklist del cap. 15.
6. Tre minuti di presentazione: cosa avete fatto, cosa avete verificato, cosa non avete fatto.

---

# Appendici

## A · Scelta rapida

| Voglio… | Strumento | Capitolo |
|---|---|---|
| Una risposta, un testo, un'analisi | Chat | 4 |
| Lavorare sempre con lo stesso contesto | Project | 5 |
| Un visual, un prototipo, una slide | Claude Design | 9 |
| Lavorare su file e cartelle senza programmare | Cowork | 2 |
| Codice, siti, file con versioni | Claude Code | 10 |
| Fare un compito sempre allo stesso modo | Skill | 11 |
| Installare un kit completo | Plugin | 12 |
| Usare i dati di Drive, Figma, Miro | Connettori | 13 |

## B · Glossario

| Termine | Significato semplice |
|---|---|
| **Agente** | Un Claude che esegue compiti in più passaggi, non solo risponde |
| **Artifact** | Un risultato modificabile accanto alla chat: documento, pagina, presentazione |
| **BRIEF** | Il metodo in sei parti per scrivere un buon prompt |
| **CLAUDE.md** | Il file con le regole di un progetto per Claude Code |
| **Connettore** | Il collegamento di Claude a uno strumento (Drive, Figma, Miro) |
| **Cowork** | La scheda dell'app desktop in cui Claude lavora sui file del computer |
| **Design system** | Colori, font e componenti di un brand, usati in modo coerente |
| **Hook** | Un'automazione che esegue un comando quando succede qualcosa |
| **Marketplace** | Un catalogo di plugin |
| **MCP** | Lo standard con cui gli strumenti si collegano a Claude |
| **Modello** | Il "cervello" di Claude: Haiku, Sonnet, Opus |
| **Plan mode** | Claude propone un piano prima di modificare i file |
| **Plugin** | Un pacchetto di Skill, comandi, agenti e connettori |
| **Project** | Uno spazio con istruzioni e documenti fissi |
| **Prompt** | La richiesta che scrivi a Claude |
| **Skill** | Un metodo riutilizzabile, in una cartella con `SKILL.md` |
| **Subagent** | Un aiutante a cui Claude Code affida un sotto-compito |
| **Token (design)** | Un valore di design condiviso: un colore, una spaziatura, un font |

## C · Da verificare prima del corso
1. Posizionamento del modello Fable nel selettore.
2. Disponibilità di Cowork e Claude Design nel piano Team, e punto di accesso.
3. Percorso di caricamento delle Skill su claude.ai e condivisione nel team.
4. Opzioni di export di Claude Design.
5. Abilitazione dei connettori Drive, Figma e Miro da parte dell'admin.
6. Plan mode, comandi slash e cartella dei subagent nella versione di Claude Code installata.
7. Struttura delle cartelle di un plugin e marketplace ufficiale.
8. Sintassi di `claude mcp add`.

## D · Fonti
**Documentazione ufficiale**
- Anthropic, *Introducing Claude Design by Anthropic Labs*: https://www.anthropic.com/news/claude-design-anthropic-labs
- Claude Help Center, guida admin di Claude Design: https://support.claude.com/en/articles/14604406-claude-design-admin-guide-for-team-and-enterprise-plans
- Claude Code, plugin: https://code.claude.com/docs/en/discover-plugins e https://code.claude.com/docs/en/plugin-marketplaces
- Claude Code, subagent: https://code.claude.com/docs/en/sub-agents
- Anthropic, *Customize Claude Code with plugins*: https://claude.com/blog/claude-code-plugins
- Skills, guida: https://claude.com/docs/skills/how-to
- Figma Help Center, connettore Claude: https://help.figma.com/hc/en-us/articles/37883260397975

**Fonti secondarie (da verificare)**
- Cowork e plugin di Cowork: guide di terze parti (es. buildfastwithai.com, digitalapplied.com).
- Opzioni di export di Claude Design: DataCamp (datacamp.com/blog/claude-design).
- Modelli della famiglia 5.5: guide comparative di terze parti.
- Limiti del frontmatter delle Skill: guide di terze parti.

---

### Note per la prossima versione
- Distribuzione dei capitoli sulle due giornate: da confermare. Proposta: giorno 1 capitoli 1–8, giorno 2 capitoli 9–16.
- Aggiornare i passaggi ⚠ dopo la verifica nel vostro account.
