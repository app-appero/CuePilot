# 00 — Vision

## Nome progetto

CuePilot

## Visione

CuePilot è un assistente AI desktop personale che supporta l'utente durante call, meeting e conversazioni digitali.

Il sistema deve ascoltare la conversazione in tempo reale, comprenderne il contesto e mostrare suggerimenti testuali che l'utente possa leggere, adattare e pronunciare.

CuePilot non deve parlare al posto dell'utente e non deve partecipare alla call come bot.

## Problema

Durante call tecniche, commerciali o operative può essere necessario:
- ricordare informazioni;
- recuperare dettagli su un progetto;
- formulare rapidamente una risposta;
- gestire domande tecniche;
- rispondere a obiezioni;
- mantenere il filo di una conversazione lunga.

CuePilot deve ridurre questo carico cognitivo.

## Esperienza ideale

1. L'utente apre CuePilot.
2. Seleziona microfono e dispositivo audio.
3. Seleziona eventualmente il contesto/progetto.
4. Avvia la sessione.
5. CuePilot ascolta microfono e audio del PC.
6. Trascrive in tempo reale.
7. Identifica le frasi dell'utente e dell'interlocutore.
8. Comprende quando è necessaria una risposta.
9. Genera un suggerimento breve e naturale.
10. Mostra il suggerimento in un overlay sempre visibile.
11. L'utente decide se usarlo o ignorarlo.

## Principi di prodotto

### Personal-first
La prima versione è destinata a un solo utente.

### Desktop-only
La prima versione supporta Windows 11.

### Local-first
Configurazioni, storico e knowledge base devono essere locali quando possibile.

### No bot
CuePilot non deve comparire tra i partecipanti della call.

### Platform agnostic
Deve funzionare con Meet, Teams, Zoom, Discord, browser e altre app senza integrazioni specifiche.

### User in control
L'AI suggerisce. L'utente decide.

## Non-obiettivi iniziali

- SaaS;
- account;
- team;
- multiutente;
- sincronizzazione cloud;
- billing;
- mobile;
- marketplace;
- CRM;
- registrazione automatica obbligatoria;
- risposta vocale automatica;
- automazione della call.

## MVP

L'MVP è valido quando:

1. CuePilot gira su Windows 11.
2. Acquisisce microfono.
3. Acquisisce audio di sistema.
4. Trascrive entrambi.
5. Distingue ME e OTHER.
6. Rileva almeno le domande più comuni.
7. Genera un suggerimento testuale.
8. Mostra il suggerimento in overlay.
9. Supporta una hotkey manuale.
10. Mantiene il contesto delle ultime battute.
