# Pricing

`products.csv` uses **real selling prices**, mapped to each SKU by **GTIN / barcode** from the price list provided by the store owner.

- All **76 variants** matched a price by GTIN (100% coverage, no placeholders).
- Prices were verified by checking that every multi-size product forms a rising ladder (e.g. 8 oz < 16 oz < 32 oz) — all 16 size ladders are monotonic, confirming a clean mapping.
- Range: **$9.74 – $58.78**.

### If prices change
Update them in **Shopify admin → Products** (bulk editor), or edit the `Variant Price` column in `products.csv` and re-import (Shopify matches on `Handle` + `Variant SKU`).

> Prices were transcribed from a screenshot of the GTIN→price list. The size-ladder check gives high confidence, but do a quick spot-check against the source before publishing live.
