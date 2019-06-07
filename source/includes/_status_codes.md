# Status Codes

The following status codes describe Provide API responses:

Status Code | Meaning
---------- | -------
`200 OK` | The request was successful
`201 Created` | The request was successful and a new entity was created
`202 Accepted` | The request was successfully accepted and processing will complete asynchronously
`204 No Content` | The request was successful but did not return a response
`401 Unauthorized` | The request required an API `Authorization` header, or one was provided which could not be authenticated
`403 Forbidden` | The supplied API `Authorization` header does not have permission to access the requested resource
`404 Not Found` | Platform did not find the requested resource
`429 Too Many Requests` | The request was not accepted due to exceeding the rate limit
`500 Internal Server Error` | The request resulted in an internal error during processing
`501 Not Implemented` | The requested resource is not implemented by the platform
`503 Service Unavailable` | The request cannot be fulfiled due to temporary unavailability of a backend service
