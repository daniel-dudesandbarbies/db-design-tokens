# @db/design-tokens

Jediný zdroj pravdy pro D&B brand barvy a typografii (CSS custom
properties) — sdílené napříč celým D&B ekosystémem (`db-platform` monorepo
i externí appky mimo něj, jako `db-internal-platform`).

Hodnoty vycházejí z D&B brandmanuálu (barevnost 03.4, typografie 03.7).

## Použití

```js
import '@db/design-tokens/tokens.css'
```

Importovat před appka-specifickým CSS. Proměnné: `--db-color-bg`,
`--db-color-fg`, `--db-color-border`, `--db-color-muted`,
`--db-color-error`, `--db-color-success`, `--db-color-accent` (+
`--db-color-secondary-*`), `--db-font-heading`, `--db-font-body` (a jejich
`-weight` varianty). Dark mode přes `prefers-color-scheme`.

Nadpisový font je dočasně **Plus Jakarta Sans** — stand-in za licencovaný
Solomon Sans Bold z brandmanuálu, dokud nejsou k dispozici jeho soubory.
Swap se dělá jen v `src/tokens.css` (`@import` + `--db-font-heading`),
nic downstream se měnit nemusí.

## Instalace odjinud

```json
"@db/design-tokens": "github:daniel-dudesandbarbies/db-design-tokens"
```

## Změna tokenu

Commit + push sem, pak bump verze/ref závislosti v každém konzumentovi
(`db-platform`, `db-internal-platform`, ...) — žádné živé workspace
linkování mezi repy.
