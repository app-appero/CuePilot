# 01 — Requirements

## Requisiti funzionali

### FR-001 — Avvio applicazione
L'utente deve poter avviare CuePilot come normale applicazione Windows.

### FR-002 — Selezione microfono
L'app deve mostrare i dispositivi di input disponibili.

### FR-003 — Selezione output audio
L'app deve mostrare i dispositivi di output disponibili.

### FR-004 — Cattura microfono
L'app deve acquisire l'audio del microfono selezionato.

### FR-005 — Cattura audio sistema
L'app deve acquisire l'audio riprodotto dal dispositivo selezionato tramite WASAPI loopback o equivalente.

### FR-006 — Trascrizione realtime
Il sistema deve trasformare l'audio in testo con latenza compatibile con una conversazione.

### FR-007 — Speaker separation
Le trascrizioni devono indicare almeno:
- ME;
- OTHER.

### FR-008 — Conversation buffer
Il sistema deve mantenere memoria delle battute recenti.

### FR-009 — Intent detection
Il sistema deve classificare almeno:
- QUESTION;
- REQUEST;
- OBJECTION;
- STATEMENT;
- CONFIRMATION;
- UNKNOWN.

### FR-010 — Rilevamento risposta necessaria
Il sistema deve stimare se l'utente dovrebbe rispondere.

### FR-011 — Generazione suggerimento
Il sistema deve produrre testo naturale e pronunciabile.

### FR-012 — Modalità risposta
Almeno:
- breve;
- normale;
- tecnica.

### FR-013 — Rigenerazione
L'utente deve poter rigenerare la risposta.

### FR-014 — Hotkey manuale
L'utente deve poter forzare la generazione sulla base dell'ultima parte della conversazione.

### FR-015 — Overlay
La risposta deve poter essere mostrata in una finestra always-on-top.

### FR-016 — Start/Stop session
L'utente deve poter avviare e terminare una sessione.

### FR-017 — Knowledge base
La V1 avanzata deve poter associare documenti locali a un progetto.

### FR-018 — Summary
A fine call il sistema può generare:
- riepilogo;
- decisioni;
- task;
- domande aperte.

## Requisiti non funzionali

### NFR-001 — Latenza
Target iniziale: suggerimento entro pochi secondi dalla fine della frase rilevante.

### NFR-002 — Stabilità audio
L'acquisizione non deve interrompersi per normali cambi di intensità o silenzi.

### NFR-003 — Privacy
Audio e trascrizioni non devono essere salvati di default.

### NFR-004 — Modularità
STT e LLM devono essere sostituibili.

### NFR-005 — Single-user
Nessun sistema di autenticazione richiesto.

### NFR-006 — Windows
Target primario Windows 11.

### NFR-007 — Fail gracefully
Se STT/LLM non è disponibile, l'app non deve crashare.

### NFR-008 — Configurazione
Segreti e chiavi API non devono essere versionati.

## Fuori scope MVP

- diarization multi-speaker avanzata;
- riconoscimento identità interlocutori;
- mobile;
- cloud sync;
- supporto team;
- login;
- pagamenti;
- browser extension;
- speech synthesis automatico.
