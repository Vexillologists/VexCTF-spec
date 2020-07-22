# GraphQL

VexCTF uses GraphQL for almost all API features. This is excluding some things like file upload which uses REST.

## Endpoint Requirements

The following GraphQL endpoint(s) must be implemented: 
- `/graphql`: A GraphQL endpoint using HTTP `POST` requests.

The request and response must be in JSON format and have a `Content-Type` header of `application/json`.

Any further GraphQL endpoint(s) may be implemented as long as they do not conflict with existing endpoints.

## GraphQL Feature Requirements

It is required that introspection must be enabled within the GraphQL implementation of choice.

Any further GraphQL features are entirely optional.

## Recommendations

It is recommended that a graphical interface for GraphQL (e.g. GraphiQL, GraphQL Playground, etc.) is implemented, as they highly aid in debugging. However, this is optional in production environments. In the case that one is implemented, it can be on any endpoint, as long as it does not conflict with existing endpoints.