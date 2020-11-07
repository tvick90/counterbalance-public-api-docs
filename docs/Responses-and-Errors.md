# Responses & Errors

All responses are returned in JSON format unless otherwise specified. The returned content will always be identified with a `Content-Type` header.

## Status Codes

All possible status codes are outlined below.

### Success Responses

Successful API calls will return one of these HTTP 2XX status codes:

Code | Response | Description
-----|----------|---------
**200** | `Ok` | The request was completed successfully. Response body will vary.
**201** | `Created` | In response to a PUT or POST request, the resource was created successfully. The new resource's ID will be returned in the response body.
**204** | `No Content` | The request was completed successfully and there is no response body to return. Such as when an object has been deleted. 


### Errors

Unsuccessful API calls will return one of the these HTTP 4XX or 5XX status codes:

Code | Response | Description
-----|----------|---------
**400** | `Bad Request` | The request was malformed, provided incorrect/incomplete/conflicting parameters, or the requested endpoint does not exist. The response body will contain additional information about why the error has occurred. Do not repeat the request without modifying it first.
**401** | `Unauthorized` | The request requires an Authorization header and a valid token but either neither was provided or the provided token has expired. Refer to the error message provided to determine the proper course of action. 
**403** | `Forbidden` | The API authentication was successful but the user does not have adequate permissions to satisfy the request or the tenant account is locked.
**404** | `Not Found` | The resource requested does not exist or was not found.
**409** | `Conflict` | The provided combination of parameters results in a conflict and the resource cannot be updated. The error message output will provide additional information as to why the call cannot be completed.
**5XX** | _`varies`_ | The API encountered an internal error when processing the request. The error message provided may provide additional information. Retrying the request after a few minutes may be successful.


## Error Logging

Most errors are automatically logged and reported and these errors will return a `logging_hash` entry ID in the error response body.

```json
{
    "error": {
        ...
    },
    "logging_hash": "034dd6ad00770337bb07e906d919ed50f8884e86"
}
```

This entry ID is also added as a header in the response.

```
X-Counterbalance-Log-Hash: 034dd6ad00770337bb07e906d919ed50f8884e86
```

## Additional Response Headers

The following table outlines additional headers that may be included in API responses.

Header | Description
-------|------------
`X-Counterbalance-Compute-Node` | The API container that processed this request