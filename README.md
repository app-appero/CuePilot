# CuePilot — Project Documentation

CuePilot è un'applicazione desktop personale per Windows 11 progettata per assistere l'utente durante call e conversazioni in tempo reale.

L'app ascolta il microfono dell'utente e l'audio di sistema, trascrive la conversazione, distingue l'utente dall'interlocutore, identifica domande/richieste e genera suggerimenti testuali da mostrare in un overlay always-on-top.

## Obiettivo del repository

Questo repository deve essere utilizzabile sia da uno sviluppatore umano sia da AI coding assistant come Codex, Claude o Cursor.

La cartella `docs/` contiene la fonte di verità del progetto.

La cartella `prompts/` contiene prompt operativi da utilizzare milestone per milestone.

## Ordine consigliato di lettura per un AI coding assistant

1. `docs/00-vision.md`
2. `docs/01-requirements.md`
3. `docs/02-architecture.md`
4. `docs/10-roadmap.md`
5. `docs/11-backlog.md`
6. `docs/12-definition-of-done.md`
7. `docs/13-coding-guidelines.md`
8. `docs/14-ai-agent-instructions.md`
9. Il documento tecnico relativo alla feature da implementare.

## Regola fondamentale

Non implementare l'intero prodotto in una sola iterazione.

Procedere per task e milestone, rispettando:
- scope del task;
- dipendenze;
- acceptance criteria;
- Definition of Done;
- vincoli architetturali.

## Stack iniziale

### Desktop
- Tauri
- React
- TypeScript
- Windows 11

### Backend locale
- Python
- FastAPI

### Storage
- SQLite

### AI
- provider abstraction per Speech-to-Text;
- provider abstraction per LLM;
- OpenAI come provider iniziale possibile;
- possibilità futura di provider locali.

## Principi

- local-first;
- desktop-first;
- single-user;
- privacy by default;
- niente autenticazione;
- niente multiutente;
- niente billing;
- niente backend cloud proprietario;
- niente dipendenza obbligatoria da Zoom/Meet/Teams;
- funzionamento tramite audio del PC.

## Avvio sviluppo consigliato

Usare i prompt nella cartella `prompts/` in ordine numerico.

Ogni prompt deve essere eseguito solo dopo che il precedente ha superato i relativi acceptance criteria.

## Nome

Nome provvisorio del progetto: **CuePilot**.
