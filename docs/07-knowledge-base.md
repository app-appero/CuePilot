# 07 — Knowledge Base

## Obiettivo

Permettere a CuePilot di generare risposte basate su informazioni reali dell'utente.

## Struttura concettuale

```text
Projects
├── General
├── Project A
├── Project B
└── Project C
```

Ogni progetto può avere:
- markdown;
- txt;
- PDF;
- JSON;
- note manuali.

## Workflow

1. L'utente crea/seleziona progetto.
2. Associa documenti.
3. Il sistema indicizza i contenuti.
4. Durante la call recupera solo chunk rilevanti.
5. I chunk vengono passati al LLM.

## V1

Evitare infrastruttura eccessiva.

Preferenze:
- storage locale;
- embeddings locali o API;
- SQLite + estensione vector se adeguata.

## Metadata

Ogni chunk dovrebbe conoscere:
- document_id;
- project_id;
- filename;
- page/section quando disponibile;
- updated_at.

## Regole retrieval

- retrieval solo sul progetto selezionato;
- General può essere incluso opzionalmente;
- limitare numero chunk;
- non usare documenti non rilevanti;
- riportare internamente la provenienza.

## Privacy

I documenti non devono essere caricati permanentemente su servizi esterni salvo esplicita scelta dell'utente.
