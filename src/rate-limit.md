# Rate Limiting

The freeipapi.com API has a rate limit of 60 requests per minute on the FREE plan. If you exceed this limit, you will
receive a status code indicating that you have reached the rate limit. Please ensure that your application adheres to
this limit to avoid disruptions.

If you hit the limit you may receive `429` HTTP Error code the responses.

The rate limit may be vary for the paid plans. For more information check our [pricing](https://freeipapi.com/#pricing)