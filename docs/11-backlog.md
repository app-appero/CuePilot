# 11 — Backlog

Legenda priorità:
- P0: fondamentale;
- P1: importante;
- P2: successivo;
- P3: idea futura.

| ID | Task | Priority | Dependency | Acceptance criteria |
|---|---|---:|---|---|
| CP-001 | Repository structure | P0 | - | Struttura conforme docs |
| CP-002 | Tauri React TS bootstrap | P0 | CP-001 | App Windows avviabile |
| CP-003 | FastAPI bootstrap | P0 | CP-001 | Backend avviabile |
| CP-004 | Health endpoint | P0 | CP-003 | `/health` ritorna OK |
| CP-005 | Frontend backend status | P0 | CP-004 | UI mostra stato |
| CP-101 | Enumerate microphones | P0 | CP-003 | Lista device reale |
| CP-102 | Select microphone | P0 | CP-101 | Device persistito in sessione |
| CP-103 | Capture microphone | P0 | CP-102 | Audio chunk ricevuti |
| CP-104 | VU meter | P1 | CP-103 | UI reagisce alla voce |
| CP-201 | Enumerate outputs | P0 | CP-003 | Lista output reale |
| CP-202 | WASAPI loopback | P0 | CP-201 | Audio PC catturato |
| CP-203 | Dual capture | P0 | CP-103, CP-202 | Stream contemporanei |
| CP-204 | Tag ME/OTHER | P0 | CP-203 | Chunk sorgente corretta |
| CP-301 | STT abstraction | P0 | CP-203 | Provider intercambiabile |
| CP-302 | STT ME | P0 | CP-301 | Trascrive microfono |
| CP-303 | STT OTHER | P0 | CP-301 | Trascrive sistema |
| CP-304 | Final transcript model | P0 | CP-302, CP-303 | Eventi consistenti |
| CP-305 | Live transcript UI | P1 | CP-304 | Testo visibile realtime |
| CP-401 | Conversation history | P0 | CP-304 | Ultime battute disponibili |
| CP-402 | Intent classification | P0 | CP-401 | Classificazione valida |
| CP-403 | requires_answer | P0 | CP-402 | Booleano affidabile |
| CP-404 | Context builder | P0 | CP-401 | Token budget rispettato |
| CP-405 | Manual hotkey trigger | P1 | CP-404 | Forza suggestion |
| CP-501 | LLM abstraction | P0 | CP-404 | Provider intercambiabile |
| CP-502 | Suggestion generation | P0 | CP-501 | Answer restituita |
| CP-503 | Styles | P1 | CP-502 | Short/Normal/Technical |
| CP-504 | Regenerate | P1 | CP-502 | Nuova risposta |
| CP-601 | Overlay | P0 | CP-502 | Always-on-top |
| CP-602 | Compact mode | P1 | CP-601 | UI ridotta |
| CP-603 | Global hotkey | P1 | CP-405 | Funziona fuori app |
| CP-701 | Projects | P2 | CP-001 | CRUD locale minimo |
| CP-702 | Import docs | P2 | CP-701 | Import file supportati |
| CP-703 | Parse docs | P2 | CP-702 | Testo estraibile |
| CP-704 | Embeddings | P2 | CP-703 | Chunk indicizzati |
| CP-705 | Retrieval | P2 | CP-704 | Top-k rilevanti |
| CP-706 | LLM KB context | P2 | CP-705, CP-502 | Answer usa knowledge |
| CP-801 | Session summary | P2 | CP-401, CP-501 | Summary generato |
| CP-901 | Packaging | P1 | MVP | Installer Windows |
