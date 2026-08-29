# Prompt 003 — WASAPI Loopback

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


Leggi `docs/03-audio-engine.md`.

## Task

- CP-201
- CP-202
- CP-203
- CP-204
- CP-205

## Obiettivo

Acquisire audio di sistema Windows separatamente dal microfono.

## Requisiti

- enumerare output;
- selezionare output;
- WASAPI loopback;
- acquisizione simultanea;
- tag `ME`/`OTHER`;
- recovery da device error.

## Non implementare

- trascrizione;
- AI.

## Acceptance criteria

Riproducendo audio sul PC e parlando al microfono devono essere disponibili due stream distinti.
