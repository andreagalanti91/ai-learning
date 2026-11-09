# Claude per il lavoro
### Corso · versione 3.0 · UX Boutique

> Un flusso di lavoro, un prompt fatto bene, un caso seguito dall'inizio alla fine.
> Il resto si impara facendo.

---

## Cosa imparerai

1. **Scegliere lo strumento giusto** tra chat, Claude Design e Claude Code.
2. **Scrivere un prompt fatto bene**, che funziona al primo o al secondo tentativo.
3. **Trasformare un lavoro riuscito in un metodo ripetibile**, con Project e Skill.

Il corso unisce cinque fonti:
- il modello **4D** del corso *AI Fluency* di Anthropic Academy (Delega, Descrizione, Discernimento, Diligenza);
- le **indicazioni ufficiali di Anthropic** per scrivere prompt;
- il **tutorial interattivo di prompt engineering** di Anthropic, per ridurre le invenzioni;
- le **buone pratiche ufficiali di Claude Code**;
- il metodo **TCREI** del corso *Google Prompting Essentials* (Task, Context, References, Evaluate, Iterate).

Le abbiamo tradotte in un flusso unico, con il nostro metodo **BRIEF** per il prompt.

---

## 1 · Claude: il modello e il prodotto

"Claude" indica due cose.

**Il modello** è il cervello. Parti da **Sonnet**, che va bene per quasi tutto. Passa a **Opus** per i lavori complessi, a **Haiku** per quelli semplici e ripetitivi.

**Il prodotto** è il posto in cui lavori:

| Prodotto | A cosa serve | Esempio |
|---|---|---|
| **Chat** (web, desktop, mobile) | Testi, analisi, documenti. Con Project e Skill | Un post, un riassunto, un report |
| **Claude Design** | Visual coerenti con il brand | Una landing, una presentazione, un one-pager |
| **Claude Code** | Lavoro su file e cartelle, codice e siti | Una pagina HTML, un componente, un sito |

