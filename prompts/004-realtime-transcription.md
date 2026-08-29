# Prompt 004 — Realtime Transcription

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


Leggi `docs/04-transcription.md`.

## Task

- CP-301
- CP-302
- CP-303
- CP-304
- CP-305

## Obiettivo

Trascrivere ME e OTHER in realtime.

## Requisiti

- `TranscriptionProvider`;
- provider iniziale configurabile;
- transcript partial/final se disponibile;
- timestamp;
- speaker;
- UI transcript.

## Vincolo

Conversation Engine e UI non devono dipendere direttamente dal provider concreto.

## Acceptance criteria

Una breve conversazione deve apparire nella UI come sequenza ME/OTHER.
