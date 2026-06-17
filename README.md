# Temple of the Elemental Evil — Patch ITA Merchant Dialog Fix

Correzione bug dialogo mercanti • Patch ITA v5.0.4

## Il problema

Nella patch italiana **v5.0.4** di Temple of the Elemental Evil (disponibile su [OldGamesItalia](https://oldgamesitalia.net/traduzioni/tempio-del-male-elementale)) è presente un bug nei messaggi di dialogo con i mercanti.

- Un personaggio **maschio** chiede di commerciare con un mercante **maschio**.
- Nel party è presente almeno un NPC.
- Invece del messaggio corretto (*"Aspetta che finisca di servire questi altri clienti"*) appare un errore di **messaggio mancante**.

## Causa

Nel file `Temple of Elemental Evil/data/mes/gd_npc_m2m.mes`, alla riga 126, manca una parentesi graffa iniziale che rompe il formato del messaggio e la lettura dei messaggi successivi:

```
- 3600}{All'ultimo sangue!}
+ {3600}{All'ultimo sangue!}
```

## La correzione

Sostituire la riga 126 del file `gd_npc_m2m.mes` con:

```
{3600}{All'ultimo sangue!}
```

### Istruzioni rapide

1. Scaricare ed installare il gioco e attivare la versione legacy
2. Scaricare ed intallare la patch ITA v5.0.4 da OldGamesItalia.
2. Aprire il file `Temple of Elemental Evil/data/mes/gd_npc_m2m.mes` con un editor di testo.
3. Andare alla riga 126 e  aggiungere la parentesi graffa all'inizio della riga.
4. Salvare il file. Il bug è risolto.

---

Fix non ufficiale • Patch ITA originale a cura di OldGamesItalia