Esistono anche **Cowork** (Claude che lavora sui file del computer, dall'app desktop) e le **API** (Claude dentro i vostri prodotti). In questo corso non servono.

---

## 2 · Il flusso di lavoro in quattro passi

Ogni lavoro con Claude segue quattro passi. Vengono dal modello 4D di Anthropic.

| Passo | Domanda | In pratica |
|---|---|---|
| **1 · Delega** | Cosa faccio fare a Claude, e cosa tengo io? | Dividi il lavoro prima di iniziare |
| **2 · Descrivi** | Come glielo chiedo? | Un prompt fatto bene, con il BRIEF |
| **3 · Valuta** | Il risultato è buono? | Controlla, dai feedback, migliora |
| **4 · Rispondi** | Posso usarlo e consegnarlo? | Verifica, privacy, trasparenza |

I passi 2 e 3 sono un ciclo: descrivi, valuti, correggi, finché il risultato è giusto.

---

## 3 · Passo 1: Delega

Prima di scrivere il prompt, decidi chi fa cosa.

| Dai a Claude | Tieni tu |
|---|---|
| Prime bozze e varianti | La decisione finale |
| Riassunti e sintesi | Il rapporto con il cliente |
| Strutture e scalette | I dati riservati |
| Controlli di coerenza | La verifica di fatti e numeri |

**Regola.** Claude accelera il lavoro, la responsabilità resta tua.

---

## 4 · Passo 2: Descrivi, con il metodo BRIEF

Un prompt funziona quando contiene tutto quello che un collega bravo ti chiederebbe prima di iniziare.

| Lettera | Parte | Domanda |
|---|---|---|
| **B** | Background | Qual è il contesto? |
| **R** | Ruolo | Chi deve rispondere? |
| **I** | Intento | Cosa deve succedere dopo? |
| **E** | Esempi | Come deve essere il risultato? |
| **F** | Formato | Lunghezza, struttura, cosa evitare |
| **+** | Verifica | Come controllo il risultato? |

Il BRIEF corrisponde al metodo TCREI di Google: Task = Intento e Formato, Context = Background e Ruolo, References = Esempi, Evaluate e Iterate = Verifica e passo 3.

**Il test del collega.** È la regola d'oro di Anthropic: fai leggere il prompt a un collega che non sa niente del lavoro. Se lui sarebbe confuso, lo sarà anche Claude.

**Quattro accorgimenti dalle guide ufficiali di Anthropic.**
- **Separa le parti con i tag.** Istruzioni, esempi e materiali vanno in blocchi distinti, per esempio `<istruzioni>`, `<esempi>`, `<materiali>`. Il nome del tag è libero, purché sia chiaro e sempre uguale.
- **Dai 3–5 esempi** quando il formato è difficile da spiegare. Mettili dentro `<esempi>`.
- **Lascia ragionare Claude** sui problemi complessi: attiva il ragionamento esteso o chiedigli di pensare per passi prima di rispondere.
- **Riduci le invenzioni.** Dagli il permesso di dire "non lo so": *"Se un'informazione non è nei materiali, scrivi che non lo sai."* Con documenti lunghi, chiedi prima le citazioni esatte e poi la risposta basata solo su quelle.

---

## 5 · Il caso: dal brief al lancio

Seguiamo un caso reale dall'inizio alla fine.

> **UX Boutique lancia un nuovo servizio: l'audit di usabilità per e-commerce.**
> Serve un post per LinkedIn, una landing page e un modo per rifare tutto la prossima volta.

### Passo 1 · Delega
- **A Claude:** prima bozza del post, varianti di titolo, struttura della landing.
- **A noi:** prezzo, dati del caso studio, approvazione finale.

### Passo 2 · Descrivi: il prompt fatto bene

```
<contesto>
UX Boutique è un'agenzia di UX design. Lanciamo un audit di usabilità
per e-commerce di medie dimensioni: in 30 minuti individuiamo i tre
punti in cui il sito perde clienti. La prima call è gratuita.
Pubblico: responsabili marketing, non designer.
</contesto>

<ruolo>
Sei un copywriter senior B2B. Tono sobrio e concreto, niente superlativi.
</ruolo>

<obiettivo>
Un post LinkedIn che porti a prenotare la call gratuita.
</obiettivo>

<esempi>
Tono da seguire: "Il checkout perde utenti? Spesso il problema è in tre passaggi."
Tono da evitare: "Rivoluziona il tuo e-commerce con il nostro audit innovativo!"
</esempi>

<formato>
- Massimo 120 parole, due hashtag, nessuna emoji.
- Apri con un problema riconoscibile, chiudi con l'invito a prenotare.
- Non inventare numeri: dove servono, usa segnaposto come [X%].
</formato>

<verifica>
Dopo il post, elenca le affermazioni che un cliente potrebbe contestare.
</verifica>
```

**Perché funziona.** Ogni parte risponde a una domanda che Claude altrimenti dovrebbe indovinare. I tag separano le istruzioni dagli esempi. Il formato dice anche cosa non fare. La verifica fa emergere i punti deboli prima che li trovi il cliente.

**Lo stesso compito, scritto male:** "Scrivimi un post per il nostro nuovo servizio di audit." Claude deve indovinare pubblico, tono, lunghezza e obiettivo. Il risultato è un post generico.

### Passo 3 · Valuta e migliora
Controlla il risultato su tre piani (dal modello 4D):
- **Il prodotto:** il post è corretto, chiaro, nel tono giusto?
- **Il processo:** il ragionamento regge? Le affermazioni sono sostenibili?
- **Il comportamento:** Claude ha seguito le istruzioni, compresi i divieti?

Poi dai feedback con la formula **cosa + perché + come**:
```
L'apertura (cosa) è troppo generica per chi gestisce un e-commerce (perché).
Riscrivila partendo da un problema concreto del checkout, in una frase.
Non cambiare il resto (come).
```

Se il risultato non migliora, usa uno dei tre modi per iterare del corso Google:
1. **Rivedi il BRIEF:** quasi sempre manca una parte.
2. **Dividi il compito:** prima tre aperture, poi il post con quella scelta.
3. **Riformula:** chiedi la stessa cosa in un altro modo, per esempio "scrivi il post come lo spiegheresti a un collega a pranzo".

### Passo 4 · Rispondi
Prima di pubblicare:
- [ ] Ogni numero e affermazione verificati sulla fonte
- [ ] Nessun dato riservato del cliente nel testo
- [ ] Tono e brand rispettati
- [ ] Approvazione del referente
- [ ] Uso dell'AI dichiarato, se il cliente o il contesto lo richiedono

### Dal post alla landing
Con lo stesso contesto si passa al visual (cap. 7): stesso brief in **Claude Design**, tre strutture di landing, revisioni singole, export. Per mettere la pagina online, il prototipo passa a **Claude Code** (cap. 8).

---

## 6 · Dal prompt al metodo: Project e Skill

Un prompt riuscito si può rendere ripetibile, in due mosse.

**Mossa 1 · Il contesto in un Project.** Il blocco `<contesto>` del caso non va riscritto ogni volta: mettilo nelle istruzioni di un **Project**, insieme ai documenti del brand. Ogni chat aperta nel Project lo conosce già.

1. Barra laterale → **Projects** → nuovo Project. *(⚠ verifica il nome della voce)*
2. Nome chiaro: "UX Boutique — Brand & Tone".
3. Istruzioni: chi siamo, tono, cosa non fare mai.
4. Documenti: guida al tono, testi approvati, glossario.

**Mossa 2 · Il metodo in una Skill.** Il resto del prompt (ruolo, regole, formato, verifica) diventa una **Skill**: una cartella con un file `SKILL.md`, che Claude usa da solo quando il compito corrisponde.

### Come funziona una Skill
Claude legge sempre solo **nome e descrizione** di ogni Skill. Se la descrizione corrisponde al compito, legge il resto. Per questo **la descrizione è la parte più importante**: deve dire cosa fa la Skill e quando usarla.

```markdown
---
name: post-linkedin-ux-boutique
description: Scrive post LinkedIn per i servizi di UX Boutique, con il
  tono del brand. Usala quando l'utente chiede un post, un annuncio o un
  lancio per LinkedIn. Non usarla per testi interni.
---

# Post LinkedIn UX Boutique

## Procedura
1. Se mancano, chiedi servizio, pubblico e obiettivo.
2. Apri con un problema riconoscibile, chiudi con un invito all'azione.
3. Massimo 120 parole, due hashtag, nessuna emoji.
4. Nessun numero inventato: usa segnaposto come [X%].

## Esempi
Tono da seguire: "Il checkout perde utenti? Spesso il problema è in tre passaggi."
Tono da evitare: "Rivoluziona il tuo e-commerce!"

## Verifica
Dopo il post, elenca le affermazioni da controllare.
```

### Creare una Skill: chiedilo a Claude
Il modo più semplice è farla scrivere a Claude:
```
Trasforma il prompt che abbiamo usato in questa chat in una Skill.
Scrivi SKILL.md con nome, una descrizione che dica cosa fa e quando
usarla, la procedura, gli esempi e la verifica.
Fammi prima le domande che ti servono.
```

### Installarla
- **Su claude.ai:** comprimi la cartella in `.zip` (la cartella deve essere la radice) e caricala nelle impostazioni, sezione **Skills**. *(⚠ il percorso esatto del menu cambia)*
- **In Claude Code:** metti la cartella in `.claude/skills/` nel progetto, oppure in `~/.claude/skills/` per averla in tutti i tuoi progetti.

### Testarla con tre casi
1. **Tipico:** "Scrivi un post per il lancio della UX research." Deve attivarsi.
2. **Al limite:** "Scrivi un post per Instagram." Deve adattarsi o chiedere.
3. **Fuori scopo:** "Riassumi il verbale interno." Non deve attivarsi.

Se non si attiva, riscrivi la descrizione con le parole che usa chi chiede. Se si attiva quando non deve, aggiungi "Non usarla per…".

---

## 7 · Claude Design: dal testo al visual

**A cosa serve.** Prototipi, slide, one-pager e landing coerenti con il brand, creati parlando. È un'anteprima di ricerca di Anthropic Labs, disponibile per i piani Pro, Max, Team ed Enterprise. *(⚠ verifica l'accesso nel vostro piano)*

