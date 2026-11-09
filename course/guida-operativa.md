# Claude AI — Guida operativa
### Come usare ogni funzionalità, passo per passo · UX Boutique

> Questa guida accompagna il corso approfondito (`corso-approfondito.md`). Qui trovate i **passi operativi**: cosa cliccare, cosa scrivere, come verificare che funzioni, cosa fare se non funziona.
>
> **Nota di verifica.** I nomi dei menu cambiano con gli aggiornamenti. Dove un nome può essere diverso, lo segnalo con *(verifica il nome nel tuo account)*. La logica di ogni passo resta la stessa.

---

## Indice

1. Scrivere un prompt corretto
2. Creare un Project
3. Artifacts
4. Ricerca web e ricerca approfondita
5. Analisi di file
6. Creare una Skill
7. Installare e far funzionare una Skill
8. Connectors
9. MCP
10. Plugins
11. Claude Design: dal brief al prototipo
12. Figma MCP
13. Claude Code: installazione e primo uso
14. CLAUDE.md
15. Plan mode, permessi, subagent
16. Attività programmate
17. Risoluzione problemi

---

## 1. Scrivere un prompt corretto

### Struttura
Un prompt efficace risponde a sei domande. Non tutte servono sempre, ma quelle mancanti spiegano quasi ogni risultato deludente.

```
[Background]  Chi siamo, per chi lavoriamo, a cosa serve questo testo.
[Ruolo]       Chi deve rispondere e con quale competenza.
[Intento]     Cosa deve ottenere la persona che legge.
[Esempi]      Un esempio di output buono (o uno cattivo da evitare).
[Formato]     Lunghezza, struttura, lingua, cosa escludere.
[Verifica]    Come controllare che il risultato sia corretto.
```

### Esempio: prima e dopo

**Prompt debole**
> Scrivi un post per Instagram sul nostro nuovo servizio di audit.

**Prompt corretto**
```
Background: UX Boutique offre audit di usabilità per e-commerce di medie
dimensioni. Il pubblico sono responsabili marketing, non designer.

Ruolo: sei un copywriter senior. Tono sobrio, concreto, senza superlativi.

Intento: far richiedere l'audit gratuito di 30 minuti.

Esempio di tono da seguire:
"Il checkout perde utenti? Di solito il problema è in tre passaggi. Li troviamo in 30 minuti."

Formato: un post di massimo 120 parole, lingua italiana, due hashtag,
nessuna emoji. Chiudi con l'invito a prenotare.

Verifica: alla fine elenca le affermazioni che un cliente potrebbe
contestare, così le controllo prima di pubblicare.
```

### Regole pratiche
- **Una richiesta per volta.** "Scrivi, traduci e adatta per LinkedIn" produce un risultato mediocre su tutto. Fate tre richieste.
- **Date esempi concreti.** Un esempio vale più di tre aggettivi. "Tono professionale" non dice nulla; un paragrafo di esempio sì.
- **Dite cosa escludere.** "Niente emoji", "non citare clienti", "non usare il termine *ottimizzare*".
- **Chiedete l'autocritica.** "Rileggi la tua bozza rispetto ai criteri sopra e segnala cosa non rispetta."

### Iterare
Un buon feedback indica cosa cambiare, perché, e come.
- Debole: "Non mi piace."
- Efficace: "Il titolo è troppo generico per un pubblico tecnico. Proponi tre alternative che contengano un numero."

Fate **una revisione per volta**. Se cambiate tre cose insieme, non capite quale ha funzionato.

### Quando il prompt non funziona
Chiedetevi:
1. Ho descritto il pubblico?
2. Ho dato un esempio?
3. Ho detto il formato e la lunghezza?
4. Il contesto (brand, documenti) è già nel Project?

Quasi sempre la risposta a una di queste domande spiega il problema.

---

## 2. Creare un Project

### Cosa serve
Un Project ha tre parti: **nome**, **istruzioni**, **knowledge base** (i documenti).

### Passi
1. Nel menu laterale scegliete **Projects** *(verifica il nome nel tuo account)* e **Nuovo Project**.
2. Date un nome preciso: "UX Boutique — Brand & Tone", non "Progetto 1".
3. Scrivete le **istruzioni** (vedi sotto).
4. Caricate i **documenti** nella knowledge base.
5. Aprite una nuova chat dentro il Project.

