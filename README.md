# CraversBest — Shopify Store

A complete Shopify storefront for **CraversBest**, a small-batch snacks brand (sweet · salty · spicy). Built on a customized [Dawn](https://github.com/Shopify/dawn) theme, with a starter catalog, page content, and the [Shopify Dev MCP](https://github.com/Shopify/dev-mcp) wired in so Claude Code can build against live Shopify docs, schemas, and your store data.

## What's in here

```
.
├── .mcp.json                 # Shopify Dev MCP server config (docs, schema, validation, store data)
├── assets/ config/ layout/   # Dawn theme (customized for CraversBest)
│   locales/ sections/
│   snippets/ templates/
├── config/settings_data.json # CraversBest brand: colors, fonts, radii, cart, footer
├── templates/index.json      # Homepage: hero → value props → categories → best sellers → story → bundles → newsletter
└── store/                    # Content to load into the store (not theme files)
    ├── products.csv          # 11 starter snack products, ready to import
    ├── collections.md        # Smart-collection rules (sweet/salty/spicy/bundles/best-sellers…)
    ├── navigation.md         # Header + footer menu structure
    └── pages/                # About, FAQ, Contact, Shipping & Returns (paste-ready HTML)
```

## Prerequisites

Already verified on this machine:

| Tool | Version | Purpose |
|---|---|---|
| Node.js | 25.x | Runs the Shopify CLI + MCP server |
| Shopify CLI | 3.94+ | `shopify theme dev / push / pull` |
| Git | 2.52+ | Version control |

## The MCP server

`.mcp.json` registers the **`shopify-dev`** MCP server (`npx @shopify/dev-mcp@latest`). When you open this repo in Claude Code, approve the server when prompted. It gives Claude:

- **Docs & schema** — `learn_shopify_api`, `search_docs`, `fetch_full_docs`, `introspect_graphql_schema`
- **Validation** — `validate_theme`, `validate_theme_codeblocks`, `validate_graphql_codeblocks` (catch Liquid/GraphQL errors before deploy)
- **Store data (Admin API)** — `read_products`, `read_orders`, `read_customers`, `read_content`, `read_online_store_pages`, `read_themes`, `read_write`, and more (authorize to your store on first use)

## Build & preview workflow

Run these from the repo root. The first command that touches your store opens a browser to log in.

```bash
# 1. Live preview with hot reload against your dev store
shopify theme dev --store your-store.myshopify.com

# 2. Lint the theme (should report only minor warnings)
shopify theme check

# 3. Push as an unpublished draft to review in the admin
shopify theme push --unpublished --theme "CraversBest"

# 4. When you're happy, publish it
shopify theme push --theme "CraversBest" --allow-live
```

> `shopify theme dev` never publishes — it serves a private preview URL. Only `--allow-live` or publishing in the admin changes what shoppers see.

## Store setup checklist

The theme is design + templates. This content lives in the store's database — set it up once:

1. **Products** — Admin → Products → Import → upload [`store/products.csv`](store/products.csv). Add product photos after import.
2. **Collections** — create the smart collections in [`store/collections.md`](store/collections.md) (they auto-fill from product tags).
3. **Pages** — Admin → Content → Pages → create About, FAQ, Contact, Shipping & Returns from [`store/pages/`](store/pages/). Set Contact's template to `page.contact`.
4. **Navigation** — build the header + footer menus from [`store/navigation.md`](store/navigation.md).
5. **Policies** — Settings → Policies → generate Refund, Privacy, Terms, Shipping (Shopify links them automatically).
6. **Branding** — upload a logo (Theme editor → Theme settings → Logo) and a favicon. Add a hero image + category tile images.
7. **Assign collections on the homepage** — in the theme editor, point "Shop by craving" tiles at Sweet/Salty/Spicy and "Best sellers" at the Best Sellers collection.

## Brand system

Defined in `config/settings_data.json`:

- **Crave Red** `#D62F27` — primary buttons & bold CTA sections
- **Espresso** `#231A15` — dark sections, text
- **Golden** `#F5A623` — accent / newsletter block
- **Cream** `#FFF7EE` — page background
- **Type** — Poppins (headings) + Assistant (body)
- **Shape** — pill buttons, 16px rounded cards with a soft shadow, drawer cart

---

Theme derived from Shopify Dawn (MIT — see `DAWN-LICENSE.md`).
