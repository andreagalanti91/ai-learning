# Corso Claude
### Versione 4.0 · UX Boutique

> Un flusso di lavoro, un prompt fatto bene, un caso seguito dall'inizio alla fine, e tutti gli strumenti per lavorare con Claude ogni giorno.

---

## Indice

**A · Le basi**
1. Cosa imparerai
2. Il modello e il prodotto
3. I mattoni di Claude

**B · Il flusso di lavoro**
4. I quattro passi
5. Passo 1: Delega

**C · Il prompt fatto bene**
6. Il metodo BRIEF
7. Il test del collega e quattro accorgimenti
8. Le tecniche da conoscere
9. Ridurre le invenzioni

**D · Il caso completo**
10. Il caso: il lancio dell'audit
11. Il prompt e l'output
12. Valutare e iterare
13. La catena di prompt
14. Claude come esperto e come cliente
15. Rispondere del risultato

**E · Gli strumenti**
16. Ricerca web e ricerca approfondita
17. File, immagini e Artifact
18. Project e memoria
19. Skill
20. Connettori e plugin
21. Claude Design
22. Claude Code
23. Cowork

**F · Pratica**
24. Per ruolo
25. Esercizi
26. Da dove viene questo corso
27. Per continuare

---

# A · Le basi

## 1 · Cosa imparerai

1. **Scegliere lo strumento giusto** per ogni lavoro.
2. **Scrivere un prompt fatto bene**, che funziona al primo o al secondo tentativo.
3. **Valutare e migliorare** il risultato con un metodo, non a tentativi.
4. **Rendere un lavoro ripetibile** con Project e Skill.

---

## 2 · Il modello e il prodotto

"Claude" indica due cose diverse.

**Il modello è il cervello.**

| Modello | Quando usarlo |
|---|---|
| **Sonnet** | Quasi tutto: è la scelta di partenza |
| **Opus** | Lavori complessi e delicati, ragionamenti lunghi |
| **Haiku** | Compiti semplici e ripetitivi, quando conta la velocità |

**Il prodotto è il posto di lavoro.**

| Prodotto | A cosa serve | Esempio |
|---|---|---|
| **Chat** (web, desktop, mobile) | Testi, analisi, ricerca, documenti | Un post, un report, una sintesi |
| **Claude Design** | Visual coerenti con il brand | Una landing, delle slide |
| **Claude Code** | Lavoro su file, codice e siti | Una pagina web, un componente |
| **Cowork** (app desktop) | Compiti in più passaggi sui file del computer | Riordinare cartelle, documenti da tanti file |

---

## 3 · I mattoni di Claude

| Mattone | Cos'è | A cosa serve |
|---|---|---|
| **Project** | Uno spazio con istruzioni e documenti fissi | Non ripetere il contesto |
| **Artifact** | Un risultato modificabile accanto alla chat | Consegnare documenti, pagine, tabelle |
| **Skill** | Un metodo scritto una volta | Fare un compito sempre allo stesso modo |
| **Connettore** | Il collegamento a Drive, Figma, Miro… | Usare i dati dei vostri strumenti |
| **Plugin** | Un pacchetto di Skill, comandi e connettori | Installare un kit completo |

**Esempio.** Il connettore Drive legge le note di una riunione, la Skill "status report" le trasforma nel formato del team, dentro il Project del cliente, e il risultato esce come Artifact.

---

# B · Il flusso di lavoro

## 4 · I quattro passi

Ogni lavoro con Claude segue quattro passi, presi dal modello **4D** del corso *AI Fluency* di Anthropic Academy.

| Passo | Domanda | In pratica |
|---|---|---|
| **1 · Delega** | Cosa faccio fare a Claude, e cosa tengo io? | Dividi il lavoro prima di iniziare |
| **2 · Descrivi** | Come glielo chiedo? | Un prompt fatto bene, con il BRIEF |
| **3 · Valuta** | Il risultato è buono? | Controlla, dai feedback, migliora |
| **4 · Rispondi** | Posso usarlo e consegnarlo? | Verifica, privacy, trasparenza |

