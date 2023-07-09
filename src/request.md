# Request

## Endpoint

The base URL for the API is `https://freeipapi.com`

You may use the following endpoint for the IP queries

```
GET /api/json/{IP-ADDRESS}
```

Replace `{IP-ADDRESS}` with the IP address that you want to query.


## Headers

| Parameter     | Type   | Required | Description                                     |
|---------------|--------|----------|-------------------------------------------------|
| Authorization | bearer | No       | If you have an API Key, you may pass this header.|


## Parameters

| Parameter | Type   | Required | Description                                     |
|-----------|--------|----------|-------------------------------------------------|
| IP-ADDRESS| string | Yes      | The IP address for which geolocation is needed.|

## Authentication

If you have subscribed to a [paid plan](https://freeipapi.com/#pricing), To use the new rate-limit offered in the plan, It is required to pass your API Key in the `Authorization` field of the request's headers.

For example:

```
Authorization: Bearer {API_KEY}
```

Replace `{API_KEY}` with your API Key which you can get it from your dashbaord > API Keys section.
