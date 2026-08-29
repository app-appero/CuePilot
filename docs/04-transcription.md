# 04 — Realtime Transcription

## Obiettivo

Trasformare segmenti audio in testo con latenza ridotta.

## Output minimo

```json
{
  "speaker": "OTHER",
  "text": "Come gestireste il database?",
  "is_final": true,
  "started_at": 12.1,
  "ended_at": 14.7
}
```

## Provider abstraction

Il Conversation Engine non deve conoscere il provider STT concreto.

## Partial vs Final

Supportare quando disponibile:
- partial transcript;
- final transcript.

Solo i transcript final devono entrare stabilmente nella conversation history.

## Lingua

V1:
- italiano prioritario;
- possibilità di auto-detection se supportata.

## Normalizzazione

Prima dell'invio al Conversation Engine:
- trim;
- rimozione duplicati evidenti;
- normalizzazione spazi;
- mantenimento punteggiatura utile.

## Error handling

In caso di errore provider:
- retry limitato;
- stato UI;
- nessun crash;
- possibilità di continuare sessione.

## Metriche interne utili

- latency audio-to-final-text;
- segment duration;
- transcription failures;
- retry count.