I passi 2 e 3 formano un ciclo: descrivi, valuti, correggi, finché il risultato è giusto.

---

## 5 · Passo 1: Delega

| Dai a Claude | Tieni tu |
|---|---|
| Prime bozze e varianti | La decisione finale |
| Riassunti e sintesi | Il rapporto con il cliente |
| Strutture e scalette | I dati riservati |
| Ricerche da verificare | La verifica di fatti e numeri |
| Controlli di coerenza | Il giudizio sulla qualità |

**Tre domande prima di delegare.**
1. **So descrivere il risultato?** Se no, chiarisci prima tu cosa vuoi.
2. **So verificarlo?** Se non puoi controllare il risultato, non delegarlo.
3. **Cosa succede se sbaglia?** Più alto il rischio, più stretta la verifica.

---

# C · Il prompt fatto bene

## 6 · Il metodo BRIEF

| Lettera | Parte | Domanda | Esempio |
|---|---|---|---|
| **B** | Background | Qual è il contesto? | "Agenzia UX, lanciamo un audit per e-commerce." |
| **R** | Ruolo | Chi deve rispondere? | "Sei un copywriter senior B2B." |
| **I** | Intento | Cosa deve succedere dopo? | "Il lettore prenota la call gratuita." |
| **E** | Esempi | Come deve essere il risultato? | Un testo con il tono giusto e uno da evitare |
| **F** | Formato | Lunghezza, struttura, cosa evitare | "120 parole, niente emoji, nessun numero inventato." |
| **+** | Verifica | Come controllo il risultato? | "Elenca le affermazioni da verificare." |

Il BRIEF corrisponde al metodo **TCREI** del corso *Google Prompting Essentials*: Task = Intento e Formato, Context = Background e Ruolo, References = Esempi, Evaluate e Iterate = Verifica e passo 3.

---

## 7 · Il test del collega e quattro accorgimenti

**Il test del collega.** È la regola d'oro della guida di Anthropic: fai leggere il prompt a un collega che non sa niente del lavoro. Se lui sarebbe confuso, lo sarà anche Claude.

**Quattro accorgimenti.**
1. **Separa le parti con i tag.** Istruzioni, esempi e materiali in blocchi distinti: `<contesto>`, `<esempi>`, `<materiali>`. Il nome è libero, purché chiaro e sempre uguale.
2. **Dai esempi.** Da 3 a 5 quando il formato è difficile da spiegare, dentro `<esempi>`.
3. **Fallo ragionare.** Sui problemi complessi attiva il ragionamento esteso o chiedi di pensare per passi prima di rispondere.
4. **Chiedi le domande prima.** Per i lavori importanti: "Prima di iniziare, fammi le domande che ti servono."

---

## 8 · Le tecniche da conoscere

| Tecnica | Cos'è | Esempio |
|---|---|---|
| **Zero-shot** | Nessun esempio: solo l'istruzione | "Riassumi questo verbale in 5 punti." |
| **Few-shot** | Alcuni esempi del risultato voluto | Tre titoli approvati, poi "scrivine altri dieci così" |
| **Ruolo** | Chi deve rispondere | "Sei un UX researcher senior." |
| **Formato strutturato** | Tabella, elenco, JSON | "Rispondi con una tabella: Problema, Gravità, Proposta." |
| **Passo per passo** | Ragionare prima di rispondere | "Prima analizza, poi proponi, poi scegli." |
| **Catena di prompt** | Un compito diviso in passaggi | Ricerca → messaggi chiave → testo → revisione (cap. 13) |
| **Meta-prompting** | Far migliorare il prompt a Claude | "Migliora questo prompt e spiegami cosa hai cambiato." (cap. 14) |
| **Gioco di ruolo** | Claude simula un esperto o un cliente | "Sei un cliente scettico: critica questa landing." (cap. 14) |

---

## 9 · Ridurre le invenzioni

