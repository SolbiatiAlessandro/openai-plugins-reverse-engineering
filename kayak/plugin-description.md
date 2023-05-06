The KAYAK plugin provides a set of functionalities related to travel planning. It includes the following types:

1. `searchFlights`: This type is used to search for flights on a specific route for certain dates. The fields it can take are:
   - `origin`: The origin from which the flight starts.
   - `destination`: The destination to which the flight goes.
   - `departDate`: Departure date of the flight at the origin.
   - `returnDate`: Return date of the flight.
   - `cabinClass`: Flight cabin class. It can be "economy", "premium_economy", "business", or "first".
   - `numAdults`: Number of adults that are flying.
   - `numChildren`: Number of children that are flying.
   - `nonStopOnly`: If set to true, only non-stop flights will be shown.

2. `searchStays`: This type is used to search for accommodations for certain dates. The fields it can take are:
   - `destination`: The city where you need a stay.
   - `landmark`: Optional landmark to refine the location.
   - `address`: Optional address to refine the location.
   - `checkinDate`: Check in date.
   - `checkoutDate`: Check out date.
   - `numAdults`: Number of adults that are staying.
   - `numChildren`: Number of children that are staying.
   - `numRooms`: Number of rooms needed.
   - `minNumStars`: Minimum number of stars the accommodation should have.

3. `searchCars`: This type is used to search for rental cars for certain dates. The fields it can take are:
   - `origin`: The location where you want to pick your rental car.
   - `destination`: The location where you want to drop off your rental car.
   - `pickupDate`: The date when you want to pick up your rental car.
   - `pickupHour`: Rental car pick up hour in 24-hour format.
   - `dropoffDate`: The date when you want to drop off your rental car.
   - `dropoffHour`: Rental car drop off hour in 24-hour format.

4. `explore`: This type is used to find places to go on a budget. The fields it can take are:
   - `origin`: The origin from which the flight starts.
   - `destinationHints`: Optional list of cities that are requested to be included in the results.
   - `departDate`: Departure date of the flight at the origin.
   - `returnDate`: Return date of the flight.
   - `budgetUsd`: Expected cost of round trip flight ticket for one person.
   - `nonStopOnly`: If set to true, only non-stop flights will be shown.
   - `useExactDates`: Set to true if travel on specific dates is requested.
   - `minDays`: Minimum duration that the suggested trips should have.
   - `maxDays`: Maximum duration that the suggested trips should have.

5. `flightInsights`: This type can be used when the flight route is known yet the travel dates are flexible. The fields it can take are:
   - `origin`: The origin from which the flight starts.
   - `destination`: The destination to which the flight goes.
   - `departDate`: Departure date of the flight at the origin.
   - `returnDate`: Return date of the flight.
   - `nonStopOnly`: If set to true, only non-stop flights will be shown.

Each of these types returns a different set of data based on the input parameters, helping users to plan their travel by searching for flights, accommodations, and rental cars, exploring destinations within