### Istruzioni: template
```
Lavoriamo per UX Boutique, agenzia di UX e design digitale.
Lingua: italiano. Tono: diretto, concreto, senza superlativi vuoti.
Ogni testo per clienti deve indicare un beneficio misurabile.
Non citare mai clienti senza approvazione scritta.
Quando non sei sicuro di un fatto, dichiaralo esplicitamente.
Usa il glossario nei documenti caricati; evita i termini elencati lì come "da non usare".
```

### Knowledge base: cosa caricare
- **Sì**: guida al tono, testi approvati come esempi, glossario, offerta ufficiale.
- **No**: bozze, duplicati, documenti con dati personali non necessari.
- **Formato**: file con testo selezionabile (non scansioni), titoli chiari, massimo qualche pagina per documento.

### Test di un Project
Chiedete una cosa che conoscete già la risposta: "Scrivi un'intro di 60 parole per la pagina servizi." Se il risultato rispetta tono, glossario e regole senza che le ripetiate, il Project funziona. Se no, controllate: le istruzioni sono chiare? I documenti sono quelli giusti?

### Condivisione (piano Team)
Il Project condiviso è disponibile a tutto il team *(verifica chi può condividere nel tuo piano)*. Chi modifica le istruzioni deve avvisare gli altri: un cambio silenzioso crea risultati diversi senza spiegazione.

---

## 3. Artifacts

### Cos'è
Un Artifact è un output autonomo (documento, presentazione, foglio, pagina interattiva) che si apre accanto alla chat e si modifica senza rifare tutto.

### Come usarlo
1. Chiedete esplicitamente il formato: "Crea un documento Artifact con…".
2. Verificate il risultato nella finestra accanto alla chat.
3. Per modificare una parte, indicatela: "Nella sezione *Metodo*, riduci a tre punti."
4. Esportate quando è pronto (copia, download *(verifica i formati disponibili)*).

### Errori frequenti
- Chiedere una modifica generica ("migliora tutto"): il risultato cambia troppo.
- Non indicare il formato: Claude può rispondere in chat invece che in Artifact.

---

## 4. Ricerca web e ricerca approfondita

### Ricerca web
Attivatela quando serve un'informazione recente. Chiedete **le fonti** nel prompt: "Indica per ogni affermazione la fonte e la data."

### Ricerca approfondita
Per temi ampi e confronti. Fa più passaggi e produce un rapporto con fonti.
- Definite la domanda in una frase.
- Indicate il periodo e il pubblico.
- Chiedete un formato: "tabella con fonte, data, affermazione".

### Regola di verifica
Ogni dato trovato va aperto sulla fonte originale prima di essere usato. Le fonti possono essere sbagliate, datate o citate in modo impreciso.

---

## 5. Analisi di file

### Tipi supportati e uso
- **PDF**: "Estrai le date di scadenza dei contratti in questo file."
- **Excel/CSV**: "Calcola il costo per lead per canale e segnala i valori anomali."
- **Immagini e screenshot**: "Individua i problemi di contrasto e accessibilità in questa schermata."

### Procedura
1. Caricate il file (icona di allegato *(verifica il nome nel tuo account)*).
2. Descrivete la domanda in una frase.
3. Chiedete un output strutturato (tabella, elenco con numeri di pagina).
4. Verificate un campione a mano: un numero su dieci.

### Attenzione
- Un'immagine sfocata o un PDF scansionato danno risultati scarsi: controllate prima la leggibilità.
- Non caricate dati personali o riservati senza permesso (vedi cap. 10 del corso).

---

## 6. Creare una Skill

### Cos'è una Skill
Una Skill è un **metodo scritto una volta** e riutilizzabile. Ha una cartella con un file principale `SKILL.md`, che contiene:
- un **nome**;
- una **descrizione** che dice quando usarla (Claude la usa per decidere se attivarla);
- le **istruzioni** passo per passo;
- eventuali **criteri di qualità** ed **esempi**.

