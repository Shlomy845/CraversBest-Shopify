# CraversBest — store build log

Snapshot of what has been created in the **cravers-best** dev store (theme id `147124224074`, unpublished). Everything below was created programmatically via the Shopify Admin API (`shopify store execute`) from the data in this folder.

## Live in the store
- **54 products** (76 variants) — all `ACTIVE`, published to the Online Store, with real Walmart-CDN images (up to 10 each), GTIN barcodes, rich descriptions, and dietary tags. Inventory is **untracked** (always available) — enable tracking before launch if desired.
- **Real prices** — mapped 1:1 by GTIN from `prices.json` (range $9.74–$58.78), size-ladder verified.
- **17 smart collections** (auto-populated by tag/type/vendor), all published:
  - Category: `nuts` (22) · `seeds` (8) · `dried-fruit` (11) · `snack-boxes` (10) · `gift-boxes` (3)
  - Brand: `sammys-naturals` (36) · `nut-cravings` (7) · `i-am-snacky` (6) · `gift-a-snack` (5)
  - Merch: `best-sellers` (18) · `new` (12) · `gifts` (12)
  - Diet: `vegan` (30) · `keto` (29) · `kosher` (37) · `gluten-free` (23) · `non-gmo` (32)
- **Pages**: `about`, `faq`, `contact` (Dawn contact-form template), `shipping-returns` — all published.
- **Menus**: `main-menu` (Shop, Brands, Gifts, Best Sellers, Diet, Our Story + 14 sub-items) and `footer` (7 links).
- **Homepage** (`templates/index.json`) + brand system pushed to the theme.

## Preview
- Storefront: https://cravers-best.myshopify.com?preview_theme_id=147124224074
- Theme editor: https://admin.shopify.com/store/cravers-best/themes/147124224074/editor

## Before going live
1. **Publish the theme** (`shopify theme push --theme 147124224074 --allow-live`, or Publish in admin) — only when ready.
2. **Spot-check prices** against the source (transcribed from a screenshot).
3. Consider **enabling inventory tracking** and setting real stock levels.
4. Add **collection images** for the homepage tiles (currently fall back to the first product's image).
5. Review **Settings → Policies** (refund/privacy/terms/shipping) and shipping rates.

## Reproducibility
`products.csv` is an equivalent Shopify import file (same 54 products) if you ever need to re-import via Admin → Products → Import. `prices.json` is the GTIN→price source of truth.
