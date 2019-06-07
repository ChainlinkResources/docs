## User Authentication

You can build applications that leverage Provide to authenticate your users. Note that the `User` and the associated credentials (i.e., email and password) are the same as the ones used to [login](https://dawn.provide.services/login) to the Provide platform.

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