Claude a volte inventa una risposta plausibile invece di dire "non lo so". Il tutorial di Anthropic indica due tecniche:

1. **Dagli il permesso di non sapere.**
```
Se un'informazione non è nei materiali, scrivi "non lo so". Non inventare.
```
2. **Prima le citazioni, poi la risposta.** Con documenti lunghi:
```
Dal documento allegato, copia le frasi esatte che parlano dei tempi di
consegna. Poi rispondi alla domanda usando solo quelle frasi.
```

In più: dagli i documenti veri invece di chiedergli di ricordare, e chiedi sempre le fonti quando usa la ricerca web.

---

# D · Il caso completo

## 10 · Il caso: il lancio dell'audit

> **UX Boutique lancia un nuovo servizio: l'audit di usabilità per e-commerce.**
> Servono un post per LinkedIn, una landing page e un modo per rifare tutto la prossima volta.

**Delega.**
- **A Claude:** ricerca sui competitor, messaggi chiave, bozza del post, struttura della landing.
- **A noi:** prezzo, dati del caso studio, approvazione finale.

---

## 11 · Il prompt e l'output

```
<contesto>
UX Boutique è un'agenzia di UX design. Lanciamo un audit di usabilità
per e-commerce di medie dimensioni: in 30 minuti individuiamo i tre
punti in cui il sito perde clienti. La prima call è gratuita.
Pubblico: responsabili marketing, non designer.
</contesto>

<ruolo>Copywriter senior B2B. Tono sobrio e concreto.</ruolo>

<obiettivo>Un post LinkedIn che porti a prenotare la call.</obiettivo>

<esempi>
Sì: "Il checkout perde utenti? Spesso il problema è in tre passaggi."
No: "Rivoluziona il tuo e-commerce con il nostro audit innovativo!"
</esempi>

<formato>
Massimo 120 parole, due hashtag, nessuna emoji. Apri con un problema,
chiudi con l'invito. Nessun numero inventato: usa [X%].
</formato>

<verifica>Elenca le affermazioni che un cliente potrebbe contestare.</verifica>
```

**Perché funziona.** Ogni parte risponde a una domanda che Claude altrimenti dovrebbe indovinare. I tag separano istruzioni ed esempi. Il formato dice anche cosa non fare. La verifica trova i punti deboli prima del cliente.

**Lo stesso compito scritto male:** "Scrivimi un post per il nostro nuovo servizio di audit." Claude deve indovinare pubblico, tono, lunghezza e obiettivo: il risultato è generico.

**Un output di esempio** (illustrativo):
> Il tuo e-commerce riceve visite ma le vendite non crescono?
> Spesso il problema non è il traffico: sono tre passaggi del percorso d'acquisto in cui le persone si fermano.
> Con l'audit di usabilità di UX Boutique li troviamo in 30 minuti, partendo dal tuo sito reale. La prima call è gratuita.
> Prenota la tua call: [link]
> #UXdesign #ecommerce
>
> **Da verificare:** "tre passaggi" è una media dei nostri audit? "30 minuti" vale per ogni dimensione di sito?

---

## 12 · Valutare e iterare

**Valuta su tre piani** (modello 4D):
- **Il prodotto:** è corretto, chiaro, nel tono giusto?
- **Il processo:** il ragionamento regge? Le affermazioni sono sostenibili?
- **Il comportamento:** ha seguito le istruzioni, compresi i divieti?

**Dai feedback con la formula cosa + perché + come:**
```
L'apertura è troppo generica per chi gestisce un e-commerce.
Riscrivila partendo da un problema concreto del checkout, in una frase.
Non cambiare il resto.
```

**Se non migliora: quattro modi per iterare** (dal corso Google):
1. **Rivedi il BRIEF:** quasi sempre manca una parte.
2. **Dividi in frasi o passaggi più brevi:** prima tre aperture, poi il post con quella scelta.
3. **Riformula o cambia approccio:** "Scrivilo come lo spiegheresti a un collega a pranzo."
4. **Aggiungi vincoli:** "Usa solo parole che userebbe un responsabile marketing, niente gergo UX."

