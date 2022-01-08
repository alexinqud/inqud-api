# Authentication

Bellow you can find the request headers which are using for the token
based authentication:


**Simple approach**:
```
X-Token-API-Id - Identifier of the token (started with TKN- prefix)
X-Token-Secret - Token secret
```

**HmacSHA256**:
```
X-Token-API-Id - Identifier of the token (started with TKN- prefix)
X-HMAC-SHA256-Signature - HMAC Signature
X-Salt - Salt (nonce)
```

Signature = HmacSHA256 function of (Request body + salt) hashed by token
secret in HEX

For GET request just use "" as a body parameter

## Python Example


Here is an example how to get a balance with the signature of the request
in python


```
import requests

id = 'TKN-6c1296b8-6929-443b-ac06-f732e0e27be1'
secret = "dBajIp3wHnw5euxohPiZvsCEorG3Fhl9gsHl1UIBlsImHjWRdSJdp4Gh6e3y2PNs"


headers = {}
headers['X-Token-API-Id'] = id
headers['X-Token-API-Secret'] = secret


url = 'https://api.inqud.com/v1/user/wallet/balances'

http_response = requests.get(url=url, headers=headers)


print(str(http_response.content.decode()))

```



HmacSHA256 example


```
import hashlib
import hmac
import requests


salt = "someSalt"
data = "" + salt

token_id = "TKN-6c1296b8-6929-443b-ac06-f732e0e27be1"

token_secret = "dBajIp3wHnw5euxohPiZvsCEorG3Fhl9gsHl1UIBlsImHjWRdSJdp4Gh6e3y2PNs"


dig = hmac.new(token_secret.encode('utf-8'), msg=data.encode('utf-8'),
digestmod=hashlib.sha256).digest()

signature = dig.hex()


headers = {'X-Token-API-Id': token_id,
         'X-HMAC-SHA256-Signature': signature,
         'X-Salt': salt}

url = 'https://api.inqud.com/v1/user/wallet/balances'

http_response = requests.get(url=url, headers=headers)

```
