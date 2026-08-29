# 06 — AI Engine

## Obiettivo

Generare suggerimenti utili, brevi, naturali e basati sul contesto reale.

## Principio

CuePilot non risponde all'interlocutore.

CuePilot suggerisce all'utente cosa potrebbe dire.

## Input

- system instructions;
- profilo utente opzionale;
- project context;
- knowledge retrieval;
- recent conversation;
- last relevant message;
- answer style.

## Output

Schema consigliato:

```json
{
  "answer": "Possiamo gestirlo attraverso...",
  "style": "NORMAL",
  "confidence": 0.84,
  "knowledge_used": true
}
```

## Answer styles

### SHORT
1-2 frasi.

### NORMAL
Risposta parlata concisa.

### TECHNICAL
Più dettagli tecnici ma ancora pronunciabili durante una call.

## Regole

- non inventare dettagli;
- usare knowledge base quando disponibile;
- non mostrare chain-of-thought;
- evitare markdown complesso nell'overlay;
- evitare prefazioni;
- privilegiare linguaggio parlato.

## Provider abstraction

L'app deve poter cambiare modello senza modificare Conversation Engine e UI.

## Cost control

Ottimizzazioni future:
- modello piccolo per intent;
- modello più capace solo per answer generation;
- token budget;
- caching contesto;
- summary incrementale.
