# Making Requests
The Counterbalance API is crafted around REST and the REST architectural style to provide developers with a stateless and language ­agnostic interface. The API leverages HTTP verbs and response codes, JWT authentication, and resource-oriented URLs.

---

## Making Requests
The API host is always `https://api.counterbalance.io/v1/`

> _**Note** The API is only available via HTTPS_


### Authenticating Requests
The authentication requirement for each endpoint varies. If authentication is required, an Authorization header must be provided as described in [Authentication](./Authentication.md).

### Supported HTTP Operations
The API supports the `GET`,`POST`,`PUT`,`PATCH`,`DELETE`, & `OPTIONS` verbs. General usage of these verbs is outlined in the following table.

Verb | Description
-----|------------
`GET`     | Retrieves a single resource or a group of resources
`POST`    | Creates a new resource
`PUT`     | Creates a new resource within or attached to an existing resource
`PATCH`   | Updates an existing resource
`DELETE`  | Removes an existing resource
`OPTIONS` | List available verbs against a resource

Standard responses and errors are documented in [Responses & Errors](./Responses-and-Errors.md)

### Data Format
The API returns data in a variety of formats depending on the endpoint used. When exchanging non-binary data, the API accepts and returns JSON. 

---

## Formatting Requests
The API is crafted around simple, resource-oriented URLs. Resource objects are accessed and manipulated in predictable ways via their UUID and common HTTP verbs.

For example, the request:
```
GET https://api.counterbalance.io/v1/user/497f6eca-6276-4993-bfeb-53cbbbba6f08 HTTP/1.1
```

Will return the user account object for the user with UUID `497f6eca-6276-4993-bfeb-53cbbbba6f08` in JSON format

### Forming a Request Body