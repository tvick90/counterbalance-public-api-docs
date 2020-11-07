# Getting Started
The Counterbalance API is crafted around REST and the REST architectural style to provide developers with a stateless and language ­agnostic interface. The API leverages HTTP verbs and response codes, JWT authentication, and resource-oriented URLs.

---

## Making Requests
The API host is `https://api.counterbalance.io/v1/`

> _**Note** The API is only available via HTTPS_


### Authenticating Requests
The authentication requirement for each endpoint varies. If authentication is required, an Authorization header must be provided as described in [Authentication](./Authentication.md).

### Supported HTTP Operations
The API supports the `GET`,`POST`,`PUT`,`PATCH`,`DELETE`, & `OPTIONS` verbs. General usage of these verbs is outlined in the following table.

Verb | Description
-----|------------
`GET`     | Retrieves existing resources
`POST`    | Creates a new resource and returns it
`PUT`     | Creates a new resource within or attached to an existing resource and returns the new resource
`PATCH`   | Updates an existing resource and returns the updated resource
`DELETE`  | Removes an existing resource and returns nothing
`OPTIONS` | List available verbs against a resource

### Responses
Working with responses and errors is documented in [Responses & Errors](./Responses-and-Errors.md)

---

## Formatting Requests
The API is crafted around simple, resource-oriented URLs. Resource objects are accessed and manipulated in predictable ways via their UUID and common HTTP verbs.

For example, the request:
```
GET https://api.counterbalance.io/v1/foo/497f6eca-6276-4993-bfeb-53cbbbba6f08 HTTP/1.1
```

Returns the _foo_ object with UUID `497f6eca-6276-4993-bfeb-53cbbbba6f08` in JSON format

### URL Parameters
URL query paramaters are not currently supported.

### Forming a Request Body
When submitting non-binary data via a `POST`, `PUT`, or `PATCH` endpoint, the data payload must be in JSON.
```
POST https://api.counterbalance.io/v1/foo HTTP/1.1
Content-Type: application/json
```
```json
{
  "bar": "baz"
}
```


