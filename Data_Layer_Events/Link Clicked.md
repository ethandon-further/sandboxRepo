# Link Clicked

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Link Clicked"
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |

## Additional Notes

This event is used for cases in which an anchor tag is used as a link.

For example, if an `<a>` tag is used to represent a  link, you would need to add these attributes to trigger the event to be collected when the anchor is clicked.

Do not include the “data-dom-event” data attribute on any other elements that you do not want to be tracked.

Check the implementation notes for data-dom-event descriptions.
