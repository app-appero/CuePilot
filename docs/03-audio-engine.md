# 03 — Audio Engine

## Obiettivo

Acquisire due sorgenti indipendenti:

1. microfono dell'utente;
2. audio riprodotto dal computer.

## Speaker mapping

```text
Microphone -> ME
System loopback -> OTHER
```

Questo mapping è valido per l'MVP.

## Windows audio

Target:
- Windows 11;
- WASAPI.

Per l'audio di sistema utilizzare WASAPI loopback.

## Requisiti

### AE-001
Enumerare dispositivi input.

### AE-002
Enumerare dispositivi output.

### AE-003
Selezionare device.

### AE-004
Start capture.

### AE-005
Stop capture.

### AE-006
Gestire device unavailable.

### AE-007
Bufferizzare chunk audio.

### AE-008
Associare source metadata.

Esempio:

```json
{
  "source": "ME",
  "sample_rate": 16000,
  "channels": 1,
  "timestamp": 123.45
}
```

## Voice Activity Detection

Obiettivo:
- evitare invio continuo di silenzio;
- identificare segmenti vocali;
- determinare fine frase con timeout configurabile.

## VU Meter

La UI deve mostrare il livello del microfono per facilitare setup e debug.

## Failure cases

- microfono scollegato;
- output cambiato durante call;
- device occupato;
- permessi negati;
- sample rate incompatibile.

Nessuno di questi eventi deve terminare brutalmente l'app.
