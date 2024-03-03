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

## Authorization

If you are using the FREE plan, You don't need to implement this part.

In order to send unlimited api requests you can either whitelist your [Domain or IP address](https://freeipapi.com/ip-addresses) in the dashboard after your subscribed to the unlimited plan or use an API Key.

To use an API Key you need to first subscribe to the Unlimited plan and then [generate an API Key](https://freeipapi.com/api-keys) in the dashboard.

Then you will need to send the API Key in the header of your requests as `Bearer` token.

| Header        | Type   | Example                                         |
|---------------|--------|-------------------------------------------------|
| Authorization | Bearer | `Authorization: Bearer TOKEN`                   |