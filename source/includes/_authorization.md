# Authorization

Provide uses API tokens to authorize the vast majority of platform requests. An API token is encoded using JWT, signed, and contains a representation of the authorized entity in the JWT subject (`sub`). Unless otherwise noted, all requests must include a `Authorization` header such as:

`Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64`

The `bearer` authorization header is scoped to an authorized platform `User` or an `Application` as described above. This header may contain a sub to further limit scope to a specific token, smart contract, wallet or other entity.