**Una volta sola: il design system.** Un designer carica i materiali del brand (siti, presentazioni, file di design). Claude ne estrae colori, tipografia e componenti. Il designer controlla il risultato e lo pubblica: da quel momento tutti i progetti del team lo usano in automatico. Senza questo passaggio, i lavori non sembrano vostri.

**Ogni volta: quattro passi.**
1. **Brief** con il BRIEF: pubblico, obiettivo, sezioni, vincoli.
2. **Tre strutture**, senza stile. Ne scegli una.
3. **Revisioni singole**, una per messaggio, con il perché.
4. **Export**: PDF, PPTX, HTML, Canva, oppure passaggio a Claude Code. *(⚠ verifica le opzioni nel menu)*

**Il prompt del caso:**
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

## 8 · Claude Code: dal visual al prodotto

**A cosa serve.** Claude Code è un agente: lavora dentro una cartella, legge e modifica file, esegue comandi. È nato per lo sviluppo, ma serve a chiunque lavori con file. Si usa da terminale, app desktop, web o editor di codice.

**Il ciclo di lavoro consigliato da Anthropic: quattro fasi.**
1. **Esplora:** Claude legge i file e capisce il problema, senza modificare niente.
2. **Pianifica:** propone un piano. Tu lo leggi e lo approvi. Esplora e pianifica si fanno in **plan mode**, che si attiva e si chiude con Shift+Tab. *(⚠ verifica nella tua versione)*
3. **Implementa e verifica:** Claude modifica i file e controlla il risultato, per esempio con i test o aprendo la pagina.
4. **Commit:** salva le modifiche con una descrizione chiara.

