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

Písmo je **Poppins** hostovaný v repu (`fonts/`, řezy 300/400/700/800),
nadpisy ExtraBold verzálkami. Brandmanuálový Solomon Sans Bold je licenčně
nedostupný; swap by se dělal jen v `src/tokens.css` (`@font-face`
+ `--db-font-heading`).

## Loga a ikony

`assets/brand/` je jediný zdroj log a brand ikon. Loga se nikdy nekreslí
ani nevymýšlí, jen se použije (případně ořízne / zmenší) soubor odtud.

| Soubor | Použití |
|---|---|
| `D&B_logo_online_-13.png` | bílý wordmark (na modré hlavičce) |
| `D&B_logo_online_-08.png`, `-12.png` | další varianty wordmarku |
| `db_internal_rounded.svg` | favikona a PWA ikony všech appek |
| `favicon.svg`, `favicondbsystem.svg` | starší favikony |
| `sytemfavi.svg`, `tvicon.svg`, `tvicon2.svg` | TV admin |
| `backico.svg` | šipka zpět (`BackIcon` v `@db/shell`) |
| `sharedico.svg` | sdílené složky na homepage |
| `boticon.png`, `slackboticon.svg` | Slack bot |

Appka si potřebný soubor zkopíruje do svého `public/`, nebo ho importuje
přes `@db/design-tokens/assets/brand/<soubor>`.

## Instalace odjinud

```json
"@db/design-tokens": "github:daniel-dudesandbarbies/db-design-tokens"
```

## Změna tokenu

Commit + push sem, pak bump verze/ref závislosti v každém konzumentovi
(`db-platform`, `db-internal-platform`, ...) — žádné živé workspace
linkování mezi repy.
