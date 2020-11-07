# Welcome

**Welcome to the Counterbalance API:** powerful, programmatic access to the Counterbalance platform and its feature-rich IT management toolset. This documentation walks through the API endpoints and their usage. 

The Counterbalance API is crafted around REST and the REST architectural style to provide developers with a stateless and language ­agnostic interface. The API leverages HTTP verbs and response codes, JWT authentication, and resource-oriented URLs.

## Making Requests
The API exclusively accepts and returns JSON data unless otherwise indicated. All requests should include a content-type header as shown:

```
Content-Type: application/json
```