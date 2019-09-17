Exercices
# open euri-test-api
open https://euri-test-api-gyitloixhh.now.sh/
Use PostMan & open the API to complete the following exercises.

---//

Exercices
- Get a list of all users ordered by
  lastName desc
https://euri-test-api-gyitloixhh.now.sh/api/users?sort=-lastName


- Get a paginated list of users where the
  pageSize is 5 and get the second page. As a
  bonus find out how the api communicates the
  total amount of users

https://euri-test-api-gyitloixhh.now.sh/api/users?page=2&pageSize=5


- Get the user with the id 2

https://euri-test-api-gyitloixhh.now.sh/api/users/2
- Create a new user with the data of yourself
POST /api/users HTTP/1.1
Host: euri-test-api-gyitloixhh.now.sh
Content-Type: application/json
User-Agent: PostmanRuntime/7.16.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8f054572-2e38-40d6-8bbe-9ade02926475,9069afdb-f07e-4cb1-a067-291650bc2e2c
Host: euri-test-api-gyitloixhh.now.sh
Accept-Encoding: gzip, deflate
Content-Length: 127
Connection: keep-alive
cache-control: no-cache

{
  "firstName": "Karima",
  "lastName": "El Hachimi",
  "age": 26,
  "email": "karima.elhachimi@euri.com",
  "role": "admin"
}
- Remove yourself again
DELETE https://euri-test-api-gyitloixhh.now.sh/api/users/1568719378220
- Get the basket with items description
GET https://euri-test-api-gyitloixhh.now.sh/api/basket/karimasbasket
-> productID gebruiken voor nieuwe GET request voor product info
GET https://euri-test-api-gyitloixhh.now.sh/api/products/1
