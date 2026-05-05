# Fundraiser Registration Started

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Fundraiser Registration Started",
  "event_data": {
    "identifier": "<FT-2019-Chicago>"
  },
  "fundraiser": {
    "fundraiserID": "<FT-2019-Chicago>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `event_data.identifier` | string | Captures the name or ID associated with each fundraiser. | FT-2019-Chicago, 19-45678, 2019-01-20_0123 |
| `fundraiser.fundraiserID` | string | Unique identifier of a specific fundraising activity. Most commonly an ID from the back-end system. | FT-2019-Chicago, 19-45678, 2019-01-20_0123 |

## Additional Notes

User begins fundraiser registration.