Una Skill non è un prompt lungo. Un prompt serve una volta; una Skill serve ogni volta che il compito si ripete.

### Quando creare una Skill
Un compito è un buon candidato se:
- si ripete più di tre volte al mese;
- segue sempre lo stesso schema;
- l'output si può giudicare (è giusto o sbagliato, completo o no).

### Struttura della cartella
```
tono-ux-boutique/
├── SKILL.md
└── esempi/
    ├── post-buono.md
    └── post-da-evitare.md
```

### SKILL.md: template completo
```markdown
---
name: tono-ux-boutique
description: Scrive o revisiona testi per UX Boutique secondo il tono di voce del brand. Usala quando l'utente chiede copy, post, claim, intro o revisione di testi destinati a clienti o al sito.
---

# Tono di voce UX Boutique

## Quando usarla
Testi per clienti, post social, pagine del sito, email commerciali.
Non usarla per documenti interni o codice.

## Procedura
1. Chiedi (se mancano) pubblico, obiettivo e lunghezza.
2. Scrivi la bozza in italiano, tono diretto e concreto.
3. Ogni affermazione deve avere un beneficio misurabile o essere marcata come da verificare.
4. Applica il glossario: usa i termini "da usare", evita quelli "da non usare".
5. Rileggi la bozza rispetto ai criteri qui sotto e segnala le violazioni.

## Criteri di qualità
- Nessun superlativo vuoto ("il migliore", "rivoluzionario").
- Massimo una call to action per testo.
- Frasi sotto le 25 parole.
- Nessun cliente citato senza approvazione.

## Esempi
Vedi la cartella `esempi/`: leggi prima il file "buono" e quello "da evitare".

## Formato di output
Testo finale, poi una lista breve: "Da verificare: ..." con le affermazioni che richiedono conferma.
```

### Regole per una buona descrizione
La descrizione è la parte più importante. Claude la legge per decidere se usare la Skill.
- **Dite cosa fa** e **quando usarla**, con le parole che userebbe l'utente.
- **Siate specifici**: "copy e post per clienti" è meglio di "scrittura".
- **Evitate i nomi interni**: se gli utenti dicono "post", scrivete "post".

Esempio debole: `description: Aiuta con i testi.`
Esempio efficace: `description: Scrive o revisiona post, claim e pagine per clienti UX Boutique. Usala quando l'utente chiede testi commerciali o revisione di copy.`

### Scrivere le istruzioni
- **Passi numerati**, nell'ordine in cui vanno fatti.
- **Istruzioni precise**: "Se il pubblico non è indicato, chiedilo" invece di "tieni conto del pubblico".
- **Un esempio buono e uno da evitare** insegnano più di una lunga descrizione.
- Tenete il file **sotto le 500 righe**. Se è più lungo, spostate i dettagli in file separati che la Skill legge quando servono.

---

## 7. Installare e far funzionare una Skill

### Dove installarla

**Su claude.ai (chat e Project)**
1. Aprite le impostazioni dell'account e cercate la sezione **Skills** *(verifica il nome nel tuo account)*.
2. Caricate la cartella (o il file `.zip` della cartella) con `SKILL.md` alla radice.
3. Attivatela per il vostro account. Nel piano Team, l'admin può renderla disponibile a tutto il team *(verifica i permessi)*.

**In Claude Code (repository)**
1. Create la cartella nel repository: `.claude/skills/tono-ux-boutique/SKILL.md`.
2. Salvate e committate la cartella: così la Skill è condivisa con chi lavora sul repo.
3. Per una Skill personale, usate la cartella dell'utente invece del repository.

### Verificare che sia caricata
Chiedete a Claude: **"Quali Skill hai disponibili per questo compito?"**. Se la vostra Skill non compare, controllate:
- il nome del file è esattamente `SKILL.md` (maiuscole comprese);
- il frontmatter è corretto (`---` sopra e sotto, `name` e `description` presenti);
- la Skill è attiva per il vostro account o per il progetto.

### Testare una Skill: il metodo a tre casi
Non basta un test. Preparate tre casi:
1. **Caso tipico**: il compito per cui è stata scritta. Deve funzionare bene.
2. **Caso al limite**: un compito simile ma non identico. Deve adattarsi o chiedere.
3. **Caso fuori scopo**: un compito che non le appartiene (es. un documento interno). Non deve attivarsi.

