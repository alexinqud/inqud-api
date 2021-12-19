# General

- The base endpoint is: **https://api.inqud.com**
- All endpoints return either a JSON object or array.
- All time and timestamp related fields are in **UTC time**.
- Datetime example: "2018-12-04T12:02:35.14Z"

[OpenAPI](openapi.yml)

[Authentication](authentication.md)

[Callbacks](callback.md)

### Dictionary
#### Pyment statuses
```
NEW
SUCCESS
PARTIAL_SUCCESS
FAILED
EXPIRED
PENDING
CANCELLED
FROZEN
```
#### Payment method types
```
CRYPTOCOIN
CC_VISAMC
QIWI
```