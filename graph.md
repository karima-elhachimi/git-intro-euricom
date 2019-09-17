Open https://euri-test-api-phflgvcuay.now.sh/graphql

##Query all users ordered by firstName (retrieve all fields)
query {
  allUsers(orderBy: "firstName") {
    user {
      ...UserFrag
    }
  }
}

fragment UserFrag on User {
  firstName
  lastName
  age
  email
  image
  phone
  company
  address {
    street
    city
    zip
  }
}

##Query a single user and use a variable
Add and complete a task
Query all products (all fields) & basket with products (all fields) in one query.
Add an other product to the basket
When using the basket use a random checkoutID (eg: "123" or "peterBasket") to get your own basket.

