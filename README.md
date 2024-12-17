# Travel API Integration  

This repository provides examples and utilities for interacting with a suite of APIs designed for travel-related applications. These APIs enable you to fetch information about activities, airports, hotels, weather, and geographic coordinates for various destinations.  

## Table of Contents  
- [Overview](#overview)  
- [Available Endpoints](#available-endpoints)  
  - [Activities](#activities)  
  - [Airport Search](#airport-search)  
  - [Hotel Search](#hotel-search)  
  - [Weather Information](#weather-information)  
  - [Geographic Coordinates](#geographic-coordinates)  
- [Usage](#usage)  
- [License](#license)  

---

## Overview  
This repository integrates with the `m2.eeazy.se/rapapi` APIs, which offer a robust set of endpoints to support travel applications. With these APIs, you can provide your users with:  
- Recommended activities based on location and travel dates.  
- Nearby airports for a given location.  
- Hotel search functionality for destinations.  
- Real-time weather data.  
- Geographic coordinates for mapping purposes.  

---

## Available Endpoints  

### 1. **Activities**  
Fetch a list of activities available for a specific city on given dates.  

**Endpoint:**  
```plaintext  
https://m2.eeazy.se/rapapi/activity/activities?city=${destination}&date=${date}&adult=${adults}&child=${children}  
```

**Parameters:**  
- `destination` (string): City name where activities are to be searched.  
- `date` (string): Activity date in `YYYY-MM-DD` format.  
- `adults` (integer): Number of adults.  
- `children` (integer): Number of children.  

### 2. **Airport Search**  
Retrieve information about airports near a specific location.  

**Endpoint:**  
```plaintext  
https://m2.eeazy.se/rapapi/airport?location=${encodeURIComponent(query)}  
```

**Parameters:**  
- `query` (string): Name of the location to search for nearby airports.  

### 3. **Hotel Search**  
Find hotels in a given city.  

**Endpoints:**  
1. Basic hotel search:  
   ```plaintext  
   https://m2.eeazy.se/rapapi/hotel/search?city=${destination}  
   ```
   
2. Hotel details with occupancy:  
   ```plaintext  
   https://m2.eeazy.se/rapapi/hotel/hotels?city=${destination}&adult=${adults}&child=${children}  
   ```

**Parameters:**  
- `destination` (string): City name to search for hotels.  
- `adults` (integer): Number of adults staying.  
- `children` (integer): Number of children staying.  

### 4. **Weather Information**  
Get real-time weather data for a specific city.  

**Endpoint:**  
```plaintext  
https://m2.eeazy.se/rapapi/weather/search?city=${destination}&apikey=${apiKey}&units=metric  
```

**Parameters:**  
- `destination` (string): City name for weather information.  
- `apiKey` (string): Your API key for authentication.  
- `units` (string): Unit of measurement (e.g., `metric` for Celsius).  

### 5. **Geographic Coordinates**  
Fetch latitude and longitude coordinates for a given city.  

**Endpoint:**  
```plaintext  
https://m2.eeazy.se/rapapi/coordinates?city=${city}  
```

**Parameters:**  
- `city` (string): City name to fetch geographic coordinates.  

---

## Usage  
1. Make sure you have an API key (if required) to access the endpoints (ask me and you will get API-key if needed for a schoolproject etc..).  
2. Use the provided endpoints in your application by replacing the placeholder variables (`${}`) with actual values.  
3. Refer to the API documentation above for required parameters and endpoint details.  

---

## License  
This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
