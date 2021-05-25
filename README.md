# Micronaut GraphQL Graal

Test application for Micronaut GraphQL and GraalVM.

To test the application:

```
curl -X POST 'http://localhost:8080/graphql' \
               -H 'content-type: application/json' \
               --data-binary '{"query":"{ bookById(id:\"book-1\") { name, pageCount, author { firstName, lastName} }  }"}'
```

Or open http://localhost:8080/graphiql and send the query:

```graphql
query {
    bookById(id:"book-1") {
        name,
        pageCount,
        author {
            firstName
            lastName
        },
    }
}
```
