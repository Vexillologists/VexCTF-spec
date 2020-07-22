# Authentication

Authentication in VexCTF uses JSON Web Tokens (JWTs) as described in [RFC 7519](https://tools.ietf.org/html/rfc7519). 

Tokens should be passed by the `Authorization` header with type `Bearer` (in uppercase).
For example:
```http
POST /graphql
Authorization: Bearer eyJhbG...shortened for example...lRTcIeq6vlpAv0
Content-Type: application/json
```

All GraphQL queries and mutations, as well as any REST APIs are assumed to require authentication, unless explicitly specified.

## Token Requirements

The JWT session token must contain the following fields:
- `exp`: The expiry timestamp as a UNIX timestamp in seconds.
- `jti`: The internal session ID, in any form. This is usually used to allow server-side expiry/validity information and revokation.
- `uid`: The user's Node ID.

The signature may be generated with any algorithm in the JWT specification, however it is recommended that any `HMACSHAnnn`-based (`HSnnn`) algorithm is used as they are typically more supported than others.

Any other application-specific fields are allowed but a basic implementation will usually only need the required fields.