Per ogni caso, annotate: si è attivata? Ha seguito i passi? L'output rispetta i criteri?

### Diagnosi: la Skill non si attiva
- **Causa più frequente**: la descrizione è troppo vaga. Riscrivetela con le parole dell'utente.
- Chiedete esplicitamente: "Usa la Skill tono-ux-boutique per questo testo." Se ora funziona, il problema è la descrizione.

### Diagnosi: si attiva ma il risultato è sbagliato
- Controllate le istruzioni: sono ambigue? Ci sono passi mancanti?
- Aggiungete un esempio "da evitare" che mostri l'errore.
- Aggiungete un criterio di qualità misurabile.

### Diagnosi: si attiva quando non dovrebbe
- Restringete la descrizione: aggiungete "non usarla per…".

### Iterare
Modificate una cosa per volta e ritestate i tre casi. Tenete una versione numerata nel repository (`SKILL.md` con storia Git) così potete tornare indietro.

---

## 8. Connectors

### Cos'è
Un connettore permette a Claude di leggere (e in alcuni casi scrivere) nei vostri strumenti: Google Drive, Notion, Slack, Gmail, GitHub, Figma.

### Collegare un connettore
1. Aprite le impostazioni e cercate **Connectors** *(verifica il nome nel tuo account)*.
2. Scegliete lo strumento e autorizzate l'accesso con il vostro account.
3. Verificate i permessi concessi: in lettura, o anche in scrittura?

### Usarlo
Chiedete in modo preciso: "Cerca nel Drive la cartella del cliente X e riassumi l'ultimo brief caricato." Specificate cosa cercare e dove.

### Regole
- **Minimo permesso**: concedete solo ciò che serve.
- **Verifica il risultato**: un connettore può trovare il file sbagliato o una versione vecchia.
- **Dati sensibili**: prima di collegare uno strumento con dati riservati, controllate con l'admin.

### Problemi comuni
- **Non trova il file**: chiedete il nome esatto o il link.
- **Accesso negato**: il vostro account non ha il permesso sullo strumento di origine; chiedete al proprietario.

---

## 9. MCP

### Cos'è
MCP (Model Context Protocol) è lo standard con cui uno strumento espone le sue funzioni a Claude. È la "presa USB": lo strumento e Claude si collegano senza adattatori su misura.

### Quando serve
- Quando un connettore già pronto non copre quello che vi serve.
- Quando lo strumento ha un server MCP ufficiale (es. Figma, GitHub).

### Aggiungere un server MCP in Claude Code
Da terminale, nella cartella del progetto:
```bash
claude mcp add nome-server -- comando-del-server
```
Per la lista dei server attivi:
```bash
claude mcp list
```
*(verifica la sintassi aggiornata nella documentazione di Claude Code)*

### Sicurezza
- Un server MCP può fare azioni reali (scrivere su un file, inviare un messaggio). Installate solo server di cui vi fidate.
- Controllate le azioni che Claude propone prima di confermarle, soprattutto se scrivono.

---

## 10. Plugins

### Cos'è
Un plugin è un **pacchetto** che combina Skill, connettori e impostazioni per un ambito preciso (es. "project management", "design review").

### Come usarlo
1. Cercate il plugin tra quelli disponibili nel vostro account *(verifica la sezione)*.
2. Installatelo e leggete la sua descrizione: cosa include, quali permessi richiede.
3. Testatelo su un caso non critico prima di usarlo su lavoro reale.

### Regola
Un plugin è scatola chiusa: prima di usarlo, capite cosa fa. Se non sapete spiegare le sue Skill e i suoi permessi, non usatelo ancora.

---

## 11. Claude Design: dal brief al prototipo

Questo è il flusso operativo. Lo seguite con un brief reale.

### Passo 1: preparare il contesto
1. Aprite il Project del brand (vedi sezione 2).
2. Verificate che contenga: tono di voce, brand kit (colori HEX, font, logo), design system se esiste.
3. Chiedete una verifica: "Descrivi il brand che stai usando: colori, font, tono." Se non corrisponde, correggete prima di procedere.

