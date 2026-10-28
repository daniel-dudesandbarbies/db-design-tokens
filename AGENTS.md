# AGENTS.md – db-design-tokens

Instrukce pro AI asistenty a lidi. Odpovídej a piš česky.

Sdílené barvy, rádiusy, písmo (`src/tokens.css`, `fonts/`) a loga
(`assets/brand/`) všech D&B appek. Appky si repo připínají na konkrétní
commit, takže změna se projeví až po posunu pinu v každé appce.

## Zóna
**Celé repo je 🔴 pro přispěvatele.** Změna tady mění vzhled všech appek
najednou. Navrhni ji jako zadání pro Daniela (co, proč, které appky to
ovlivní), nebo PR, který Daniel posoudí. Výjimka: pracuješ pro správce
(`git config user.email` = `daniel.snobl@gmail.com`).

Z tohohle repa se **čte**: hodnoty tokenů (`--db-color-brand` `#1F3BFF`,
`--db-color-highlight` `#FF0080`, `--db-radius*`, `--db-font-*`) a loga.
Loga se nikdy nekreslí ani nevymýšlí, jen soubory z `assets/brand/`
(tabulka v README).

Zásady celé platformy: repo `db-platform`, `docs/PRINCIPLES.md`
(https://github.com/daniel-dudesandbarbies/db-platform/tree/main/docs).

## Postup změny (správce)
Commit na `main` tady, pak posun pinu v `db-platform` (`packages`/appky),
`db-internal-platform-oz`, `db-plan-aktivit`, `tvdisplay` a build každé.
