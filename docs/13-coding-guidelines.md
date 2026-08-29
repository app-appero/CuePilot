# 13 — Coding Guidelines

## Generale

- preferire semplicità;
- evitare over-engineering;
- niente dipendenze senza necessità;
- componenti piccoli;
- contratti espliciti;
- error handling;
- niente magic values non documentati.

## TypeScript

- strict mode;
- evitare `any`;
- tipi condivisi per API;
- componenti React piccoli;
- logica business fuori dai componenti UI.

## Python

- type hints;
- async quando necessario;
- Pydantic per contratti API;
- eccezioni specifiche;
- niente global state incontrollato.

## FastAPI

Endpoint raggruppati per dominio.

Esempio:

```text
/api/health
/api/audio/*
/api/session/*
/api/settings/*
```

WebSocket per eventi realtime quando necessario.

## Naming

- classi: PascalCase;
- funzioni/variabili: convenzione linguaggio;
- task: `CP-NNN`;
- eventi: `domain.event`.

## Logging

Livelli:
- DEBUG;
- INFO;
- WARNING;
- ERROR.

Mai loggare:
- segreti;
- API key;
- raw audio;
- transcript completo per default.

## Testing

Priorità:
1. unit test per logica;
2. integration test API;
3. smoke test audio;
4. manual Windows test per device/overlay.

## Git

Commit piccoli e coerenti.

Non includere:
- `.env`;
- cache;
- build;
- DB locale reale;
- documenti personali.
