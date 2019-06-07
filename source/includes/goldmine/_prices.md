# Prices

## List Prices

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/prices
HTTP/2 200
```

> Response JSON:

```json
{
    "btcusd": 14105.2,
    "ethusd": 707,
    "ltcusd": 244.48,
    "prvdusd": 0.42
}
```

This endpoint retrieves real-time pricing data for major currency pairs and supported tokens.


### HTTP Request

`GET /api/v1/prices`
