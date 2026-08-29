# 05 — Conversation Engine

## Responsabilità

Il Conversation Engine mantiene lo stato semantico della call.

Non è un semplice log di trascrizione.

## Message model

```json
{
  "id": "uuid",
  "speaker": "ME",
  "text": "Abbiamo scelto PostgreSQL.",
  "timestamp": 30.2,
  "intent": "STATEMENT",
  "requires_answer": false
}
```

## Intent

Valori iniziali:
- QUESTION;
- REQUEST;
- OBJECTION;
- STATEMENT;
- CONFIRMATION;
- UNKNOWN.

## requires_answer

Booleano che indica se è opportuno generare un suggerimento.

Esempi:

"Ok, perfetto."
- CONFIRMATION
- false

"Come avete implementato questa parte?"
- QUESTION
- true

"Non sono convinto dei tempi."
- OBJECTION
- true

## Context window

Non inviare tutta la call al modello.

Strategia iniziale:
- ultime N battute;
- limite token;
- summary incrementale della parte precedente.

## Manual trigger

La hotkey deve poter creare una suggestion request anche se `requires_answer == false`.

## Suggestion request

```json
{
  "trigger": "AUTO",
  "last_other_message_id": "...",
  "conversation_context": [],
  "project_id": null,
  "answer_style": "NORMAL"
}
```

## Anti-spam

Non generare continuamente suggerimenti per:
- partial transcript;
- frase ancora in corso;
- duplicate;
- conferme brevi;
- rumore.
