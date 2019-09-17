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
mutation {
  addTask(desc: "this is a new task") {
    task {
      desc
    }
  }
}

mutation completeMyTask($taskId: Int!) {
  completeTask(id: $taskId) {
    task {
      id
      desc
      completed
    }
  }
}

{
  "taskId": 8
}

##Query all products (all fields) & basket with products (all fields) in one query.
query {
  allProducts(first: 1) {
    product {
      ...ProductFrag
    }
  }
  basket(checkoutID: "test") {
    items {
      id
      product {
        ...ProductFrag
      }
    }
  }
}

fragment ProductFrag on Product {
  id
  sku
  title
  desc
  image
  stocked
  basePrice
  price
}


##Add an other product to the basket
mutation {
  addItemToBasket(
    input: { checkoutID: "test", item: { quantity: 2, productId: 1 } }
  ) {
    basket {
      checkoutID
      items {
        product {
          ...ProductFrag
        }
      }
    }
  }
}
fragment ProductFrag on Product {
  id
  sku
  title
  desc
  image
  stocked
  basePrice
  price
}


When using the basket use a random checkoutID (eg: "123" or "peterBasket") to get your own basket.

