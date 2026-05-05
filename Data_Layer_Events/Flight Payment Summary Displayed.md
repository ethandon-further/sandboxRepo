# Flight Payment Summary Displayed

## JavaScript Code
```javascript
window.appEventData.push({
  "event": "Flight Payment Summary Displayed",
  "airTravel": {
    "duration": "<1>",
    "numAdults": "<zero>",
    "flightList": [
      {
        "tripId": "<SFO>YYC:YYC>SFO>",
        "flightId": "<SFO>YYC>",
        "flightBaseFare": "<flightBaseFare>",
        "flightDuration": "<46>",
        "flightSequence": "<1>",
        "flightFareClass": "<E>",
        "flightSegmentId": "<SFO>YYC>",
        "flightTotalFare": "<flightTotalFare>",
        "flightFareBundle": "<Basic>",
        "flightArrivalDate": "<2021-10-20>",
        "flightNumSegments": "<1>",
        "flightDepartureDate": "<2021-10-20>",
        "flightSegmentDuration": "<35>",
        "flightSegmentOperator": "<WestJet>",
        "flightSegmentSequence": "<1>",
        "flightSegmentEquipment": "<Boeing 737-600>",
        "flightSegmentGuestSeat": "<3B>",
        "flightSegmentGuestType": "<Adult>",
        "flightSegmentDesignator": "<WJ1515>",
        "flightSegmentGuestCabin": "<economy>",
        "flightSegmentGuestNumber": "<1>",
        "flightSegmentGuestSSRCodes": "<deaf>",
        "flightSegmentGuestSeatCost": "<zero>",
        "flightSegmentSeatSelectionMethod": "<Manual>",
        "flightSegmentAutoSeatSelectionStatus": "<Available>"
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
| `airTravel.flightList[n].flightBaseFare` | string | The base fare of the flight only in the currency displayed to the user.  |  |
| `airTravel.flightList[n].flightDuration` | string | The total duration of the flight (in minutes) from departure to arrival at final destination including time in flight and layovers.  | 46, 90, 120, 204 |
| `airTravel.flightList[n].flightSequence` | integer | The sequence of the flight within a trip.  The returning flight of a Round-Trip would be "2". | 1, 2, 3, 4, 5 |
| `airTravel.flightList[n].flightFareClass` | string | Describes the fare class for a flight (e.g. E,X, or B) | E, B, X |
| `airTravel.flightList[n].flightSegmentId` | string | A two-part string composed of the origin and destination airport codes for a segment with ">" between the airport codes. e.g. YYZ>SFO.   | SFO>YYC, YYC>SFO, ORD>YUL, YXC>LGA |
| `airTravel.flightList[n].flightTotalFare` | string | The total fare for the flight including Base Fare and Taxes in the currency displayed to the user.  |  |
| `airTravel.flightList[n].flightFareBundle` | string | Flight Fare Bundle describes the fare bundle chosen by the user. e.g. Basic, Econo, EconoRewards | Basic, Econo, EconoRewards, EconoFlex, Premium |
| `airTravel.flightList[n].flightArrivalDate` | string | The date upon which a flight is scheduled to arrive (in YYYY-MM-DD format).  | 2021-10-20, 2022-01-31, 2022-03-03 |
| `airTravel.flightList[n].flightNumSegments` | integer | The number of segments between the flight origin and final destination. | 1, 2, 3, 4 |
| `airTravel.flightList[n].flightDepartureDate` | string | The date upon which a flight is scheduled to depart (in YYYY-MM-DD format).  | 2021-10-20, 2022-01-31, 2022-03-03 |
| `airTravel.flightList[n].flightSegmentDuration` | integer | The total duration of the flight segment (in minutes).  | 35, 55, 90, 122 |
| `airTravel.flightList[n].flightSegmentOperator` | string | The airline that operates a flight segment. (e.g. WestJet, Delta) | WestJet, Delta, American Airlines, TWA |
| `airTravel.flightList[n].flightSegmentSequence` | integer | The sequence of a segment withing a flight.  The first segment of a flight is sequence 1. | 1, 2, 3, 4 |
| `airTravel.flightList[n].flightSegmentEquipment` | string | The equipment that flies a flight segment. (e.g. Boeing 737 MAX 8) | Boeing 737-600, Boeing 737 MAX 8, De Havilland Dash8 Q400, Saab 340B, Embraer 175 |
| `airTravel.flightList[n].flightSegmentGuestSeat` | string | Describes the selected seat. May be simple (e.g. '16D') or overloaded (e.g. '3E~3~E~Aisle~NoExitRow') | 3B, 16E, 3E~3~E~Aisle~NoExitRow, 11B~11~B~Middle~ExitRow |
| `airTravel.flightList[n].flightSegmentGuestType` | string | Indicates if the guest is an Adult or Child (or other as desired e.g. Military, Veteran, etc) | Adult, Child, Active Military, Veteran |
| `airTravel.flightList[n].flightSegmentDesignator` | string | A combination of a two character airline code and a numeric flight number. (e.g. WJ1521) | WJ1515, WJ501, DL2745, AA55 |
| `airTravel.flightList[n].flightSegmentGuestCabin` | string | Describes the cabin section where the seat exists. (e.g. economy, economy-plus, premier, business, 1st class) | economy, economy-plus, business, premier, first class |
| `airTravel.flightList[n].flightSegmentGuestNumber` | integer | Indicates to which a seat is assigned in multiple guest bookings.  | 1, 2, 3, 4 |
| `airTravel.flightList[n].flightSegmentGuestSSRCodes` | string | Captures all Special Services Request codes for the guest.  | deaf, blnd~deaf~wchr, blind, no SSR codes |
| `airTravel.flightList[n].flightSegmentGuestSeatCost` | string | The cost of the seat above that included in the fare.  (e.g. 'zero', '19', '27') | zero, 19, 27, 45 |
| `airTravel.flightList[n].flightSegmentSeatSelectionMethod` | string | Indicates the method used for seat selection. This might be 'Unselected' , 'Manual',  'Auto Selection', or 'Auto Selection Failure' | Manual, Auto Selected, AutoSelect Failure |
| `airTravel.flightList[n].flightSegmentAutoSeatSelectionStatus` | string | Indicates if automatic seat selection is avaiable or unavailable for a flight segment. | Available, Unavailable |
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

A summary of all trip selections is displayed to the user for review prior to the collection of payment information.
