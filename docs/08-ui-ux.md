# 08 — UI/UX

## Principio

Durante una call l'interfaccia deve essere leggibile in meno di un secondo.

## Schermate

### Home
- stato backend;
- microfono;
- output audio;
- progetto;
- tipo risposta;
- Start Call.

### Live Session
- stato listening;
- ultima trascrizione OTHER;
- suggestion;
- pulsanti style;
- regenerate;
- stop.

### Settings
- devices;
- provider;
- hotkey;
- privacy;
- persistence.

### History
Post-MVP.

## Overlay

Requisiti:
- always-on-top;
- ridimensionabile;
- compatto;
- posizionabile;
- non invasivo.

Contenuto minimo:

```text
● LISTENING

Domanda:
Come gestireste...

SUGGERIMENTO
Possiamo...

[Breve] [Tecnica] [Rigenera]
```

## Hotkey

Default candidato:
`CTRL + SHIFT + SPACE`

Funzione:
genera un suggerimento manuale dall'ultimo contesto disponibile.

## Stati UI

- IDLE;
- STARTING;
- LISTENING;
- TRANSCRIBING;
- GENERATING;
- ERROR;
- STOPPED.

## Errori

Mostrare errori brevi e azionabili.
Non usare stack trace in UI.
