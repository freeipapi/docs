# Response

## Fields

The API response will be a JSON object containing the following fields:

| Field          | Type   | Description                                       |
|----------------|--------|---------------------------------------------------|
| ipVersion      | string | The IP version (e.g., 4 for IPv4).              |
| ipAddress      | string | The IP address for which geolocation information is provided. |
| latitude       | string | The latitude coordinate of the IP address location.|
| longitude      | string | The longitude coordinate of the IP address location.|
| countryName    | string | The name of the country where the IP address is located.|
| countryCode    | string | The ISO 3166-1 alpha-2 country code of the IP address location.|
| timeZone       | string | The time zone offset of the IP address location.|
| zipCode        | string | The ZIP code or postal code of the IP address location.|
| cityName       | string | The name of the city where the IP address is located.|
| regionName     | string | The name of the region or state where the IP address is located.|
| continent      | string | The name of the continent where the IP address is located.|
| continentCode  | string | The ISO code of the continent where the IP address is located.|

## Status Codes

The API uses standard HTTP status codes to indicate the success or failure of a request. Below are the common status codes returned by the API:

| Status Code | Description |
|-------------|-------------|
| 200         | OK - The request was successful and the response is valid.|
| 422         | Bad Request - The request was invalid or malformed.|
| 404         | Not Found - The requested resource was not found.|
| 429         | Too Many Requests - The rate limit for the API has been exceeded.|
| 500         | Internal Server Error - An error occurred on the server.|


## Example Response

```json
{
 "ipVersion": 4,
 "ipAddress": "77.111.245.13",
 "latitude": 58.416588,
 "longitude": 15.616713,
 "countryName": "Sweden",
 "countryCode": "SE",
 "timeZone": "+02:00",
 "zipCode": "58957",
 "cityName": "Linkoping",
 "regionName": "Ostergotlands lan",
 "continent": "Europe",
 "continentCode": "EU"
}
```