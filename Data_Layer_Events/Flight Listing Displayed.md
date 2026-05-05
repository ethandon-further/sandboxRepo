# Flight Listing Displayed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Flight Listing Displayed",
  "airTravel": {
    "duration": "<1>",
    "numAdults": "<zero>",
    "flightList": [
      {
        "tripId": "<SFO>YYC:YYC>SFO>",
        "flightId": "<SFO>YYC>",
        "flightSequence": "<1>",
        "flightDepartureDate": "<2021-10-20>"
      }
    ],
    "numFlights": "<1>",
    "numInfants": "<zero>",
    "returnDate": "<2021-10-22>",
    "numChildren": "<zero>",
    "tripRouting": "<one way>",
    "departureDate": "<2021-10-20>",
    "bookingLeadTime": "<zero>",
    "numSeatedGuests": "<1>",
    "bookingInteraction": "<Flight Search Performed>",
    "companionFareIndicator": "<available>"
  },
  "voucherDiscount": {
    "discountCode": "<5OFFSHOES>",
    "discountCodeStatus": "<valid>"
  }
});
```

## Variable Definitions

| Path | Type | Description | Example |
| --- | --- | --- | --- |
| `airTravel.duration` | integer | Number of days from the first segment departure to the final segment departure. For One-Way trips, the duration is always 1. | 1, 3, 5, 14, 20 |
| `airTravel.numAdults` | string | A count of adult travelers for a trip. | zero, 1, 2, 3, 4 |
| `airTravel.flightList[n].tripId` | string | A unique representation of the main departure and arrival points for all primary trip legs (not including connections).  | SFO>YYC:YYC>SFO, SFO>YYC, SFO>YYC:YYC>YXC:YKA>SFO |
| `airTravel.flightList[n].flightId` | string | A two-part string composed of the origin and destination airport codes for a flight with ">" between the airport codes. e.g. YYZ>SFO.  All flights from YYZ to SFO have the same ID regardless of how many stops/segments are involved. | SFO>YYC, YYC>SFO, ORD>YUL, YXC>LGA |
| `airTravel.flightList[n].flightSequence` | integer | The sequence of the flight within a trip.  The returning flight of a Round-Trip would be "2". | 1, 2, 3, 4, 5 |
| `airTravel.flightList[n].flightDepartureDate` | string | The date upon which a flight is scheduled to depart (in YYYY-MM-DD format).  | 2021-10-20, 2022-01-31, 2022-03-03 |
| `airTravel.numFlights` | integer | Number of flights within the trip. One-way is always 1. Round-trip is aways two. Multi-City is 2 or more. | 1, 2, 3, 4, 5 |
| `airTravel.numInfants` | string | A count of infant travelers for a trip. | zero, 1, 2, 3, 4 |
| `airTravel.returnDate` | string | Date of return for the last segment of a round trip or multi-city routing. | 2021-10-22, 2022-02-21, 2022-03-10 |
| `airTravel.numChildren` | string | A count of child travelers for a trip. | zero, 1, 2, 3, 4 |
| `airTravel.tripRouting` | string | Describes the routing for a trip. e.g. one way, round trip, or multi-city.  | one way, round trip, multi city |
| `airTravel.departureDate` | string | Date of departure for the first segment of a trip. | 2021-10-20, 2022-01-31, 2022-03-03 |
| `airTravel.bookingLeadTime` | string | Number of days ahead of departure for the first segment of a trip. | zero, 1, 20, 22, 33 |
| `airTravel.numSeatedGuests` | integer | Number of required seats for all travelers on a trip.  Typically adults + children. | 1, 2, 3, 4, 5 |
| `airTravel.bookingInteraction` | string | Captures the various interactions within the Trip Booking flow.  | Flight Search Performed, Flight Listing Displayed, Flight Summary Displayed, Guest Info Form Displayed, Flight Segment Seat Map Displayed |
| `airTravel.companionFareIndicator` | string | An indication of whether a companion fare is available / being requested / used for the trip. | available, unavailable, in use |
| `voucherDiscount.discountCode` | string | Discount code entered or applied | 5OFFSHOES, AKRONCANDLES2019 |
| `voucherDiscount.discountCodeStatus` | string | Indicates whether a discount code is valid, expired, or invalid. | valid, invalid, expired |

## Additional Notes

Flight options were listed (typically) as a result of a Flight Search.  The user may select which (if any) of the listed flights best meets their needs. 
