# Interstitial Viewed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Interstitial Viewed",
  "event_data": {
    "type": "<alert>"
  },
  "interstitial": {
    "viewType": "<alert>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `event_data.type` | string | Captures the type of interstitial that was shown to visitors. | alert, offer, info required |
| `interstitial.viewType` | string | Type of interstitial view | alert, offer, info required |

## Additional Notes

User views an interstitial (modal) page or box.
