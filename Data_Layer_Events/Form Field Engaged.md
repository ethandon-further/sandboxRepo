# Form Field Engaged

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Form Field Engaged",
  "form": {
    "formID": "<F-0113>",
    "formName": "<Payment Info>",
    "formField": [
      {
        "fieldID": "<first_name>"
      }
    ]
  },
  "event_data": {
    "name": "<Payment Info>",
    "form_field_id": "<form_field_id>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `form.formID` | string | Unique identifier of a form.  | F-0113, 2543, CU001, PI-0988 |
| `form.formName` | string | Plain text form name. Generally used if formID is not obtainable.  | Payment Info, Mailing Address, Payment Address, Contact Us |
| `form.formField[n].fieldID` | string | Unique identifier of a form field within a form.  | first_name, last_name, addr_line1, addr_line2 |
| `event_data.name` | string | Captures the human-friendly name of the form. | Payment Info, Mailing Address, Payment Address, Contact Us |
| `event_data.form_field_id` | string | Captures the ID of each field contained on a form. |  |

## Additional Notes

Inidcates that the user has enaged with a form field and changed the field value