Separare la ricerca dalla modifica evita di risolvere il problema sbagliato. Tra un compito e l'altro, usa `/clear`: lo spazio di contesto si riempie in fretta e le prestazioni calano.

**Due regole di base.**
- **CLAUDE.md:** un file nella cartella con le regole del progetto (comandi, stile, cosa non toccare). Claude Code lo legge a ogni sessione. È il Project della cartella.
- **Permessi:** Claude chiede conferma prima di modificare file o eseguire comandi. Leggi sempre cosa chiede.

**Il prompt del caso:**
```
Trasforma il prototipo esportato da Claude Design nella pagina
servizi/audit.html del nostro sito. Usa solo i colori e i font di
design/tokens.json. Mostrami il piano prima di modificare.
```

**Metodo: prima i file.** Prepara i contenuti in file `.md` e trasformali in pagina o presentazione solo alla fine. Ogni modifica tocca solo la parte che serve e la storia resta salvata. Questo corso è fatto così.

---

## 9 · Plugin e connettori, in breve

- **Connettore:** collega Claude a uno strumento (Google Drive, Figma, Miro) per leggerne i dati. Si attiva nelle impostazioni, sezione Connectors. Nel piano Team, l'admin deve prima abilitarlo. *(⚠ verifica)*
- **Plugin:** un pacchetto che installa insieme Skill, comandi e connettori. In Claude Code si installano con `/plugin`. Nell'app desktop esistono plugin ufficiali per marketing, project management e altro. *(⚠ verifica la disponibilità nel vostro piano)*

**Regola di sicurezza.** Plugin e Skill scaricati possono eseguire istruzioni e comandi. Installa solo da fonti affidabili, e leggi cosa contengono prima di usarli.

---

## 10 · Cosa ci fa ogni ruolo

