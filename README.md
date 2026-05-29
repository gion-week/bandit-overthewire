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
| [Level 0](./level-00/level-00-README.md) | Connessione SSH, lettura file | ✅ |
| [Level 1](./level-01/level-01-README.md) | File con nome `-`, percorso relativo vs stdin | ✅ |
| Level 2 | — | ⬜ |
| Level 3 | — | ⬜ |
| Level 4 | — | ⬜ |
| Level 5 | — | ⬜ |
| Level 6 | — | ⬜ |
| Level 7 | — | ⬜ |
| Level 8 | — | ⬜ |
| Level 9 | — | ⬜ |
| Level 10 | — | ⬜ |
| Level 11 | — | ⬜ |
| Level 12 | — | ⬜ |
| Level 13 | — | ⬜ |
| Level 14 | — | ⬜ |
| Level 15 | — | ⬜ |
| Level 16 | — | ⬜ |
| Level 17 | — | ⬜ |
| Level 18 | — | ⬜ |
| Level 19 | — | ⬜ |
| Level 20 | — | ⬜ |
| Level 21 | — | ⬜ |
| Level 22 | — | ⬜ |
| Level 23 | — | ⬜ |
| Level 24 | — | ⬜ |
| Level 25 | — | ⬜ |
| Level 26 | — | ⬜ |
| Level 27 | — | ⬜ |
| Level 28 | — | ⬜ |
| Level 29 | — | ⬜ |
| Level 30 | — | ⬜ |
| Level 31 | — | ⬜ |
| Level 32 | — | ⬜ |
| Level 33 | — | ⬜ |

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
