# Callbacks

Callback will be invoked after each step during payment processing:

HTTP Method: POST
```

{
  "paymentId":"PMT-4f333be0-bf14-4756-b226-a6e252236eeb",
  "orderId":"ORD-59b58494-def7-4d9b-89e7-30fddba2abc6",
  "userId":"OWN-1f6280a8-372f-488b-89bf-2e54c6a98bb4",
  "status":"SUCCESS",
  "orderType":"PAYIN",
  "amount":1,
  "currency":"BTC",
  "timestamp":"2020-02-14T14:29:00.937Z"
}
```
## Setup callback:

You have to execute POST request with user settings "callback.url" where
value is your endpoint. 


**User Settings**


#### Retry iterations:

1, 2, 5, 15, 30, 60, 120, 360, 720, 1440 minutes


#### Expected http code:

200 OK