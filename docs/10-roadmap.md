# 10 — Roadmap

## Milestone 0 — Foundation

Obiettivo:
repository, documentazione, desktop shell, backend health.

Task:
- CP-001 struttura repo;
- CP-002 Tauri + React;
- CP-003 FastAPI;
- CP-004 `/health`;
- CP-005 config;
- CP-006 docs baseline.

Exit criteria:
desktop e backend avviabili localmente.

---

## Milestone 1 — Microphone

Obiettivo:
acquisizione microfono affidabile.

Task:
- CP-101 device enumeration;
- CP-102 device selection;
- CP-103 start/stop capture;
- CP-104 VU meter;
- CP-105 error handling.

Exit criteria:
microfono selezionabile e livello audio visibile.

---

## Milestone 2 — System Audio

Obiettivo:
cattura audio PC tramite WASAPI loopback.

Task:
- CP-201 output enumeration;
- CP-202 loopback capture;
- CP-203 dual source;
- CP-204 source tagging;
- CP-205 device recovery.

Exit criteria:
ME e OTHER acquisiti separatamente.

---

## Milestone 3 — Realtime STT

Task:
- CP-301 provider interface;
- CP-302 STT microfono;
- CP-303 STT system;
- CP-304 partial/final;
- CP-305 live transcript.

Exit criteria:
dialogo visibile in UI con ME/OTHER.

---

## Milestone 4 — Conversation Intelligence

Task:
- CP-401 history;
- CP-402 intent;
- CP-403 requires_answer;
- CP-404 context window;
- CP-405 manual trigger.

Exit criteria:
CuePilot sa quando richiedere una risposta.

---

## Milestone 5 — AI Suggestions

Task:
- CP-501 LLM provider;
- CP-502 answer prompt;
- CP-503 answer styles;
- CP-504 regenerate;
- CP-505 error/cancel;
- CP-506 latency instrumentation.

Exit criteria:
domanda reale -> suggerimento utile.

---

## Milestone 6 — Overlay

Task:
- CP-601 always-on-top;
- CP-602 compact mode;
- CP-603 hotkey;
- CP-604 reposition;
- CP-605 live status.

Exit criteria:
utilizzabile durante Meet/Teams senza cambiare finestra.

---

## Milestone 7 — Knowledge Base

Task:
- CP-701 projects;
- CP-702 document import;
- CP-703 parsing;
- CP-704 embeddings;
- CP-705 retrieval;
- CP-706 project context.

Exit criteria:
risposte basate sui documenti selezionati.

---

## Milestone 8 — Session Summary

Task:
- CP-801 stop workflow;
- CP-802 summary;
- CP-803 decisions;
- CP-804 tasks;
- CP-805 optional persistence.

---

## Milestone 9 — Hardening

- latency;
- memory;
- reconnect;
- audio device switch;
- provider fallback;
- cancellation;
- crash recovery.

---

## Milestone 10 — Distribution

- Tauri build;
- backend packaging;
- installer;
- first-run;
- configuration;
- Windows smoke test.