### Passo 2: scrivere il brief
Usate la struttura del BRIEF:
```
Background: UX Boutique offre audit di usabilità per e-commerce di medie dimensioni.
Ruolo: designer UX senior, sobrio e concreto.
Intento: far richiedere l'audit gratuito.
Esempi: [allegate uno screenshot di una landing che vi piace] + una frase su
        cosa vi piace (es. "gerarchia chiara, un'unica call to action").
Formato: landing con hero, tre benefici misurabili, un caso studio,
         una call to action, footer. Mobile first.
```

### Passo 3: chiedere la struttura, non lo stile
Primo prompt:
```
Proponi tre strutture diverse di landing. Per ciascuna: sezioni in ordine
e contenuto di ogni sezione. Non applicare ancora colori né font.
```
Perché: se struttura e stile arrivano insieme, non capite quale parte non funziona.

### Passo 4: scegliere e produrre il prototipo
Scegliete una struttura e chiedete:
```
Procedi con la struttura 2. Crea il prototipo come Artifact, mobile first.
```

### Passo 5: revisioni mirate
Una revisione per volta:
```
Il titolo dell'hero è generico. Proponi tre alternative che contengano
un numero concreto. Applica la prima e lascia il resto invariato.
```

### Passo 6: verificare prima di esportare
Checklist:
- [ ] Il contenuto è vero? I numeri sono approvati?
- [ ] Il tono rispetta il Project?
- [ ] Il layout funziona su mobile?
- [ ] La call to action è una sola?
- [ ] Il brand (colori, font) corrisponde al brand kit?

### Passo 7: esportare
- **HTML**: prototipo navigabile, da condividere o passare allo sviluppo.
- **PDF**: one-pager o documento da inviare o stampare.
- **PPTX**: presentazione da modificare in PowerPoint o Keynote. Verificate i font.
- **Canva**: da completare in Canva. Dipende dal connettore attivo.

*(verifica i formati disponibili nel vostro piano)*

### Errori frequenti
| Sintomo | Causa | Soluzione |
|---|---|---|
| Risultato generico | Brief vago | Aggiungete pubblico, obiettivo, esempio |
| Stile non coerente con il brand | Brand kit assente nel Project | Caricate il brand kit e ritestate |
| Testi con claim non verificati | Nessuna regola di verifica | Aggiungete "marca come da verificare" nelle istruzioni |
| Layout rotto su mobile | Non richiesto | Chiedete esplicitamente "mobile first" |

---

## 12. Figma MCP

### Cosa fa
Permette a Claude di leggere e, in alcuni casi, scrivere nei file Figma del team.

### Collegarlo
1. Attivate il connettore o il server MCP di Figma *(verifica il nome nel tuo account)*.
2. Autorizzate l'accesso con il vostro account Figma di team.
3. Verificate con una domanda semplice: "Elenca i file Figma a cui hai accesso."

### Leggere: estrarre i token
Chiedete: "Dal file [nome o link], estrai i colori e i font del design system in formato JSON."
Verificate i valori sul file originale: un token mancante o sbagliato propaga errori.

### Scrivere: creare o modificare sul canvas
**Regola.** Fate le scritture su una copia o su una pagina di prova. Verificate prima di confermare, perché il file è del team.

### Flusso completo Design ↔ Figma ↔ Code
1. Claude Design produce il prototipo.
2. Figma MCP estrae i token dal design system.
3. Claude Code usa i token per generare il componente.

---

## 13. Claude Code: installazione e primo uso

### Installazione
Scegliete una via:
- **App desktop**: scaricatela dal sito Claude e accedete con il vostro account.
- **Terminale**: installate Claude Code seguendo la documentazione ufficiale *(verifica il comando aggiornato)*, poi lanciate `claude` dalla cartella di lavoro e accedete.

### Primo uso
1. Aprite una cartella **con Git** (un repository). Se non è un repository, inizializzatelo: `git init`.
2. Avviate `claude` nella cartella.
3. Chiedete una cosa semplice: "Elenca i file di questa cartella e spiega cosa contengono."
4. Verificate che il risultato sia corretto prima di chiedere modifiche.

