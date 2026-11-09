# Books

Repository privat pentru cartile publicate si in lucru.

## Structura folderelor

```
books/
├── README.md                  # acest fisier
├── amazon-kdp/                # cartile self-publicate pe Amazon KDP
│   ├── manuscripts/           # manuscrisele finale (fisiere sursa, fara versiuni temporare)
│   ├── covers/                # coperte si fisiere sursa pentru coperte
│   ├── metadata/              # titluri, descrieri, categorii, preturi, ISBN-uri
│   └── marketing/             # texte promotionale, campanii, note de lansare
├── luca-series/               # versiunile ilustrate ale seriei Luca
│   ├── stories/               # textele povestilor din serie
│   ├── illustrations/         # ilustratii si fisiere sursa
│   ├── audio/                 # versiunile audio
│   └── print-layouts/         # machete pentru tiparire si export
└── docs/
    └── processes/             # pasi repetabili: publicare KDP, export, verificari
```

## Conventii

- Un folder pentru fiecare titlu sau serie, cu numele in format `kebab-case`.
- Fisierele de lucru mari (PSD, InDesign, audio brut) se pastreaza in afara repo-ului sau prin Git LFS.
- Fiecare carte publicata are o intrare in `amazon-kdp/metadata/` cu data publicarii si versiunea trimisa.
- Documentatia noua se adauga in folderul corespunzator, nu in radacina.

## Repository

Privat.
