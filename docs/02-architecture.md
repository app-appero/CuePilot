# 02 — Architecture

## Architettura generale

```text
Call application
      |
      +--> System Audio ----+
      |                     |
      +--> Microphone ------+--> Audio Engine
                                  |
                                  v
                           Transcription Layer
                                  |
                                  v
                           Conversation Engine
                                  |
                     +------------+------------+
                     |                         |
                     v                         v
              Knowledge Retrieval         Intent Engine
                     |                         |
                     +------------+------------+
                                  |
                                  v
                              LLM Layer
                                  |
                                  v
                          Suggestion Engine
                                  |
                                  v
                          Desktop Overlay
```

## Componenti

### Desktop application
Stack:
- Tauri;
- React;
- TypeScript.

Responsabilità:
- UI;
- settings;
- device selection;
- overlay;
- session controls;
- hotkeys;
- system tray;
- rendering transcript/suggestions.

### Backend locale
Stack:
- Python;
- FastAPI.

Responsabilità:
- orchestrazione audio;
- trascrizione;
- conversation state;
- intent classification;
- LLM;
- retrieval;
- storage.

## Comunicazione

Prima scelta:
- HTTP/WebSocket locale tra desktop e backend.

Possibile evoluzione:
- IPC nativo.

## Moduli backend

```text
backend/app/
├── api/
├── audio/
├── transcription/
├── conversation/
├── ai/
├── knowledge/
├── storage/
├── models/
├── config/
└── main.py
```

## Provider abstraction

### STT

```python
class TranscriptionProvider:
    async def transcribe_chunk(self, audio_chunk): ...
```

Provider possibili:
- OpenAI;
- Whisper locale;
- Deepgram;
- Azure.

### LLM

```python
class LLMProvider:
    async def generate(self, request): ...
```

## Storage

SQLite per:
- settings non sensibili;
- projects;
- document metadata;
- session summaries;
- opzionalmente transcript.

Non salvare API key in chiaro nel DB se evitabile.

## Event model

Eventi principali:

```text
audio.microphone.chunk
audio.system.chunk
speech.segment.started
speech.segment.completed
transcript.partial
transcript.final
conversation.intent
suggestion.requested
suggestion.generated
session.started
session.ended
```

## Principio

I moduli devono comunicare tramite contratti chiari e non tramite dipendenze circolari.