---

## 13 · La catena di prompt

Un lavoro grande funziona meglio diviso in passaggi, ognuno con il suo prompt. L'output di uno è il materiale del successivo.

| # | Prompt | Output |
|---|---|---|
| 1 | "Cerca i servizi di audit UX offerti in Italia. Per ognuno: promessa, prezzo visibile, pubblico. Indica le fonti." (ricerca web) | Tabella dei competitor |
| 2 | "Da questa tabella, proponi tre messaggi chiave che ci distinguono." | Tre messaggi |
| 3 | Il prompt del cap. 11, con il messaggio scelto nel contesto | Il post |
| 4 | "Rileggi il post come un responsabile marketing scettico. Cosa non ti convince?" | Critiche da risolvere |

Vantaggi: puoi controllare ogni passaggio, e se un passaggio sbaglia lo rifai senza ripartire da zero.

---

## 14 · Claude come esperto e come cliente

**Meta-prompting: fai migliorare il prompt a Claude.**
```
Ecco il prompt che uso per i post di lancio: <prompt>…</prompt>
Miglioralo seguendo il metodo BRIEF. Poi spiegami cosa hai cambiato e perché.
```

**Gioco di ruolo: Claude come esperto.**
```
Sei un consulente CRO con dieci anni di esperienza sugli e-commerce.
Valuta la struttura di questa landing e indica i tre rischi principali
per la conversione.
```

**Gioco di ruolo: Claude come cliente.**
```
Sei il responsabile marketing di un e-commerce di arredamento, scettico
verso le agenzie. Leggi questo post e dimmi perché non prenoteresti la call.
```

Il gioco di ruolo non sostituisce il parere di clienti veri: serve a trovare le obiezioni prima di loro.

---

## 15 · Rispondere del risultato

Prima di pubblicare:
- [ ] Ogni numero e affermazione verificati sulla fonte
- [ ] Nessun dato riservato del cliente nel testo
- [ ] Tono e brand rispettati
- [ ] Approvazione del referente
- [ ] Uso dell'AI dichiarato, se il cliente o il contesto lo richiedono

Non caricare mai password, chiavi, dati personali senza base legale o documenti coperti da NDA. Sui casi reali, anonimizza.

---

# E · Gli strumenti

## 16 · Ricerca web e ricerca approfondita

- **Ricerca web:** per informazioni recenti. Claude cerca, legge e cita le fonti.
- **Ricerca approfondita:** per temi ampi. Fa molte ricerche in sequenza e produce un rapporto con fonti. Richiede più tempo.

**Prompt di esempio:**
```
Fai una ricerca sui tempi di caricamento medi degli e-commerce italiani
nel 2026. Per ogni dato: valore, fonte, data. Separa i dati ufficiali
dalle stime. Segnala se le fonti non sono d'accordo.
```

**Regola.** Apri sempre le fonti delle affermazioni che userai. Una fonte citata non è una fonte verificata.

---

## 17 · File, immagini e Artifact

**Cosa puoi caricare:** PDF, Word, Excel e CSV, immagini e screenshot.

| File | Esempio di richiesta |
|---|---|
| PDF | "Estrai le date di scadenza e le penali da questo contratto." |
| Excel / CSV | "Calcola il costo per lead per canale e segnala i valori anomali." |
| Screenshot | "Valuta questa schermata con le 10 euristiche di Nielsen." |
| Foto di una lavagna | "Trascrivi le note e raggruppale per tema." |

**Artifact.** Quando il risultato è un documento, una tabella, una pagina o un grafico, chiedilo come Artifact: si apre accanto alla chat e si modifica per parti ("Nella sezione Metodo, riduci a tre punti").

**Verifica.** Ricalcola a mano un numero su dieci. Con immagini sfocate o PDF scansionati, il risultato peggiora.

---

