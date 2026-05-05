# Form Submission Failed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Form Submission Failed",
  "form": {
    "formID": "<F-0113>",
    "formName": "<Payment Info>",
    "formType": "<Address>",
    "formError": "<Credit card declined>",
    "formField": [
      {
        "fieldID": "<first_name>",
        "formSection": "<address1>",
        "fieldPosition": "<1>",
        "formFieldError": "<email address invalid>"
      }
    ]
  },
  "ecommerce": {
    "items": [
      {
        "location_id": "<155>"
      }
    ]
  },
  "event_data": {
    "name": "<Payment Info>",
    "type": "<Address>",
    "identifier": "<F-0113>",
    "error_message": "<Credit card declined>",
    "form_field_id": "<form_field_id>",
    "form_field_section": "<address1>",
    "form_field_position": "<1>",
    "form_field_error_message": "<email address invalid>"
  },
  "locationList": [
    {
      "locationId": "<155>",
      "locationName": "<Deerefiled Outlet>"
    }
  ]
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `form.formID` | string | Unique identifier of a form.  | F-0113, 2543, CU001, PI-0988 |
| `form.formName` | string | Plain text form name. Generally used if formID is not obtainable.  | Payment Info, Mailing Address, Payment Address, Contact Us |
| `form.formType` | string | Form type used for grouping of similar forms in reports.   | Address, Contact, Comment, Review, Payment |
| `form.formError` | string | Error text or code describing a form error.  This is the form-level error. | Credit card declined, Required entries missing, EC3456, EC8976 |
| `form.formField[n].fieldID` | string | Unique identifier of a form field within a form.  | first_name, last_name, addr_line1, addr_line2 |
| `form.formField[n].formSection` | string | Describes the section of a form to which a form field belongs. Useful for reporting on complex forms. | address1, address2, cc info, terms acceptance |
| `form.formField[n].fieldPosition` | integer | Integer position of a form field within a form.  The first for field is position 1. | 1, 2, 3, 4, 5 |
| `form.formField[n].formFieldError` | string | Error text or code describing a form field error.   | email address invalid, date required. EC987767, EC4567 |
| `ecommerce.items[n].location_id` | string | Captures a unique ID of a physical location such as a store, banking branch, atm, hotel, office, or other. | 155, 65588, 987764448 |
| `event_data.name` | string | Captures the human-friendly name of the form. | Payment Info, Mailing Address, Payment Address, Contact Us |
| `event_data.type` | string | Captures the type of form (i.e. demo, free trial, contact us). | Address, Contact, Comment, Review, Payment |
| `event_data.identifier` | string | Captures the unique ID of the form. | F-0113, 2543, CU001, PI-0988 |
| `event_data.error_message` | string | Captures the form error code or message associated with form errors. | Credit card declined, Required entries missing, EC3456, EC8976 |
| `event_data.form_field_id` | string | Captures the ID of each field contained on a form. |  |
| `event_data.form_field_section` | string | Captures the section containing each form field (i.e. CC Info, Address). | address1, address2, cc info, terms acceptance |
| `event_data.form_field_position` | string | Captures the numeric position of each form field within a form (i.e. 1, 2, 3). | 1, 2, 3, 4, 5 |
| `event_data.form_field_error_message` | string | Captures the form field error code or message associated with form field errors. | email address invalid, date required. EC987767, EC4567 |
| `locationList[n].locationId` | string | Unique Identifier of a Location.  | 155, 65588, 987764448 |
| `locationList[n].locationName` | string | The friendly name of the location. | Deerefiled Outlet, Old Orchard, Manhatten Midtown |

## Additional Notes

User submits an invalid form.