### Regola d'oro
Prima di ogni modifica importante: commit. Così potete tornare indietro con `git` se qualcosa va storto.

---

## 14. CLAUDE.md

### Cos'è
Il file `CLAUDE.md` nella radice del progetto contiene le istruzioni permanenti. Claude Code lo legge all'inizio di ogni sessione.

### Cosa scriverci
- Cos'è il progetto e a cosa serve.
- Stack e strumenti (es. HTML + CSS, nessun framework).
- Dove sono le regole (tono, design system).
- Cosa non toccare.
- Come si lavora: "prima di ogni modifica, mostra il piano".

### Template
```markdown
# Progetto: sito UX Boutique

## Cos'è
Sito vetrina e pagine servizi. Lingua italiana.

## Stack
- HTML e CSS. Nessun framework.
- Token di design in `design/tokens.json`.

## Regole
- Tono dei testi: `docs/tono-di-voce.md`.
- Non modificare mai la cartella `legacy/`.
- Non committare file con chiavi o credenziali.

## Come lavorare
- Prima di modifiche che toccano più file: mostra il piano e aspetta approvazione.
- Dopo ogni modifica: elenca i file cambiati.
```

### Verifica
Chiedete: "Quali regole del CLAUDE.md stai applicando?" Se la risposta è corretta, il file è letto.

---

## 15. Plan mode, permessi, subagent

### Plan mode
Claude propone un piano e aspetta la vostra approvazione prima di modificare i file.
- Attivazione: di solito con **Shift+Tab** nel terminale *(verifica la scorciatoia nella versione installata)*.
- Usatelo sempre per modifiche su più file o non facili da annullare.
- Leggete il piano: se un passo non vi è chiaro, chiedete di spiegarlo prima di approvare.

### Permessi
Claude Code chiede il permesso per modificare file ed eseguire comandi.
- **Leggete cosa vi viene chiesto** prima di confermare.
- Non concedete permessi generici ("approva tutto") se non sapete cosa fanno.
- Potete concedere permessi per una singola azione o per la sessione.

### Subagent
Un subagent è un agente secondario che lavora su un sotto-compito e restituisce il risultato.
- Utile per compiti separati (es. "verifica i test" mentre l'altro agente scrive il codice).
- Ogni subagent ha istruzioni proprie: definitele in modo chiaro.

---

## 16. Attività programmate

### Cosa sono
Compiti che Claude esegue a intervalli regolari (es. ogni lunedì, il report settimanale).

### Come configurarle
1. Scrivete il compito come se lo deste a un collega: input, passi, output.
2. Testatelo a mano una volta, prima di programmarlo.
3. Programmate con l'intervallo desiderato *(verifica dove si configura nel vostro account)*.
4. Definite dove finisce l'output (cartella, documento, canale).

### Regola
Ogni output automatico ha un controllo umano. Non inviate a un cliente un report generato automaticamente senza rileggerlo.

---

## 17. Risoluzione problemi

| Problema | Cosa controllare | Soluzione |
|---|---|---|
| La risposta è generica | Il brief ha Background e Intento? | Aggiungete le parti mancanti |
| La Skill non si attiva | La descrizione del frontmatter | Riscrivetela con le parole dell'utente |
| La Skill si attiva sempre | La descrizione è troppo ampia | Aggiungete "non usarla per…" |
| Il connettore non trova il file | Nome esatto, permessi | Chiedete il link diretto |
| Claude ignora il Project | Il Project è quello giusto? | Aprite una nuova chat dentro il Project |
| La chat è lenta o confusa | Chat molto lunga | Riassumete e aprite una chat nuova |
| Claude Code non segue CLAUDE.md | Il file è nella radice? | Spostatelo e chiedete la verifica |
| Numeri sbagliati | Nessuna verifica | Controllate un campione a mano |

---

## Domande aperte per la prossima revisione

Queste informazioni cambiano il contenuto delle guide:
- Usate Claude principalmente dalla chat web, da Claude Code o da entrambi?
- Il vostro admin ha già abilitato Skills, connettori e Project condivisi nel piano Team?
- Quali strumenti del team devono essere collegati per primi (Drive, Notion, Figma, GitHub)?
