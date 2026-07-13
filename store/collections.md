# CraversBest — Collections

Create these in **Shopify admin → Products → Collections**. Use **Smart (automated)** collections so products self-sort by the tags already set in `products.csv`. Handles must match exactly — the theme links to them.

| Collection | Handle | Type | Rule | Used by |
|---|---|---|---|---|
| All snacks | `all` | Auto (built-in) | — | Hero CTA, nav, "Shop all" |
| Best Sellers | `best-sellers` | Smart | Product tag **is equal to** `best-seller` | Homepage "Best sellers", nav |
| Sweet | `sweet` | Smart | Product tag **is equal to** `sweet` | "Shop by craving" tile 1 |
| Salty | `salty` | Smart | Product tag **is equal to** `salty` | "Shop by craving" tile 2 |
| Spicy | `spicy` | Smart | Product tag **is equal to** `spicy` | "Shop by craving" tile 3 |
| Bundles | `bundles` | Smart | Product tag **is equal to** `bundle` | Hero CTA, homepage "Build your own bundle", nav |
| New | `new` | Smart | Product tag **is equal to** `new` | Optional nav/promo |
| Vegan | `vegan` | Smart | Product tag **is equal to** `vegan` | Optional filter/nav |
| Gluten-Free | `gluten-free` | Smart | Product tag **is equal to** `gluten-free` | Optional filter/nav |

## After creating them
1. Open the homepage in the theme editor (`shopify theme dev` → the local preview, or the admin customizer).
2. In **Shop by craving**, assign the three tiles to **Sweet**, **Salty**, **Spicy**.
3. In **Best sellers**, set the collection to **Best Sellers**.
4. Add a collection image to each (used on the "Shop by craving" tiles and collection cards).

> Tip: the **Bundles** collection handle is `bundles` — the hero's "Build a bundle" button and the bundles section already point there, so it lights up automatically once the collection exists.
