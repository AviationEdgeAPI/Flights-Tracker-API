# Flights-Tracker-API
Aviation Edge <a href="https://aviation-edge.com/flight-radar-and-tracker-api/"> Flights Tracker API</a> a JSON REST API that provides real-time location data of live, airborne flights worldwide. It generally covers ADS-B flights with a small amount of radar flights. The data is gathered from multiple sources, aggregated in  our servers and provided to API users in a constantly updated manner in real-time.

### Documentation
You may find input parameters, output examples with explanations for each item, filter list, and more in the [documentation](https://aviation-edge.com/developers/), also available as a [GitHub repository](https://github.com/AviationEdgeAPI/aviation-edge-api). 

### Example Fields of Use
- Virtual maps for flight tracking
- Airport greeting and transportation services
- Route analysis
- Fuel consumption analysis
- Flight simulation

### Response
Data of all live flights in the world in one call:

**GET** http://aviation-edge.com/v2/public/flights?key=[API_KEY]&limit=30000

Specific flight based on flight number:

**GET** http://aviation-edge.com/v2/public/flights?key=[API_KEY]&flightIata=W8519

All flights of a specific airline:

**GET** http://aviation-edge.com/v2/public/flights?key=[API_KEY]&airlineIata=W8

Flights from a departure location:

GET http://aviation-edge.com/v2/public/flights?key=[API_KEY]&depIata=MAD

Flights to an arrival location:

**GET** http://aviation-edge.com/v2/public/flights?key=[API_KEY]&arrIata=GIG

Flights within a circle area based on lat and lng values and radius as the distance:

**GET** https://aviation-edge.com/v2/public/flights?key=[API_KEY]&lat=51.5074&lng=0.1278&distance=100&arrIata=LHR

Combinations: two airports and a specific airline flying between them:

**GET** http://aviation-edge.com/v2/public/flights?key=[API_KEY]&depIata=ATL&arrIata=ORD&airlineIata=UA

```

[
{"aircraft":
{
"iataCode":"B77W",
"icao24":"C0173A",
"icaoCode":"B77W",
"regNumber":"C-FIUR"
},
"airline":
{"iataCode":"AC",
"icaoCode":"ACA"
},
"arrival":
{"iataCode":"YYZ",
"icaoCode":"CYYZ"
},
"departure":
{"iataCode":"GRU",
"icaoCode":"SBGR"
},
"flight":
{"iataNumber":"AC91",
"icaoNumber":"ACA091",
"number":"91"
},
"geography":
{"altitude":10363.2,
"direction":342.0,
"latitude":23.36,
"longitude":-70.37
},
"speed":
{"horizontal":820.436,
"isGround":0.0,
"vspeed":0.0},
"status":"en-route",
"system":
{"squawk":null,
"updated":1643111484}
}
]
```

### Access & Support
[Contact us](https://aviation-edge.com/contact/) via email for any questions or support requests.

[Get your API key](https://aviation-edge.com/premium-api/) in a minute and start testing the data right away. The API is provided through API subscriptions. All plans grant access to the Flights Tracker API and other APIs with a difference of the monthly API call limit. Choose the best plan for you and upgrade, downgrade or cancel your plan anytime without  commitments.

### License
The use of the API is subject to Aviation Edge [Terms and Conditions](https://aviation-edge.com/api-terms-of-service/).
