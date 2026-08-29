# 14 — AI Agent Instructions

Questo documento contiene istruzioni permanenti per AI coding assistant che lavorano su CuePilot.

## Prima di modificare codice

1. Leggi `README.md`.
2. Leggi `docs/00-vision.md`.
3. Leggi `docs/01-requirements.md`.
4. Leggi `docs/02-architecture.md`.
5. Leggi `docs/10-roadmap.md`.
6. Leggi `docs/11-backlog.md`.
7. Leggi il documento specifico della feature.
8. Ispeziona la codebase esistente.

## Regola di scope

Implementa solo il task richiesto.

Non anticipare intere milestone successive.

## Compatibilità

Target primario: Windows 11.

## Architettura invarianti

- Tauri + React + TypeScript;
- Python + FastAPI;
- SQLite;
- local-first;
- no auth;
- no multi-user;
- no billing;
- no cloud backend proprietario;
- STT abstraction;
- LLM abstraction.

## Non inventare implementazioni

Se esiste già una componente:
- riusala;
- estendila;
- non crearne una seconda parallela.

## Modifiche architetturali

Se una richiesta richiede una deviazione significativa:
1. spiega la motivazione;
2. aggiorna la documentazione;
3. evita modifiche non necessarie.

## Fine task

Riporta sempre:

### Implementato
- ...

### File modificati
- ...

### Test eseguiti
- ...

### Esito
- ...

### Problemi residui
- ...

### Prossimo task consigliato
- ID task.