## 18 · Project e memoria

**Project.** Uno spazio con istruzioni e documenti che valgono per tutte le chat al suo interno.
1. Barra laterale → **Projects** → nuovo Project. *(⚠ verifica il nome della voce)*
2. Nome chiaro: "UX Boutique — Brand & Tone".
3. Istruzioni in 5–10 righe: chi siamo, tono, cosa non fare mai.
4. Documenti aggiornati: guida al tono, testi approvati, glossario.
5. Chat sempre **dentro** il Project.

**Istruzioni di esempio:**
```
Lavoriamo per UX Boutique. Lingua italiana, tono diretto e concreto.
Ogni testo per clienti indica un beneficio misurabile.
Mai citare clienti senza approvazione. Se non sei sicuro, dichiaralo.
```

**Memoria.** Claude può ritrovare informazioni da chat precedenti. Controlla sempre che siano ancora valide.

**Chat lunghe.** Quando cambi argomento: "Riassumi questa chat in decisioni prese, file usati e cose da fare", poi apri una chat nuova con quel riassunto.

---

## 19 · Skill

**Cos'è.** Una cartella con un file `SKILL.md`: un metodo scritto una volta, che Claude usa da solo quando il compito corrisponde.

**Come funziona: tre livelli.**
1. **Sempre:** Claude legge solo nome e descrizione di ogni Skill.
2. **Quando serve:** se la descrizione corrisponde, legge il corpo di `SKILL.md`.
3. **Se richiesto:** legge i file aggiuntivi (esempi, riferimenti).

Per questo **la descrizione è la parte più importante**: deve dire cosa fa e quando usarla.

```markdown
---
name: post-linkedin-ux-boutique
description: Scrive post LinkedIn per i servizi di UX Boutique, con il
  tono del brand. Usala quando l'utente chiede un post, un annuncio o un
  lancio per LinkedIn. Non usarla per testi interni.
---
## Procedura
1. Se mancano, chiedi servizio, pubblico e obiettivo.
2. Apri con un problema, chiudi con un invito all'azione.
3. Massimo 120 parole, due hashtag, nessuna emoji.
4. Nessun numero inventato: usa segnaposto come [X%].
## Esempi
Sì: "Il checkout perde utenti? Spesso il problema è in tre passaggi."
No: "Rivoluziona il tuo e-commerce!"
## Verifica
Elenca le affermazioni da controllare.
```

**Crea.** Il modo più semplice è chiederlo a Claude: "Trasforma il prompt di questa chat in una Skill. Fammi prima le domande che ti servono."

**Installa.**
- **claude.ai:** cartella in `.zip` (la cartella è la radice), impostazioni → Skills. *(⚠ il percorso del menu cambia)*
- **Claude Code:** cartella in `.claude/skills/` nel progetto, o in `~/.claude/skills/` per tutti i progetti.

**Testa con tre casi.** Tipico (si attiva), al limite (si adatta o chiede), fuori scopo (non si attiva). Se non si attiva, riscrivi la descrizione con le parole di chi chiede; se si attiva quando non deve, aggiungi "Non usarla per…".

---

## 20 · Connettori e plugin

**Connettori.** Collegano Claude ai vostri strumenti.

| Strumento | Esempio |
|---|---|
| Google Drive | "Riassumi l'ultimo brief nella cartella del cliente X." |
| Figma | "Estrai colori e font dal file [link]." |
| Miro | "Raggruppa per tema le note della board del workshop." |

Si attivano in impostazioni → Connectors. Nel piano Team l'admin li abilita, poi ognuno collega il proprio account. *(⚠ verifica)* Concedi solo i permessi necessari.

**Plugin.** Un pacchetto che installa insieme Skill, comandi e connettori.
- In **Claude Code**: `/plugin` per cercarli e installarli.
- Nell'**app desktop** (Cowork): plugin ufficiali per marketing, project management e altro. *(⚠ verifica la disponibilità nel piano)*

