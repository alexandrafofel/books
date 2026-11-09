# Workflow Jira si documentatie

Document comun pentru proiectele CRA Desk, Books si Supplier Trust Desk. Fiecare proiect are propriul proiect Jira si propriul repo git.

## Statusuri

| Status | Cine il pune | Cand |
|---|---|---|
| To Do | Claude | La crearea tichetului |
| Ready | Alexandra | Dupa verificarea tichetului. Claude nu incepe un ticket fara Ready. |
| In Progress | Claude | Imediat ce incepe lucrul |
| In Review | Claude | Dupa ce documentatia e in git, comentariul final e scris si follow-up-urile sunt create |

## Naming

Format: `[PROIECT][Categorie][SubCategorie][Nume-scurt]`

Exemplu: `[CRA][Decide][Niche][Niche-and-ICP]`

- PROIECT: cheia proiectului Jira (CRA, BOOKS sau SUP, dupa cum e configurat)
- Categorie: Decide, Build, Validate, Launch etc.
- SubCategorie: zona de lucru in cadrul categoriei
- Nume-scurt: 2 pana la 4 cuvinte in kebab-case

## Structura unui tichet

Fiecare tichet are aceste sectiuni in descriere:

1. **Context**: de ce exista tichetul, legat de ce epic sau obiectiv.
2. **Scop**: rezultatul concret.
3. **Actiune**: ce trebuie facut.
4. **Dependente**: ce trebuie sa fie gata inainte (before) si ce deblocheaza tichetul (after). Fiecare dependenta apare si ca link Jira.
5. **DoR (Definition of Ready)**: ce trebuie sa fie adevarat inainte sa inceapa lucrul.
6. **Acceptance Criteria**: conditiile de acceptare. Include mereu documentatia in git. Daca lucrul cere alte tichete (improvements sau bugs), acestea trebuie create si listate.
7. **Definition of Done**: include mereu documentatia in git, comentariul final pe Jira si crearea tichetelor follow-up daca exista.

Campurile existente (model recomandat, estimare) se pastreaza.

## Dependente

- In descriere: `Depinde de: CRA-X (before)` si `Deblocheaza: CRA-Y (after)`.
- In Jira: link de tip "is blocked by" sau "blocks", in aceeasi directie.

## Cand Claude incepe un ticket

1. Verifica ca tichetul e in Ready. Daca nu, nu incepe.
2. Muta tichetul in In Progress.
3. Lucreaza pe acceptance criteria.

## Cand Claude termina un ticket

1. Scrie documentatia in repo-ul proiectului, in folderul potrivit, cu numele `<CHEIE>-<slug>.md`. Exemplu: `docs/niche/CRA-7-niche-and-icp.md`.
2. Face commit cu cheia tichetului in mesaj, de exemplu `CRA-7: niche and ICP`.
3. Creeaza tichetele follow-up (improvements sau bugs) cu toate sectiunile de mai sus, in To Do.
4. Scrie un comentariu final pe tichet, cu linkul la fisierul din git.
5. Muta tichetul in In Review. Alexandra verifica si muta in Done.

## Reguli generale

- Un tichet nu are apeluri, outreach la rece sau sesiuni live daca proiectul spune asta (regula din epicul CRA-1).
- Estimarile proprii se marcheaza ca estimari.
