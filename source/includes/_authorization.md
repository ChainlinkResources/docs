# Authorization

Provide requires an API token to authorize the vast majority of platform requests. An API token is encoded using JWT, signed, and contains a representation of the authorized entity (i.e., a `User` or `Application` which owns the `Token`) in the JWT subject (`sub`). Unless otherwise noted, all requests must include a header such as: `Authorization: bearer <JWT>`.

The bearer `Authorization` header is scoped to an authorized platform `User` or an `Application` as described above.
