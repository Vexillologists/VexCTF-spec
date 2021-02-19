# Overview of Server Architecture

## GraphQL

VexCTF uses [GraphQL](https://graphql.org) for many features of its API. Terminology and normative requirements for GraphQL should be interpreted as in the [June 2018 edition of the GraphQL specification](https://spec.graphql.org/June2018).

### GraphQL Endpoint Requirements

#### Location

The GraphQL endpoint must be hosted at `/graphql` relative to the server's root. For example:

```example
https://ctf.example.com/graphql
https://example.com/ctf/graphql
```

Endpoints that are not at this location, such as this one, are disallowed, and will not work well with pre-existing clients without modifications:

```counter-example
https://example.com/api
```

#### GraphQL Features

The GraphQL endpoint must allow introspection. Timing and other profiling information, however, is optional but potentially recommended in development environments.

GraphiQL or other visual interfaces to the GraphQL API are not required but are recommended in development environments. These may be hosted at any endpoint given that it does not interfere with regular API operation. It is suggested that it is hosted at `/graphql` (only on GET requests) or at `/graphiql`.

The GraphQL endpoint must accept valid POST requests. GET requests are not recommended but are not required nor disallowed.

The GraphQL endpoint must allow the following MIME types:
- `application/json`
- `application/x-www-form-urlencoded`

It is recommended that the endpoint accept the `application/graphql` content-type but this is optional.

### GraphQL Architecture Design

To facilitate better interaction with the GraphQL API, VexCTF aims to follow the [Relay](https://relay.dev) [connection specification](https://relay.dev/graphql/connections.htm) as well as the [GraphQL Global Object Identification](https://graphql.org/learn/global-object-identification/) pattern.