**Sicurezza.** Plugin e Skill scaricati possono eseguire istruzioni e comandi: installa solo da fonti affidabili e leggi cosa contengono.

---

## 21 · Claude Design

**A cosa serve.** Prototipi, slide, one-pager e landing coerenti con il brand, creati parlando. Anteprima di ricerca di Anthropic Labs, per i piani Pro, Max, Team ed Enterprise. *(⚠ verifica l'accesso)*

**Una volta sola: il design system.** Un designer carica i materiali del brand (siti, presentazioni, file di design). Claude estrae colori, tipografia e componenti. Il designer controlla e pubblica: da quel momento tutti i progetti del team lo usano in automatico.

**Ogni volta: quattro passi.**
1. **Brief** con il BRIEF.
2. **Tre strutture**, senza stile. Ne scegli una.
3. **Revisioni singole**, una per messaggio, con il perché.
4. **Export:** PDF, PPTX, HTML, Canva, o passaggio a Claude Code. *(⚠ verifica le opzioni)*

```
Crea la landing per il nostro audit di usabilità.
Pubblico: responsabili marketing di e-commerce medi.
Obiettivo: prenotare la call gratuita di 30 minuti.
Sezioni: promessa e invito; tre benefici; un caso studio;
come funziona in tre passi; domande frequenti.
Vincoli: mobile first, un solo pulsante d'azione, nessun numero
inventato. Prima proponi tre strutture, senza stile.
```

---

## 22 · Claude Code

**A cosa serve.** Un agente che lavora dentro una cartella: legge e modifica file, esegue comandi. Utile a chiunque lavori con file, non solo a chi programma. Si usa da terminale, app desktop, web o editor.

**Il ciclo consigliato da Anthropic.**
1. **Esplora:** legge i file e capisce il problema, senza modificare.
2. **Pianifica:** propone un piano in plan mode (Shift+Tab). Tu lo approvi. *(⚠ verifica la scorciatoia)*
3. **Implementa e verifica:** modifica e controlla, per esempio con i test.
4. **Commit:** salva le modifiche con una descrizione chiara.

Tra un compito e l'altro usa `/clear`: lo spazio di contesto si riempie in fretta.

**CLAUDE.md** contiene le regole del progetto e viene letto a ogni sessione. **I permessi** vanno sempre letti prima di confermare.

```
Trasforma il prototipo di Claude Design nella pagina servizi/audit.html.
Usa solo i colori e i font di design/tokens.json.
Mostrami il piano prima di modificare.
```

**Metodo: prima i file.** Prepara i contenuti in file `.md` e trasformali in pagina o presentazione solo alla fine. Questo corso è fatto così.

---

## 23 · Cowork

**A cosa serve.** Una modalità dell'app desktop in cui Claude esegue compiti in più passaggi sui file del tuo computer, senza bisogno di programmare. *(⚠ verifica la disponibilità nel piano)*

**Quando sceglierlo.**
- Riordinare e rinominare file in una cartella.
- Produrre un documento partendo da molti file.
- Compiti lunghi da lasciare in esecuzione.

**Chat, Cowork o Claude Code?** Chat per domande e testi. Cowork per lavori su documenti e cartelle. Claude Code per codice, siti e file con versioni.

---

# F · Pratica

## 24 · Per ruolo

| Marketing | Design | Sviluppo |
|---|---|---|
| Piani editoriali e post con Project e Skill | Sintesi di interviste e personas | Capire un progetto nuovo |
| Ricerca competitor con fonti | Analisi euristica da screenshot | Bug corretti partendo da un test |
| Varianti di titoli con few-shot | Microcopy e messaggi di errore | Code review con le regole del team |
| Report da CSV o Excel | Prototipi in Claude Design | Componenti dai token del design system |

---

## 25 · Esercizi

1. **Il prompt.** Riscrivi un tuo prompt reale con il BRIEF. Fai il test del collega. Confronta i risultati.
2. **Il ciclo.** Valuta il risultato su prodotto, processo e comportamento. Fai due iterazioni.
3. **La catena.** Dividi un tuo lavoro in tre o quattro prompt collegati.
4. **Il metodo.** Trasforma il prompt riuscito in una Skill e testala con tre casi.

**Workshop finale a coppie miste.** Rifate il caso su un servizio vostro: delega, catena di prompt, valutazione, verifica, Skill. Tre minuti per presentarlo.

---

## 26 · Da dove viene questo corso

| Fonte | Cosa abbiamo preso |
|---|---|
| **AI Fluency** (Anthropic Academy) | Il flusso in 4 passi, la valutazione su tre piani, la trasparenza |
| **Claude 101** (Anthropic Academy) | Project, Artifact, Skill, connettori, ricerca, casi d'uso per ruolo |
| **Guida ai prompt di Anthropic** | Test del collega, tag, esempi, ragionamento |
| **Tutorial interattivo di Anthropic** | Ruolo, formato, catene, ridurre le invenzioni |
| **Buone pratiche di Claude Code** | Esplora, pianifica, implementa, commit |
| **Google Prompting Essentials** | TCREI, quattro modi di iterare, catene, meta-prompting, gioco di ruolo |
| **Claude 101 (DataCamp)** | Scegliere la modalità giusta, ricerca e connettori |
| **Corso Coursera sui fondamenti di Claude** | Zero-shot e few-shot, formati strutturati |

Corsi in italiano: abbiamo trovato solo corsi commerciali di taglio diverso, nessun programma ufficiale.

---

## 27 · Per continuare

Corsi gratuiti di Anthropic Academy (in inglese, con certificato):

| Corso | Per chi |
|---|---|
| **Claude 101** e **AI Fluency** | Tutti |
| **Claude Code 101** e **Claude Code in Action** | Chi lavora con file e codice |
| **Introduction to agent skills** e **Introduction to subagents** | Chi crea Skill e automazioni |

Per il prompt: il **tutorial interattivo** di Anthropic su GitHub e **Google Prompting Essentials** su Coursera. *(⚠ alcune fonti riportano che Anthropic Academy è stata rinominata Claude Academy)*

---

## Prima del corso: da verificare
1. Voci Projects, Skills e Connectors nel vostro account.
2. Accesso a Claude Design nel piano Team e opzioni di export.
3. Disponibilità di Cowork e dei plugin nel piano Team.
4. Connettori Drive, Figma e Miro abilitati dall'admin.
5. Scorciatoia del plan mode in Claude Code.

## Fonti
- Anthropic Academy, *AI Fluency*: https://anthropic.skilljar.com · framework 4D: https://www-cdn.anthropic.com/b383cf6baddbfc72fdf8b0ed533a518e2872d531.pdf
- Anthropic Academy, *Claude 101*: https://anthropic.skilljar.com/claude-101
- Anthropic, *Prompting best practices*: https://platform.claude.com/en/docs/build-with-claude/prompt-engineering/claude-prompting-best-practices
- Anthropic, *Use XML tags*: https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/use-xml-tags
- Anthropic, *Prompt Engineering Interactive Tutorial*: https://github.com/anthropics/prompt-eng-interactive-tutorial
- Claude Code, *Best practices*: https://code.claude.com/docs/en/best-practices
- Google, *Prompting Essentials*: https://grow.google/prompting-essentials
- DataCamp, *Claude 101*: https://www.datacamp.com/courses/claude-101
- Coursera, *Claude AI Foundations and Prompt Engineering*: https://www.coursera.org/learn/claude-fundamentals-prompt-engineering
- Anthropic, *Introducing Claude Design*: https://www.anthropic.com/news/claude-design-anthropic-labs
- Claude Help Center, guida admin di Claude Design: https://support.claude.com/en/articles/14604406-claude-design-admin-guide-for-team-and-enterprise-plans
- Claude Code, plugin: https://code.claude.com/docs/en/discover-plugins
- Skills: https://claude.com/docs/skills/how-to
