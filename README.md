# OverTheWire – Bandit

Writeup personale dei livelli del wargame **Bandit** di [OverTheWire](https://overthewire.org/wargames/bandit/).

Bandit è pensato per chi si avvicina alla sicurezza informatica partendo da zero: insegna i fondamentali della command line Linux, la gestione di file, permessi, processi, rete e crittografia attraverso sfide pratiche in progressione.

---

## Struttura della repo

```
bandit-overthewire/
├── README.md          ← questo file
├── level-00/          ← Bandit Level 0 → 1
│   ├── README.md      ← writeup del livello
│   └── screenshots/   ← screenshot di supporto
├── level-01/          ← Bandit Level 1 → 2
│   └── ...
└── ...
```

Ogni cartella `level-XX` rappresenta la risoluzione del livello XX, ovvero i passi necessari per trovare la password che consente l'accesso al livello successivo (XX+1).

---

## Progressione

| Livello | Argomento principale | Completato |
|---------|----------------------|:----------:|
| [Level 0](./level-00/README.md) | Connessione SSH, lettura file | ✅ |
| [Level 1](./level-01/README.md) | File con nome `-`, percorso relativo vs stdin | ✅ |
| [Level 2](./level-02/README.md) | File con spazi nel nome, quoting e percorso relativo | ✅ |
| [Level 3](./level-03/README.md) | File nascosti, navigazione tra cartelle | ✅ |
| [Level 4](./level-04/README.md) | Tipi di file, comando `file`, wildcard `*` | ✅ |
| [Level 5](./level-05/README.md) | Comando `find`, ricerca per dimensione | ✅ |
| [Level 6](./level-06/README.md) | Ricerca su tutto il filesystem, criteri `find` combinati, stderr | ✅ |
| [Level 7](./level-07/README.md) | `grep`, `pipe`, ricerca in file di grandi dimensioni | ✅ |
| [Level 8](./level-08/README.md) | `sort`, `uniq -u`, righe uniche in un file | ✅ |
| [Level 9](./level-09/README.md) | `strings`, file binari, pipeline `grep` + `awk` | ✅ |
| [Level 10](./level-10/README.md) | Encoding Base64, decodifica con `base64 -d` | ✅ |
| [Level 11](./level-11/README.md) | Cifrario ROT13, comando `tr` | ✅ |
| [Level 12](./level-12/README.md) | Hexdump e decompressione file, `xdd`,`gzip`,`bzip2`,`tar` | ✅ |
| [Level 13](./level-13/README.md) | Autenticazione SSH con chiave privata, `scp`, modifica permessi con `chmod`  | ✅ |
| [Level 14](./level-14/README.md) | Connessione TCP con `telnet`, interazione con servizi di rete su porta locale | ✅ |
| [Level 15](./level-15/README.md) | Connessione SSL/TLS con `openssl s_client`, lettura del manuale | ✅ |
| [Level 16](./level-16/README.md) | Scansione porte e servizi con `nmap`, identificazione servizio SSL, chiave RSA come credenziale | ✅ |
| [Level 17](./level-17/README.md) | Confronto file con `diff` | ✅ |
| [Level 18](./level-18/README.md) | Esecuzione comandi remoti via SSH senza shell interattiva, .bashrc e tipi di shell | ✅ |
| [Level 19](./level-19/README.md) | Bit setuid, eseguibile con privilegi elevati, privilege escalation | ✅ |
| [Level 20](./level-20/README.md) | `tmux` e job control, processi concorrenti, `nc` in ascolto, command-line injection | ✅ |
| [Level 21](./level-21/README.md) | Cron e cronjob, lettura di script pianificati, `/etc/cron.d/` | ✅ |
| [Level 22](./level-22/README.md) | Analisi di script `cron`, hashing con `md5sum`, parsing con `cut` | ✅ |
| [Level 23](./level-23/README.md) | Scrittura di script per `cron`, analisi di script complessi, permessi per esecuzione cross-utente | ✅ |
| [Level 24](./level-24/README.md) | — | ✅ |
| [Level 25](./level-25/README.md) | — | ✅ |
| [Level 26](./level-26/README.md) | — | ✅ |
| [Level 27](./level-27/README.md) | — | ✅ |
| [Level 28](./level-28/README.md) | — | ✅ |
| [Level 29](./level-29/README.md) | — | ✅ |
| [Level 30](./level-30/README.md) | — | ✅ |
| [Level 31](./level-31/README.md) | — | ✅ |
| [Level 32](./level-32/README.md) | — | ✅ |
| [Level 33](./level-33/README.md) | — | ✅ |

---

## Ambiente di lavoro

I livelli sono stati risolti su una macchina virtuale con le seguenti caratteristiche:

| Componente | Dettaglio |
|------------|-----------|
| Hypervisor | VMware |
| OS | Ubuntu 25.10 |
| RAM | 6 GB |
| Disco | 25 GB |
| CPU | 2 core |

---

## Connessione al server

Il server di Bandit è raggiungibile via SSH sulla porta `2220`:

```bash
ssh bandit<N>@bandit.labs.overthewire.org -p 2220
```

Dove `<N>` è il numero del livello a cui si vuole accedere. La password di ogni livello è la soluzione del livello precedente (ad eccezione del level 0, la cui password è `bandit0`).

---

## Note

- Le password trovate **non vengono pubblicate** nei writeup per rispetto delle linee guida di OverTheWire.
- I writeup descrivono il ragionamento e i comandi usati, non la soluzione letterale.
- Ogni livello include i comandi rilevanti e, dove utile, screenshot del terminale.
