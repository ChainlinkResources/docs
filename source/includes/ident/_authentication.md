## User Authentication

You can build applications that optionally leverage Provide to authenticate your users. Note that the `User` and the associated credentials (i.e., email and password) are the same as the ones used to [login](https://dawn.provide.services/login) to the Provide platform.

> To authorize the creation of a new `Token` on behalf of a platform `User`:

```shell
curl -i -H 'content-type: application/json' \
    https://ident.provide.services/api/v1/authenticate \
    -d '{"email": "vitalik@example.com", "password": "M38&pzQfWNZeBSq$*Qtnzd*f^d8P8RNz"}'
```

> To authorize the creation of a new `Token` on behalf of a platform `Application` (note that the `User` and the associated credentials (i.e., email and password) are specific to the `Application`):

```shell
curl -i -H 'content-type: application/json' \
    https://ident.provide.services/api/v1/authenticate \
    -d '{"email": "vitalik@example.com", "password": "M38&pzQfWNZeBSq$*Qtnzd*f^d8P8RNz", "application_id": "cb2037f7-79fc-40f4-9720-ada636da4183"}'
```

> The above command, regardless of whether or not the `Token` was authorized on behalf of an `Application`, returns JSON structured like this:

```
{
    "user": {
        "id": "40bc70bf-1140-4978-99bc-b8b800672842",
        "created_at": "2018-10-10T17:56:08.047007Z",
        "name": "Vitalik Buterin",
        "email": "vitalik@example.com"
    },
    "token": {
        "id": "862c271e-2bef-4be9-92ce-43ce277f7100",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4ODEwNTQsImp0aSI6Ijg2MmMyNzFlLTJiZWYtNGJlOS05MmNlLTQzY2UyNzdmNzEwMCIsInN1YiI6InVzZXI6M2Q5ZDYyZTgtMGFjZi00N2NkLWI3NGYtNTJjMWY5NmY4Mzk3In0.QQW5purvJbjxUXW51rH4cFReNQMLLOm4oTV2qwvi_AM"
    }
}
```


## Reset Password Request

```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users/reset_password \
    -d '{"email": "vitalik@example.com"}'
HTTP/2 201
```

> Response JSON:

```json
{
    "reset_password_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7Im5hbWUiOiJLeWxlIFRob21hcyJ9LCJleHAiOjE1Njg2MjE1ODIsImlhdCI6MTU2ODYxNzk4MiwianRpIjoiYmUyNjRmYTAtM2Q1OC00Yjk1LTg1ZTktY2MzZGM1ZWI3Y2ZjIiwic3ViIjoidXNlcjo5ZTE1NzkxYS1kYmYxLTRlNWUtOGM2Yi1hNzI1M2UxOThiNGMifQ.vthjA4dkvNz8VXFftyoAhjiT-FANVrEbmIiQ7C4kKzM"
}
```

Initiate a password reset request for a platform `User` or a `User` on behalf of an authorized `Application`, in which case the `Authorization` header is provided containing `Application` credentials.

### Request Parameters

Parameter | Description
--------- | -----------
email | email address for the `User` to initiate the password reset request


## Reset Password

```shell
curl -i -H 'content-type: application/json' \
    https://ident.provide.services/api/v1/users/reset_password/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7Im5hbWUiOiJLeWxlIFRob21hcyJ9LCJleHAiOjE1Njg2MjE1ODIsImlhdCI6MTU2ODYxNzk4MiwianRpIjoiYmUyNjRmYTAtM2Q1OC00Yjk1LTg1ZTktY2MzZGM1ZWI3Y2ZjIiwic3ViIjoidXNlcjo5ZTE1NzkxYS1kYmYxLTRlNWUtOGM2Yi1hNzI1M2UxOThiNGMifQ.vthjA4dkvNz8VXFftyoAhjiT-FANVrEbmIiQ7C4kKzM \
    -d '{"password": "the new password"}'
HTTP/2 204
```

Complete a password reset request for a platform `User` or a `User` on behalf of an authorized `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
token | reset password token acquired in the reset password request

### Request Parameters

Parameter | Description
--------- | -----------
password | the new password for the `User`