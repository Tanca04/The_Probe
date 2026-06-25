# The Probe — pacchetto Axure-ready

## Struttura consigliata in Axure

Crea queste pagine:

1. `01_Home_Missione`
2. `02_Check_Prevolo`
3. `03_Missione_Attiva`
4. `04_AI_Agent`
5. `05_Controllo_Braccia`
6. `06_Warning_Sicurezza`
7. `07_Archivio_Missioni`

## Dynamic panel consigliati

- `DP_ModeSwitch`: stati Manuale / Assistito / Automatico.
- `DP_PreflightStatus`: stato OK / stato critico.
- `DP_AICommand`: input vocale / input testuale / conferma comando.
- `DP_ArmControl`: manuale braccia / presa assistita / conferma presa.
- `DP_WarningModal`: ostacolo / persona / batteria bassa / connessione instabile.

## Interazioni principali da impostare

- Home: click su profilo missione → `02_Check_Prevolo` con variabile `MissionProfile`.
- Check pre-volo: se batteria, carico, sensori o connessione sono critici → disabilita `Avvia missione` e mostra motivo.
- Missione attiva: `AI Agent` → `04_AI_Agent`; `Braccia` → `05_Controllo_Braccia`; `Warning` → `06_Warning_Sicurezza`.
- AI Agent: per azioni critiche mostra comando interpretato e conferma; `Takeover manuale` torna sempre a `03_Missione_Attiva`.
- Braccia: abilita controllo braccia solo se `Stable = true`; `Presa assistita` mostra conferma umana prima della chiusura.
- Warning: mostra le 3 CTA: `Accetta deviazione`, `Manuale`, `Stop/Hover`.
- Archivio: filtri per data, profilo, luogo, tag e tipo dati.
