# CraversBest — Collections

CraversBest is a multi-brand snack shop carrying **4 brands** (Sammys Naturals, Nut Cravings, I AM Snacky, Gift A Snack) across nuts, seeds, dried fruit, snack boxes, and gift boxes.

Create these in **Shopify admin → Products → Collections** as **Smart (automated)** collections so products self-sort from the tags in `products.csv`. Handles must match exactly — the theme + navigation link to them.

## Category collections (by product Type)
| Collection | Handle | Rule |
|---|---|---|
| Nuts | `nuts` | Product **Type** is equal to `Nuts` |
| Seeds | `seeds` | Product **Type** is equal to `Seeds` |
| Dried Fruit | `dried-fruit` | Product **Type** is equal to `Dried Fruit` |
| Snack Boxes | `snack-boxes` | Product **Type** is equal to `Snack Boxes` |
| Gift Boxes | `gift-boxes` | Product **Type** is equal to `Gift Boxes` |

## Brand collections (by Vendor)
| Collection | Handle | Rule |
|---|---|---|
| Sammys Naturals | `sammys-naturals` | Product **Vendor** is equal to `Sammys Naturals` |
| Nut Cravings | `nut-cravings` | Product **Vendor** is equal to `Nut Cravings` |
| I AM Snacky | `i-am-snacky` | Product **Vendor** is equal to `I AM Snacky` |
| Gift A Snack | `gift-a-snack` | Product **Vendor** is equal to `Gift A Snack` |

## Merchandising collections (by tag)
| Collection | Handle | Rule | ~count |
|---|---|---|---|
| Best Sellers | `best-sellers` | Product **tag** is equal to `best-seller` | 18 |
| New Arrivals | `new` | Product **tag** is equal to `New` | 13 |
| Gifts | `gifts` | Product **tag** is equal to `Gifts` | 13 |

## Dietary collections (by tag)
| Collection | Handle | Rule | ~count |
|---|---|---|---|
| Vegan | `vegan` | Product **tag** is equal to `Vegan` | 30 |
| Keto | `keto` | Product **tag** is equal to `Keto` | 29 |
| Kosher | `kosher` | Product **tag** is equal to `Kosher` | 38 |
| Gluten-Free | `gluten-free` | Product **tag** is equal to `Gluten-Free` | 25 |
| Non-GMO | `non-gmo` | Product **tag** is equal to `Non-GMO` | 34 |

> `all` (built-in) contains every product. The homepage "Shop by category" and "Shop by brand" rows, plus the header/footer menus, all reference the handles above — create them and the store lights up automatically.

## After creating them
1. Add a **collection image** to each category + brand collection (used on the homepage tiles and collection cards).
2. On the homepage (theme editor), assign the "Shop by category" tiles to Nuts / Seeds / Dried Fruit / Snack Boxes / Gift Boxes and the "Shop by brand" tiles to the 4 brand collections.
3. Optionally enable **collection filtering** (Search & Discovery app) so shoppers can filter by the dietary tags.
