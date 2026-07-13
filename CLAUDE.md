# CraversBest — Shopify store (Claude Code notes)

CraversBest is a small-batch **snacks** brand (sweet · salty · spicy). This repo is a customized **Shopify Dawn** theme (v15.5.0 base) plus store content in `store/`.

## Tooling
- **Shopify CLI** (`shopify theme dev/check/push`) — run from repo root; the repo root IS the theme.
- **Shopify Dev MCP** (`shopify-dev` in `.mcp.json`) — use it liberally:
  - Before changing Liquid or theme JSON, `validate_theme` / `validate_theme_codeblocks`.
  - For any Shopify API/Liquid question, `learn_shopify_api` then `search_docs` — don't guess Liquid or section-schema shapes.
  - `introspect_graphql_schema` before writing Admin/Storefront GraphQL.

## Conventions
- **Theme = design + templates only.** Products, collections, pages, menus, and policies live in the store DB — author them under `store/` and load via CSV import / admin, never hard-code catalog data into Liquid.
- **Homepage** is `templates/index.json`. Section/block `type`s must match files in `sections/` and their `{% schema %}` — verify block types against the schema before editing.
- **Brand** lives in `config/settings_data.json` (`current` object): Crave Red `#D62F27`, Espresso `#231A15`, Golden `#F5A623`, Cream `#FFF7EE`; Poppins headings + Assistant body; pill buttons, 16px rounded cards, drawer cart. Keep new sections on this system via the 5 color schemes.
- After editing theme JSON/Liquid, run `shopify theme check` — expect only the ~8 pre-existing Dawn orphaned-snippet warnings; anything new is yours.

## Don't
- Don't publish to a live theme without an explicit ask (`--allow-live`). `shopify theme dev` is safe (private preview).
- Don't commit secrets. Store tokens go in `.env` (git-ignored); never in `.mcp.json` or theme files.
