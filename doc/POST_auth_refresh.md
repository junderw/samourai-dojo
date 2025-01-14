# Refresh the access token

Request a new access token from the backend. A valid refresh token must be passed as an argument or through the `Authorization` HTTP header (with the `Bearer` scheme).


```
POST /auth/refresh
```

## Parameters
* **rt** - `string` - A valid refresh token


### Example

```
POST /auth/refresh?rt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJTYW1vdXJhaSBXYWxsZXQgYmFja2VuZCIsInR5cGUiOiJyZWZyZXNoLXRva2VuIiwiaWF0IjoxNTQ0MTAzOTI5LCJleHAiOjE1NDQxMTExMjl9.6gykKq31WL4Jq7hfmoTwi1fpmBTtAeFb4KjfmSO6l00
```

#### Success
Status code 200 with JSON response:
```json
{
  "authorizations": {
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJTYW1vdXJhaSBXYWxsZXQgYmFja2VuZCIsInR5cGUiOiJhY2Nlc3MtdG9rZW4iLCJpYXQiOjE1NDQxMDM5MjksImV4cCI6MTU0NDEwNDUyOX0.DDzz0EUEQS8vqdhfUwi_MFhjnSLKZ9nY-P55Yoi0wlI"
  }
}
```

#### Failure
Status code 401
