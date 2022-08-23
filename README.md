- quais problemas graphql resolve ?
  - Overfetching
    - http://localhost:3000/users
      - DB (usuários,endereços)
  - Underfetching
    - http://localhost:3000/users
      - DB(usuários)
    - http://localhost:3000/addresses

// http://localhost:3000/graphql

Dificuldades :

- Cache
- Erros

```gql
query {
  users {
    id
    name
    github

    addresses {
      city
      state
      country
    }
  }
}
```

http://localhost:3000/users

Cache-control: 5 segundos

http://localhost:3000/graphql
