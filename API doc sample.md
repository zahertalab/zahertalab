**Weather Information API - Get Weather by Location**

This API endpoint allows users to query weather information based on a specific location.

**Endpoint URL:**
```
https://api.weatherdata.io/v1/weather
```

**HTTP Method:**
```
GET
```

**Parameters:**

1. **API Key (Required)**

   The API key is required to access the Weather Information API. You can obtain your unique API key by signing up on the WeatherData website.

   Parameter name: `api_key`
   - Type: String
   - Example: `api_key=abcdef1234567890`

2. **Location (Required)**

   The location for which the weather information is requested.

   Parameter name: `location`
   - Type: String
   - Example: `location=Amman`

3. **Units (Optional)**

   The unit system to be used for temperature and other measurements.

   Parameter name: `units`
   - Type: String
   - Accepted values: `metric`, `imperial`
   - Default: `metric`
   - Example: `units=metric`

**Response Format:**

The API response will be in JSON format, containing weather information for the requested location.

**Example Usage:**

**Request:**
```
GET https://api.weatherdata.io/v1/weather?api_key=abcdef1234567890&location=Amman&units=metric
```

**Response:**
```json
{
    "location": "Amman",
    "latitude": 31.9566,
    "longitude": 35.9456,
    "weather": "Sunny",
    "temperature": 30.2,
    "humidity": 45,
    "wind_speed": 5.6,
    "wind_direction": "SE",
    "pressure": 1012.1,
    "description": "Clear sky with gentle breeze",
    "icon_url": "https://api.weatherdata.io/icons/sunny.png",
    "timestamp": "2023-07-21T12:00:00"
}
```

**Response Explanation:**

- `location`: The name of the requested location.
- `latitude`: The latitude of the location.
- `longitude`: The longitude of the location.
- `weather`: The current weather condition at the location.
- `temperature`: The current temperature at the location (in Celsius since `units=metric` was specified).
- `humidity`: The relative humidity percentage at the location.
- `wind_speed`: The wind speed at the location (in meters per second since `units=metric` was specified).
- `wind_direction`: The wind direction at the location.
- `pressure`: The atmospheric pressure at the location.
- `description`: A brief description of the weather condition.
- `icon_url`: URL to an icon representing the weather condition.
- `timestamp`: The date and time of the weather data.

Please ensure to use the correct API key (`abcdef1234567890` in this example) to make successful requests.
