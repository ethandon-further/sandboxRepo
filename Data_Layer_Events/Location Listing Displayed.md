# Location Listing Displayed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Location Listing Displayed",
  "ecommerce": {
    "type": "<Product>",
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
        "item_category": "<pants>",
        "item_category2": "<item_category2>",
        "item_category3": "<item_category3>",
        "item_category4": "<item_category4>",
        "item_category5": "<item_category5>",
        "item_list_name": "<filter_by_group>"
      }
    ],
    "facets": "<sort~price ascending|color~green|size~medium>",
    "currency": "<USD>",
    "sort_order": "<high-low>",
    "item_list_id": "<12345abcde12345>",
    "item_list_name": "<filter_by_group>",
    "listing_driver": "<Onsite Search>",
    "listing_context": "<Filter Added>",
    "number_of_items": "<1>",
    "default_sort_order": "<A to Z>",
    "listing_filter_count": "<0>",
    "number_of_items_displayed": "<10>"
  },
  "listingDisplayed": {
    "listing": [
      {
        "room": {
          "numUnitsAvailable": "<0>"
        },
        "price": {
          "currency": "<USD>",
          "priceType": "<1st mark>",
          "pointRangeLow": "<1000>",
          "priceRangeLow": "<priceRangeLow>",
          "pointRangeHigh": "<5000>",
          "priceRangeHigh": "<priceRangeHigh>"
        },
        "location": {
          "rating": {
            "count": "<1>",
            "average": "<1.1>"
          },
          "latitude": "<48.858093>",
          "longitude": "<2.294694>",
          "locationId": "<155>",
          "locationName": "<Deerefiled Outlet>",
          "locationType": "<Retail Store>",
          "locationBrand": "<BMO Harris>",
          "locationStatus": "<Closed>",
          "locationDistanceFromPOI": "<12>"
        },
        "isDisplayed": "<true>",
        "itemPosition": "<1>"
      }
    ],
    "sortOrder": "<high-low>",
    "filterList": "<sort~price ascending|color~green|size~medium>",
    "listingType": "<text>",
    "sortDefault": "<A to Z>",
    "displayCount": "<10>",
    "resultsCount": "<1>",
    "listingDriver": "<Onsite Search>",
    "listingContext": "<Filter Added>",
    "filterListLength": "<0>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `ecommerce.type` | string | Captures the methods that bring users to listings (i.e. Onsite Search, Top Nav, External Link, Category Landing Page). Does not update if listings are sorted, filtered, or paginated. | Product, Location, Event, Room, Content |
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
| `ecommerce.items[n].item_category` | string | Item Category (context-specific). item_category2 through item_category5 can also be used if the item has many categories. | pants |
| `ecommerce.items[n].item_category2` | string | The second category of an item. |  |
| `ecommerce.items[n].item_category3` | string | The third category of an item. |  |
| `ecommerce.items[n].item_category4` | string | The fourth category of an item. |  |
| `ecommerce.items[n].item_category5` | string | The fifth category of an item. |  |
| `ecommerce.items[n].item_list_name` | string | The human-readable name of the item list the item showed up in (if sent with a view_item_list event). If one is not available, populate with numerical index of which list this is on the page (1-indexed). For filter_by_group component, use that value. | filter_by_group, recommended_products, recently_viewed_products |
| `ecommerce.facets` | string | Details filters used to refine a listing | sort~price ascending\|color~green\|size~medium |
| `ecommerce.currency` | string | Captures the currency code of a specific item in a listing. | USD, CAD, GBP, CHF |
| `ecommerce.sort_order` | number | The sort value selected by the user on listings. | high-low, low-high, nearest-farthest, a-z, newest-oldest |
| `ecommerce.item_list_id` | string | The computer-readable machine name of the list the item showed up in (if sent with a view_item_list event). Use UUID provided by the component if no more specific ID is available. | 12345abcde12345 |
| `ecommerce.item_list_name` | string | The human-readable name of the item list the item showed up in (if sent with a view_item_list event). If one is not available, populate with numerical index of which list this is on the page (1-indexed). For filter_by_group component, use that value. | filter_by_group, recommended_products, recently_viewed_products |
| `ecommerce.listing_driver` | string |  | Onsite Search, Curated Assortment, Navigation |
| `ecommerce.listing_context` | string | The context in which the listing is displayed (Onsite Search, Curated Assortment, Navigation) | Filter Added, Filter Removed, Sort Change, Pagination |
| `ecommerce.number_of_items` | integer | Count of locations returned in location listings. | 1, 21, 111, 166 |
| `ecommerce.default_sort_order` | string | The sort value selected by default on listings. | A to Z, Low to High, Newest to Oldest |
| `ecommerce.listing_filter_count` | integer | Captures the number of filters applied to a listing. | 0, 20, 12 |
| `ecommerce.number_of_items_displayed` | integer | Captures the number of locations displayed in a location listing. | 10, 20, 30, 40 |
| `listingDisplayed.listing[n].room.numUnitsAvailable` | integer | Integer number of rooms available for the given search parameters at a property or of a room type. | 0, 10, 20, 23 |
| `listingDisplayed.listing[n].price.currency` | string | Currency of the prices given. ISO 4217 (3 character alpha), uppercase  | USD, CAD, GBP, CHF |
| `listingDisplayed.listing[n].price.priceType` | string | Describes the type of price offered using commonly used terms.  | 1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster |
| `listingDisplayed.listing[n].price.pointRangeLow` | integer | Lower end of the point range shown. | 1000, 1510, 1800 |
| `listingDisplayed.listing[n].price.priceRangeLow` | string | String representation of the lower end of the price range shown. |  |
| `listingDisplayed.listing[n].price.pointRangeHigh` | integer | Upper end of the point range shown. | 5000, 2520, 3200 |
| `listingDisplayed.listing[n].price.priceRangeHigh` | string | String representation of the upper end of the price range shown. |  |
| `listingDisplayed.listing[n].location.rating.count` | integer | Integer number of customer ratings.  | 1, 5, 11, 200 |
| `listingDisplayed.listing[n].location.rating.average` | string | String representation of the average customer rating.  Positive. Up to two decimal places. This is most often a number between 0 and 5.  | 1.1, 2, 5 |
| `listingDisplayed.listing[n].location.latitude` | number | The latitude of the map center for a location search. | 48.858093 |
| `listingDisplayed.listing[n].location.longitude` | number | The longitude of the map center for a location search. | 2.294694 |
| `listingDisplayed.listing[n].location.locationId` | string | Unique Identifier of a Location.  | 155, 65588, 987764448 |
| `listingDisplayed.listing[n].location.locationName` | string | The friendly name of the location. | Deerefiled Outlet, Old Orchard, Manhatten Midtown |
| `listingDisplayed.listing[n].location.locationType` | string | The type of the location | Retail Store, Lodging, ATM, Banking Branch |
| `listingDisplayed.listing[n].location.locationBrand` | string | The brand associated with a location. | BMO Harris, Walmart, Lands' End, Motel 6, AC Hotels |
| `listingDisplayed.listing[n].location.locationStatus` | string | The status of a location. | Closed, Open, Coming Soon, Wait-listed |
| `listingDisplayed.listing[n].location.locationDistanceFromPOI` | integer | The distance from the location to the user's point of interest | 12, 3, 5, 200 |
| `listingDisplayed.listing[n].isDisplayed` | boolean | Helper node used by AA Product String Builder to set product scoped events | true |
| `listingDisplayed.listing[n].itemPosition` | integer | Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI. | 1, 2, 3, 4, 5 |
| `listingDisplayed.sortOrder` | string | Indicates the sort order. | high-low, low-high, nearest-farthest, a-z, newest-oldest |
| `listingDisplayed.filterList` | string | A twice delimited string of filterType and filterValue pairs.  Use ~ between type and value.  Use \| between pairs | sort~price ascending\|color~green\|size~medium |
| `listingDisplayed.listingType` | string | The type of results being listed | text, product, location, event, room, product location |
| `listingDisplayed.sortDefault` | integer | The default sort value on listings | A to Z, Low to High, Newest to Oldest |
| `listingDisplayed.displayCount` | integer | The total number of items displayed out of all returned items. (Integer) | 10, 20, 30, 40 |
| `listingDisplayed.resultsCount` | integer | The total number of items returned that matched the search criteria. (Integer) | 1, 21, 111, 166 |
| `listingDisplayed.listingDriver` | string | Describes the action that caused the listing to be displayed | Onsite Search, Curated Assortment, Navigation |
| `listingDisplayed.listingContext` | string | Describes the context of a listing display (sort changed, filter added, filter removed) | Filter Added, Filter Removed, Sort Change, Pagination |
| `listingDisplayed.filterListLength` | integer | The number of filterValue pairs in the filterList | 0, 20, 12 |

## Additional Notes

User views a location in a listing.