| Marketing | Design | Sviluppo |
|---|---|---|
| Piani editoriali e post, con Project e Skill | Sintesi di interviste e personas | Capire un progetto nuovo |
| Varianti di titoli e annunci | Analisi euristica da screenshot | Correggere bug partendo da un test |
| Report da file CSV o Excel | Prototipi in Claude Design | Componenti dai token del design system |

---

## 11 · Esercizi

1. **Il prompt.** Riscrivi un tuo prompt reale con il BRIEF. Fai il test del collega. Confronta i due risultati.
2. **Il ciclo.** Valuta il risultato su prodotto, processo e comportamento. Fai due iterazioni con la formula cosa + perché + come.
3. **Il metodo.** Trasforma il prompt riuscito in una Skill chiedendolo a Claude. Testala con i tre casi.

**Workshop finale a coppie miste.** Rifate il caso del capitolo 5 su un servizio vostro: delega, prompt, valutazione, verifica, Skill. Tre minuti per presentarlo.

---

## 12 · Per continuare: corsi gratuiti
Dopo questo corso, i passi naturali sono i corsi gratuiti di Anthropic Academy (in inglese, con certificato):

| Corso | Per chi | Cosa aggiunge |
|---|---|---|
| **Claude 101** | Tutti | Le basi del prodotto: Project, Artifacts, Skill, connettori, ricerca |
| **AI Fluency: Framework & Foundations** | Tutti | Il modello 4D nel dettaglio |
| **Claude Code 101** | Chi inizia con Claude Code | Primi passi con l'agente |
| **Claude Code in Action** | Chi usa già Claude Code | Il lavoro reale con l'agente |
| **Introduction to agent skills** | Chi crea Skill | Creare, configurare e condividere Skill |
| **Introduction to subagents** | Chi usa Claude Code | Affidare compiti ad agenti secondari |

Per il prompt: il **tutorial interattivo di prompt engineering** di Anthropic (gratuito, su GitHub) e **Google Prompting Essentials** (su Coursera).

*(⚠ Il catalogo cambia spesso: alcune fonti riportano che Anthropic Academy è stata rinominata Claude Academy. Verifica titoli e disponibilità sul sito.)*

---

## Prima del corso: da verificare
1. Nome e posizione delle voci Projects, Skills e Connectors nel vostro account.
2. Accesso a Claude Design nel piano Team e opzioni di export.
3. Connettori Drive, Figma e Miro abilitati dall'admin.
4. Scorciatoia del plan mode nella versione di Claude Code installata.
5. Disponibilità dei plugin nel vostro piano.

## Fonti
- Anthropic Academy, *AI Fluency: Framework & Foundations* (modello 4D): https://anthropic.skilljar.com · documento del framework: https://www-cdn.anthropic.com/b383cf6baddbfc72fdf8b0ed533a518e2872d531.pdf
- Anthropic Academy, *Claude 101*: https://anthropic.skilljar.com/claude-101
- Anthropic, *Prompting best practices*: https://platform.claude.com/en/docs/build-with-claude/prompt-engineering/claude-prompting-best-practices
- Anthropic, *Use XML tags*: https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/use-xml-tags
- Anthropic, *Prompt Engineering Interactive Tutorial*: https://github.com/anthropics/prompt-eng-interactive-tutorial
- Claude Code, *Best practices*: https://code.claude.com/docs/en/best-practices
- Google, *Prompting Essentials* (metodo TCREI): https://www.coursera.org/google-learn/prompting-essentials
- Anthropic, *Introducing Claude Design*: https://www.anthropic.com/news/claude-design-anthropic-labs
- Claude Help Center, guida admin di Claude Design: https://support.claude.com/en/articles/14604406-claude-design-admin-guide-for-team-and-enterprise-plans
- Claude Code, plugin: https://code.claude.com/docs/en/discover-plugins
- Skills: https://claude.com/docs/skills/how-to

Corsi in italiano: ho trovato solo corsi commerciali di taglio diverso (per commercialisti, per sviluppatori) e nessun programma ufficiale. Non c'era materiale da integrare.
