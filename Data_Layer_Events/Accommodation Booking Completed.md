# Accommodation Booking Completed

## JavaScript Code
```javascript
window.EthanTest.push({
  "event": "Accommodation Booking Completed",
  "booking": {
    "test": "<test>",
    "total": {
      "currency": "<USD>"
    },
    "payment": [
      {
        "paymentID": "<ZPH-87698-098>",
        "paymentMethod": "<Credit Card>",
        "paymentSequence": "<1>",
        "loyaltyPointsAmount": "<100>"
      }
    ],
    "roomList": [
      {
        "room": {
          "numKids": "<1>",
          "rateCode": "<AAA>",
          "stayDate": "<2001-12-22>",
          "typeCode": "<1-K-NS>",
          "numAdults": "<1>",
          "ratePerNight": "<200>",
          "numberInMultiRoomReservation": "<1>"
        },
        "location": {
          "locationId": "<155>"
        }
      }
    ],
    "transactionID": "<transactionID>"
  },
  "ecommerce": {
    "tax": "<1.11>",
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
    "coupon": "<summer_fun>",
    "currency": "<USD>",
    "sequence": "<1>",
    "shipping": "<3.33>",
    "payment_id": "<payment_id>",
    "affiliation": "<Google Store>",
    "payment_type": "<Credit Card>",
    "reservation_id": "<reservation_id>",
    "transaction_id": "<T_12345>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example | Requirement Status | XDM Path |
| --- | --- | --- | --- | --- | --- |
| `booking.test` | string |  |  | Optional |  |
| `booking.total.currency` | string | Currency of the payment for the booking. ISO 4217 (3 character alpha), uppercase  | USD, CAD, GBP, CHF | Required |  |
| `booking.payment[n].paymentID` | string | Unique identifier of a payment.  Typically an integration key from a back-end system. | ZPH-87698-098 | Optional |  |
| `booking.payment[n].paymentMethod` | string | Describes the method of payment for a transaction.  | Credit Card, PayPal, Mastercard, Visa, Amex, Discover | Optional |  |
| `booking.payment[n].paymentSequence` | integer | Integer indicator of the sequence in which payments were applied within a transaction.  Starting with 1. | 1, 2, 3, 4, 5 | Optional |  |
| `booking.payment[n].loyaltyPointsAmount` | integer | Number of loyalty points  | 100, 101, 1000 | Optional |  |
| `booking.roomList[n].room.numKids` | integer | Integer number of kids for the booking. | 1, 2, 3, 4, 5 | Optional |  |
| `booking.roomList[n].room.rateCode` | string | Description of the rate being offered. Should match rate codes from back-end systems to allow data import.  | AAA, MILITARY, CORP-567, CORP-345 | Optional |  |
| `booking.roomList[n].room.stayDate` | string | Date of each room night. ISO 8601 form (YYYY-MM-DD). Jan 1, 2019 is 2019-01-01 | 2001-12-22, 2011-01-01 | Optional |  |
| `booking.roomList[n].room.typeCode` | string | A code describing the room features. Often indicates number of beds, smoking or non-smoking, ADA accessibility and so on. | 1-K-NS, 2-Q-S, S-K-NS-City | Optional |  |
| `booking.roomList[n].room.numAdults` | integer | Integer number of adults for the booking. | 1, 2, 3, 4, 5 | Optional |  |
| `booking.roomList[n].room.ratePerNight` | string | String representation of the price per use-period. Typically nightly rate for a hotel room or monthly rate for an apartment. Positive. Up to two decimal places for cents. No currency symbol. | 200, 75.29, 150, 89.2 | Optional |  |
| `booking.roomList[n].room.numberInMultiRoomReservation` | integer | Integer position of a room in a multi-room booking action. | 1, 2, 3 | Optional |  |
| `booking.roomList[n].location.locationId` | string | Unique Identifier of a Location.  | 155, 65588, 987764448 | Required |  |
| `booking.transactionID` | string | Unique identifier of the transaction. Max Length 20. Used as a key for upload of post transaction data.  |  | Recommended |  |
| `ecommerce.tax` | number | Tax cost associated with a transaction. | 1.11 | Recommended |  |
| `ecommerce.items[n].index` | number | The index/position of the item in a list. | 1, 2, 3, 4 | Optional |  |
| `ecommerce.items[n].price` | number | The monetary price of the item, in units of the specified currency parameter. | 9.99 | Recommended |  |
| `ecommerce.items[n].coupon` | string | Item-level coupon code used for a purchase. | SUMMER_FUN | Optional |  |
| `ecommerce.items[n].item_id` | string | Item ID (context-specific).The product primary ID (SKU or UPC) | SKU_12345 | Required |  |
| `ecommerce.items[n].currency` | string | The currency, in 3-letter ISO 4217 format. | USD | Optional |  |
| `ecommerce.items[n].discount` | number | Monetary value of discount associated with a purchase. | 2.22 | Optional |  |
| `ecommerce.items[n].quantity` | integer | Item quantity. | 1 | Recommended |  |
| `ecommerce.items[n].item_name` | string | Item Name (context-specific). | jeggings | Required |  |
| `ecommerce.items[n].item_brand` | string | Item brand | Gucci | Recommended |  |
| `ecommerce.items[n].affiliation` | string | A product affiliation to designate a supplying company or brick and mortar store location. | Google Store | Optional |  |
| `ecommerce.items[n].location_id` | string | The location associated with the event. If possible, set to the Google Place ID that corresponds to the associated item. Can also be overridden to a custom location ID string. | L_12345 | Optional |  |
| `ecommerce.items[n].item_list_id` | string | The computer-readable machine name of the list the item showed up in (if sent with a view_item_list event). Use UUID provided by the component if no more specific ID is available. | 12345abcde12345 | Optional |  |
| `ecommerce.items[n].item_variant` | string | The variant of the item. | Black | Recommended |  |
| `ecommerce.items[n].item_category` | string | Item Category (context-specific). item_category2 through item_category5 can also be used if the item has many categories. | pants | Recommended |  |
| `ecommerce.items[n].item_category2` | string | The second category of an item. |  | Recommended |  |
| `ecommerce.items[n].item_category3` | string | The third category of an item. |  | Recommended |  |
| `ecommerce.items[n].item_category4` | string | The fourth category of an item. |  | Recommended |  |
| `ecommerce.items[n].item_category5` | string | The fifth category of an item. |  | Recommended |  |
| `ecommerce.items[n].item_list_name` | string | The human-readable name of the item list the item showed up in (if sent with a view_item_list event). If one is not available, populate with numerical index of which list this is on the page (1-indexed). For filter_by_group component, use that value. | filter_by_group, recommended_products, recently_viewed_products | Optional |  |
| `ecommerce.value` | number | The monetary value of the event. | 7.77, 239.55, 659 | Required |  |
| `ecommerce.coupon` | string | Order-level coupon code used for a purchase. | summer_fun | Optional |  |
| `ecommerce.currency` | string | The currency, in 3-letter ISO 4217 format. | USD | Required |  |
| `ecommerce.sequence` | integer | Indicates the sequence of payment application within a transaction | 1, 2, 3, 4, 5 | Optional |  |
| `ecommerce.shipping` | number | Shipping cost associated with a transaction. | 3.33 | Recommended |  |
| `ecommerce.payment_id` | string | Captures a unique payment ID for a transaction. |  | Optional |  |
| `ecommerce.affiliation` | string | A order affiliation to designate a supplying company or brick and mortar store location. | Google Store | Optional |  |
| `ecommerce.payment_type` | string | Captures the payment methods used for a transaction (i.e. credit card, Visa, MasterCard, Amex, Paypal, purchase order, etc). | Credit Card, PayPal, Mastercard, Visa, Amex, Discover | Optional |  |
| `ecommerce.reservation_id` | string | Captures the reservation ID associated with each booking. |  | Recommended |  |
| `ecommerce.transaction_id` | string | The unique identifier of a transaction. | T_12345, 19283j2nm9jdjs | Required |  |

## Additional Notes

User completes an accommodation booking.
