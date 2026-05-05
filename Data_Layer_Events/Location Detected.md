# Location Detected

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Location Detected",
  "location": {
    "locationDeterminationMethod": "<Automatic - IP based>"
  },
  "ecommerce": {
    "items": [
      {
        "location_id": "<155>"
      }
    ]
  },
  "event_data": {
    "determination_method": "<Automatic - IP based>"
  },
  "locationList": [
    {
      "locationId": "<155>",
      "locationName": "<Deerefiled Outlet>",
      "locationType": "<Retail Store>"
    }
  ]
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `location.locationDeterminationMethod` | string | Describes how a location selection was determined.  Was it automatic or customer choice. | Automatic - IP based, Automatic - Device Based, Customer Selected |
| `ecommerce.items[n].location_id` | string | Captures a unique ID of a physical location such as a store, banking branch, atm, hotel, office, or other. | 155, 65588, 987764448 |
| `event_data.determination_method` | string | Captures the method that was used to determine the location associated with visitor activity. | Automatic - IP based, Automatic - Device Based, Customer Selected |
| `locationList[n].locationId` | string | Unique Identifier of a Location.  | 155, 65588, 987764448 |
| `locationList[n].locationName` | string | The friendly name of the location. | Deerefiled Outlet, Old Orchard, Manhatten Midtown |
| `locationList[n].locationType` | string | The type of location associated with activity and conversion. | Retail Store, Lodging, ATM, Banking Branch |

## Additional Notes

Location is known at the time of user activity or conversion. (i.e., a user has a selected retailer as their retailer and is performing subsequent activities that should be associated with the retailer)
