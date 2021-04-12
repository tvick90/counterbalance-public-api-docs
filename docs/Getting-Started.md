# Getting Started
The **Counterbalance Core API** provides powerful, programmatic access to the Counterbalance platform and powers its feature-rich building management UI. Everything that is possible via the [Counterbalance System Console](https://app.counterbalance.io) is powered by this API.

This documentation walks through the API endpoints and their usage.

## Making Requests
The API is crafted around REST and the REST architectural style to provide developers with a stateless and language ­agnostic interface.

The root API host for the endpoints outlined in this documentation is `https://api.counterbalance.io/`

<!-- theme: success -->
> _The API is only available via HTTPS_

The API employs simple, resource-oriented URLs. Resource objects are accessed and manipulated in predictable ways via their UUID and common HTTP verbs.

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

## Submitting Data
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

Procedures for submitting other types of data to the API are documented on a per-endpoint basis. 

## Authenticating Requests
The authentication requirement for each endpoint varies. If authentication is required, authorization must be provided as described in [Authentication](./Authentication.md).

### Request Authorization
Some API endpoints require a paid subscription. If a request is made to a paid feature that is not available, a `403 Forbidden` response will be returned. 

Additionally, some platform resources and features are measured against a licensed quota limit. If an attempt is made to add additional resources once a quota limit has been reached, a `403 Forbidden` response will be returned.

