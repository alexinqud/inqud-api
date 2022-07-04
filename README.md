### [!!!] This documentation is no longer maintained. For the latest Inqud documentation please refer to https://docs.inqud.com/

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
#### Bank codes IDR
```
CIMB - CIMB Bank
BNI - BNI Bank
BCA - BCA Bank
PERMATA - PERMATA Bank
```
#### Channel codes IDR
```
BT - Permata Bank Virtual Account
I1 - BNI Virtual Account
M1 - Mandiri Virtual Account
RI - Bank Rakyat Indonesia
QRIS - QRIS
```
