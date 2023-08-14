# Request

## Endpoint

The base URL for the API is `https://freeipapi.com`

You may use the following endpoint for the IP queries

```
GET /api/json/{IP-ADDRESS}
```

Replace `{IP-ADDRESS}` with the IP address that you want to query.

Or don't replace the `{IP-ADDRESS}` to get the information of the request sender.

## Parameters

| Parameter | Type   | Required | Description                                     |
|-----------|--------|----------|-------------------------------------------------|
| IP-ADDRESS| string | No       | The IP address for which geolocation is needed. |


**Note**: If you don't send the `IP-ADDRESS`, The API will return you the geolocation information of the sender (Who makes the request)
