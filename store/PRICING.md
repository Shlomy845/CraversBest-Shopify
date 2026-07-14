# ⚠️ Pricing — placeholder values, must be set before going live

The Walmart export in `products.csv` **did not include selling prices** (Walmart manages price separately). To make the store previewable, `Variant Price` is filled with **placeholder prices by size**:

| Size / type | Placeholder |
|---|---|
| ≤ 4 oz | $7.99 |
| ≤ 8 oz | $10.99 |
| ≤ 16 oz | $16.99 |
| ≤ 24 oz | $22.99 |
| ≤ 32 oz | $27.99 |
| Snack Boxes | $29.99 |
| Gift Boxes | $49.99 |

**These are NOT real prices.** Before publishing the theme live:

1. Provide the real price list (per SKU) — I'll drop it into `products.csv` and re-import, **or**
2. Set prices in **Shopify admin → Products** (bulk editor: select all → Edit prices), **or**
3. Export current products, fill the Price column, and re-import.

The store is safe in the meantime: it's on a **password-protected dev store** with an **unpublished theme**, so nothing is publicly purchasable at these prices. Do not publish live until prices are confirmed.
