# 09 — Privacy & Security

## Principio

Privacy by default.

## Default consigliati

```text
Save raw audio: OFF
Save transcript: OFF
Save summary: OFF/ASK
Telemetry: OFF
```

## Audio

L'audio deve preferibilmente:
1. entrare in buffer;
2. essere elaborato;
3. essere eliminato.

## Transcript

La trascrizione può restare in RAM durante la call.

Persistenza solo se esplicitamente abilitata.

## API keys

- mai nel repository;
- `.env` escluso da Git;
- `.env.example` senza valori;
- valutare Windows Credential Manager nelle versioni successive.

## Logs

Non inserire nei log:
- API key;
- audio raw;
- transcript completo;
- documenti sensibili.

## Network

Documentare chiaramente quando:
- audio lascia il PC;
- testo lascia il PC;
- documenti vengono inviati a provider esterni.

## Reminder

L'utente è responsabile dell'utilizzo conforme alle regole applicabili alle conversazioni e alla registrazione/trascrizione di terzi.
