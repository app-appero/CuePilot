# 12 — Definition of Done

Un task è completato solo se:

1. Lo scope richiesto è implementato.
2. Non sono state aggiunte feature fuori scope senza necessità.
3. Il codice compila.
4. I test pertinenti passano.
5. TypeScript strict non presenta errori.
6. Il codice Python è tipizzato nelle API pubbliche.
7. Gli errori comuni sono gestiti.
8. Non sono presenti segreti nel repository.
9. La documentazione viene aggiornata se l'architettura cambia.
10. L'AI coding assistant riporta:
   - file modificati;
   - test eseguiti;
   - problemi aperti;
   - eventuali decisioni tecniche.

## Definition of Done MVP

Il prodotto MVP è completato quando un test reale soddisfa:

1. CuePilot viene aperto su Windows 11.
2. L'utente seleziona microfono e output.
3. Avvia la sessione.
4. Interlocutore parla tramite una call.
5. CuePilot acquisisce l'audio.
6. Trascrive correttamente una domanda.
7. La domanda viene classificata come risposta necessaria.
8. Il modello riceve il contesto.
9. Una risposta utile viene generata.
10. L'overlay la mostra.
11. La risposta successiva considera il contesto precedente.
12. La hotkey permette di generare manualmente.
13. La sessione può essere terminata senza crash.
