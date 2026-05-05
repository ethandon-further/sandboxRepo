# Cart Popup Displayed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Cart Popup Displayed",
  "cart": {
    "item": [
      {
        "price": {
          "priceTier": "<Good>",
          "priceType": "<1st mark>"
        },
        "productInfo": {
          "sku": "<34567890>",
          "name": "<Oceana>",
          "brand": "<Ford>",
          "color": "<Antique Oak>",
          "productID": "<155>",
          "productLine": "<Laminate Wood>",
          "trademarkedTechnology": "<Stainmaster>"
        }
      }
    ],
    "cartID": "<12345>"
  },
  "ecommerce": {
    "items": [
      {
        "index": "<1>",
        "price": "<9.99>",
        "coupon": "<SUMMER_FUN>",
        "item_id": "<SKU_12345>",
        "currency": "<USD>",
        "discount": "<2.22>",
        "quantity": "<1>",
        "item_name": "<jeggings>",
        "item_brand": "<Gucci>",
        "affiliation": "<Google Store>",
        "location_id": "<L_12345>",
        "item_list_id": "<12345abcde12345>",
        "item_variant": "<Black>",
        "item_category": "<pants>",
        "item_category2": "<item_category2>",
        "item_category3": "<item_category3>",
        "item_category4": "<item_category4>",
        "item_category5": "<item_category5>",
        "item_list_name": "<filter_by_group>"
      }
    ],
    "value": "<7.77>",
    "cart_id": "<12345>",
    "currency": "<USD>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `cart.item[n].price.priceTier` | string | Describes the general pricing tier of a product. (Good, Better, Best) | Good, Better, Best, Bronze, Silver, Gold |
| `cart.item[n].price.priceType` | string | Describes the type of price offered using commonly used terms.  | 1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster |
| `cart.item[n].productInfo.sku` | string | Stock Keeping Unit (SKU) Unique Identifier of specific item (typically) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants.  | 34567890, 4567890, 00155-large-cornflower |
| `cart.item[n].productInfo.name` | string | Name of the product or offering.  Should be unique and 1:1 with productID | Oceana, Corsica, Flame Tech, Air Jordan 88 |
| `cart.item[n].productInfo.brand` | string | Describes the brand of a product or offering. | Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia |
| `cart.item[n].productInfo.color` | string | Describes the colorway of a product or product variant | Antique Oak, Granite, Black Marble, Knotty Pine |
| `cart.item[n].productInfo.productID` | string | Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants.  | 155, 65588, 987764448 |
| `cart.item[n].productInfo.productLine` | string | Describes the product Line of a product.  | Laminate Wood, Vinyl, Hardwood, Stone, Ceramic |
| `cart.item[n].productInfo.trademarkedTechnology` | string | Describes trademarks and/or technical branding used to describe the product | Stainmaster, GoreTex, WeatherShield |
| `cart.cartID` | string | Back-end identifier for a shopping cart | 12345, 435678, 34567, XCV456, XCV876 |
| `ecommerce.items[n].index` | number | The index/position of the item in a list. | 1, 2, 3, 4 |
| `ecommerce.items[n].price` | number | The monetary price of the item, in units of the specified currency parameter. | 9.99 |
| `ecommerce.items[n].coupon` | string | Item-level coupon code used for a purchase. | SUMMER_FUN |
| `ecommerce.items[n].item_id` | string | Item ID (context-specific).The product primary ID (SKU or UPC) | SKU_12345 |
| `ecommerce.items[n].currency` | string | The currency, in 3-letter ISO 4217 format. | USD |
| `ecommerce.items[n].discount` | number | Monetary value of discount associated with a purchase. | 2.22 |
| `ecommerce.items[n].quantity` | integer | Item quantity. | 1 |
| `ecommerce.items[n].item_name` | string | Item Name (context-specific). | jeggings |
| `ecommerce.items[n].item_brand` | string | Item brand | Gucci |
| `ecommerce.items[n].affiliation` | string | A product affiliation to designate a supplying company or brick and mortar store location. | Google Store |
| `ecommerce.items[n].location_id` | string | The location associated with the event. If possible, set to the Google Place ID that corresponds to the associated item. Can also be overridden to a custom location ID string. | L_12345 |
| `ecommerce.items[n].item_list_id` | string | The computer-readable machine name of the list the item showed up in (if sent with a view_item_list event). Use UUID provided by the component if no more specific ID is available. | 12345abcde12345 |
| `ecommerce.items[n].item_variant` | string | The variant of the item. | Black |
| `ecommerce.items[n].item_category` | string | Item Category (context-specific). item_category2 through item_category5 can also be used if the item has many categories. | pants |
| `ecommerce.items[n].item_category2` | string | The second category of an item. |  |
| `ecommerce.items[n].item_category3` | string | The third category of an item. |  |
| `ecommerce.items[n].item_category4` | string | The fourth category of an item. |  |
| `ecommerce.items[n].item_category5` | string | The fifth category of an item. |  |
| `ecommerce.items[n].item_list_name` | string | The human-readable name of the item list the item showed up in (if sent with a view_item_list event). If one is not available, populate with numerical index of which list this is on the page (1-indexed). For filter_by_group component, use that value. | filter_by_group, recommended_products, recently_viewed_products |
| `ecommerce.value` | number | The monetary value of the event. | 7.77, 239.55, 659 |
| `ecommerce.cart_id` | string | Captures the name or ID of the region within which CTA links are used. | 12345, 435678, 34567, XCV456, XCV876 |
| `ecommerce.currency` | string | The currency, in 3-letter ISO 4217 format. | USD |

## Additional Notes

User encounters a pop-up while in the shopping cart.
