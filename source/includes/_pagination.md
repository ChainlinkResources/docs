# Pagination

Collection endpoints which return large datasets support the following pagination query parameters:

Query Param | Purpose
---------- | -------
`page` | The `1`-based page number being requested
`rpp` | The results per page being requested

When no `page` and `rpp` parameters are provided in the query, sane defaults (i.e., `page=1&rpp=25` will be applied based on the resource being requested.

An `X-Total-Results-Count` header is provided in the response as a hint indicating how many total results exist for the requested resource, all filters applied.

The `Range` and `Content-Range` entity headers are not currently supported for pagination.
