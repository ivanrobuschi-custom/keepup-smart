---
title: "KeepUp Smart - Manuale Ristorante"
date: "2025-06-25"
categoria: software KeepUp Smart
---

# KeepUp Smart — Portale Documentale Ristorante

Benvenuto nel portale documentale di **KeepUp Smart**, il sistema di cassa e gestione ordini sviluppato da Custom S.p.A. per la ristorazione.

Questo manuale illustra la configurazione e l'utilizzo completo del sistema nella versione demo per ristorante, composta da due applicazioni principali che lavorano in sinergia:

| Applicazione | Ruolo | Dispositivo |
|---|---|---|
| **KeepUp Smart** | Cassa principale, programmazione, statistiche | Android (BlueStacks / terminale fisso) |
| **KeepUp Order** | Palmare cameriere, inserimento ordini al tavolo | Smartphone / tablet Android |

---

## Sezioni del manuale

### KeepUp Smart (Cassa)

- [Interfaccia principale](pos-interfaccia.md) — schermata di vendita, categorie articoli e tasti funzione
- [Programmazione articoli](pos-articoli.md) — creazione e modifica PLU, reparti, stampanti di produzione
- [Programmazione sale](pos-sale.md) — configurazione sale e assegnazione stampanti per reparto
- [Gestione operatori](pos-operatori.md) — permessi e profili utente
- [Stampanti fiscali](pos-stampanti.md) — configurazione registratori di cassa e stampanti comanda
- [Statistiche e report](pos-statistiche.md) — giacenza di cassa, venduto per articolo, operatore, reparto
- [Impostazioni avanzate](pos-impostazioni.md) — configurazione base dispositivo, timeout, password programma
- [Archivi](pos-archivi.md) — menu principale degli archivi (operatori, sale, tavoli, articoli, menu, buoni pasto)

### KeepUp Order (Palmare cameriere)

- [Schermata principale](order-home.md) — funzioni disponibili dal palmare
- [Gestione tavoli](order-tavoli.md) — mappa sale, stato occupazione tavoli, legenda colori
- [Inserimento ordini](order-inserimento.md) — presa comanda al tavolo con categorie e articoli
- [Sincronizzazione](order-sync.md) — download database dalla stazione centrale
- [Configurazione palmari](order-configurazione.md) — abbinamento dispositivi, indirizzo IP, Super User

### Amministrazione

- [Gestione licenze](licenze.md) — portale custom4u per attivazione e gestione licenze KeepUp Smart
- [Gestione Monopoli](monopoli.md) — configurazione vendita prodotti monopolio (tabacchi)

---

## Architettura del sistema

```
Stazione Centrale (KeepUp Smart)
         │  IP: 10.0.2.15 / 10.10.62.8
        │
        ├── Stampante Fiscale principale  (10.10.62.8)
        ├── Stampante Fiscale KeepUp Order (192.10.10.15)
        │
        └── Rete LAN / Wi-Fi
                │
                ├── Palmare 1 (KeepUp Order) — Configurazione: Seconda cassa
                └── Palmare 2 (KeepUp Order) — Configurazione: Order classico
```

!!! tip "Versione software"
    La versione documentata in questo manuale è **v.86.31 db 201** (demo del 25 giugno 2025).

!!! note "Video dimostrativo"
    Il video originale `Demo_kus_Risto_sdg.mp4` (56 minuti) illustra la configurazione completa del sistema. Per ospitarlo su GitHub Pages usa **Git LFS** oppure caricalo su **GitHub Releases** e aggiorna il path nel file `order-home.md`.
