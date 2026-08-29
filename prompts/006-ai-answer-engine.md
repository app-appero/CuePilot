# Prompt 006 — AI Answer Engine

## Istruzioni comuni

Prima di procedere:

1. leggi `README.md`;
2. leggi `docs/00-vision.md`;
3. leggi `docs/01-requirements.md`;
4. leggi `docs/02-architecture.md`;
5. leggi `docs/10-roadmap.md`;
6. leggi `docs/11-backlog.md`;
7. leggi `docs/12-definition-of-done.md`;
8. leggi `docs/13-coding-guidelines.md`;
9. leggi `docs/14-ai-agent-instructions.md`;
10. analizza la codebase esistente.

Non implementare feature fuori scope.

Al termine:
- esegui i controlli disponibili;
- elenca file modificati;
- indica test eseguiti;
- segnala problemi aperti;
- suggerisci il prossimo task ID.


Leggi `docs/06-ai-engine.md`.

## Task

- CP-501
- CP-502
- CP-503
- CP-504
- CP-505
- CP-506

## Obiettivo

Generare suggerimenti testuali.

## System prompt di base

Sei un assistente personale che supporta l'utente durante una conversazione in tempo reale.

Il tuo compito è suggerire all'utente cosa potrebbe rispondere all'interlocutore.

Non stai parlando direttamente con l'interlocutore.

Regole:
1. usa il contesto disponibile;
2. non inventare informazioni;
3. rispondi all'ultima domanda/richiesta rilevante;
4. usa linguaggio naturale e parlato;
5. evita introduzioni inutili;
6. non mostrare ragionamento interno;
7. mantieni la risposta compatibile con una conversazione live.

## Acceptance criteria

Input con domanda + contesto deve restituire answer valida nei tre stili previsti.
