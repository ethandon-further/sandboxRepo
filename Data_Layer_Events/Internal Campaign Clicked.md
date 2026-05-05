# Internal Campaign Clicked

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Internal Campaign Clicked",
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
        "location_id": "<155>",
        "item_list_id": "<12345abcde12345>",
        "item_variant": "<Black>",
        "promotion_id": "<P_12345>",
        "creative_name": "<summer_banner2>",
        "creative_slot": "<featured_app_1>",
        "item_category": "<pants>",
        "item_category2": "<item_category2>",
        "item_category3": "<item_category3>",
        "item_category4": "<item_category4>",
        "item_category5": "<item_category5>",
        "item_list_name": "<filter_by_group>",
        "promotion_name": "<Summer Sale>"
      }
    ],
    "promotion_id": "<2345>",
    "creative_name": "<Girl with bike>",
    "creative_slot": "<creative_slot>",
    "promotion_name": "<Trek bikes for kids>",
    "promotion_objective": "<Order Starter>"
  },
  "internalCampaign": {
    "campaignList": [
      {
        "internalCampaignID": "<2345>",
        "internalCampaignName": "<Trek bikes for kids>",
        "internalCampaignCreative": "<Girl with bike>",
        "internalCampaignPosition": "<1>",
        "internalCampaignObjective": "<Order Starter>"
      }
    ],
    "internalCampaignID": "<2345>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
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
| `ecommerce.items[n].location_id` | string | Captures a unique ID of a physical location such as a store, banking branch, atm, hotel, office, or other. | 155, 65588, 987764448 |
| `ecommerce.items[n].item_list_id` | string | The computer-readable machine name of the list the item showed up in (if sent with a view_item_list event). Use UUID provided by the component if no more specific ID is available. | 12345abcde12345 |
| `ecommerce.items[n].item_variant` | string | The variant of the item. | Black |
| `ecommerce.items[n].promotion_id` | string | The ID of a product promotion. | P_12345 |
| `ecommerce.items[n].creative_name` | string | The name of a creative used in a promotional spot. | summer_banner2 |
| `ecommerce.items[n].creative_slot` | string | The name of a creative slot. | featured_app_1 |
| `ecommerce.items[n].item_category` | string | Item Category (context-specific). item_category2 through item_category5 can also be used if the item has many categories. | pants |
| `ecommerce.items[n].item_category2` | string | The second category of an item. |  |
| `ecommerce.items[n].item_category3` | string | The third category of an item. |  |
| `ecommerce.items[n].item_category4` | string | The fourth category of an item. |  |
| `ecommerce.items[n].item_category5` | string | The fifth category of an item. |  |
| `ecommerce.items[n].item_list_name` | string | The human-readable name of the item list the item showed up in (if sent with a view_item_list event). If one is not available, populate with numerical index of which list this is on the page (1-indexed). For filter_by_group component, use that value. | filter_by_group, recommended_products, recently_viewed_products |
| `ecommerce.items[n].promotion_name` | string | The name of a product promotion. One of promotion_id or promotion name is required. | Summer Sale |
| `ecommerce.promotion_id` | string | Captures the ID associated with internal campaigns. Used for internal campaign impressions and clicks only. | 2345, 56789, 9876 |
| `ecommerce.creative_name` | string | Captures the internal campaign creative associated with internal campaigns. Used for internal campaign impressions and clicks only. | Girl with bike, Mountain Top, River Cruise Danube |
| `ecommerce.creative_slot` | string | The name of the promotional creative slot associated with the event. |  |
| `ecommerce.promotion_name` | string | Captures the name associated with internal campaigns. Used for internal campaign impressions and clicks only. | Trek bikes for kids, REI Spring Sale 2019, Viking Cruise Fall Specials |
| `ecommerce.promotion_objective` | string | Captures the objective (A/B Test, sale promo) associated with each internal campaign click and the impact on downstream success or conversion. | Order Starter, Order Value, Newsletter Subscriptions, 12, 33, 44 |
| `internalCampaign.campaignList[n].internalCampaignID` | string | Unique Identifier of an internal campaign | 2345, 56789, 9876 |
| `internalCampaign.campaignList[n].internalCampaignName` | string | The name of the promotion. | Trek bikes for kids, REI Spring Sale 2019, Viking Cruise Fall Specials |
| `internalCampaign.campaignList[n].internalCampaignCreative` | string | Describes the creative treatment for an internal campaign | Girl with bike, Mountain Top, River Cruise Danube |
| `internalCampaign.campaignList[n].internalCampaignPosition` | integer | The position of a internal campaign offering within a list of internal campaigns | 1, 5, 78, 3 |
| `internalCampaign.campaignList[n].internalCampaignObjective` | string | Objective of the Internal Campaign | Order Starter, Order Value, Newsletter Subscriptions, 12, 33, 44 |
| `internalCampaign.internalCampaignID` | string | Unique Identifier of an internal campaign | 2345, 56789, 9876 |

## Additional Notes

User clicks on an internal marketing campaign item.
