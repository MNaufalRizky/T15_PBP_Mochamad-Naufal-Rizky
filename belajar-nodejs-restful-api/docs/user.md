# User API Spec

## Register User API

Endpoint :  POST /api/users 

Request Body :

```json
{
  "username" : "sky",
  "password" : "naufalsky",
  "name" : "Mochamad Naufal Rizky"
}
```

Response Body Success :

```json
{
  "data" : {
    "username" : "sky",
    "name" : "Mochamad Naufal Rizky"
  }
}
```

Response Body Error : 

```json
{
  "errors" : "Username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username" : "sky",
  "password" : "naufalsky"
}
```

Response Body Success : 

```json
{
  "data" : {
    "token" : "unique-token"
  }
}
```

Response Body Error :

```json
{
  "errors" : "Username or password wrong"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :
- Authorization : token 

Request Body :

```json
{
  "name" : "Mas Langit", // optional
  "password" : "naufalrizky" // optional
}
```

Response Body Success : 

```json
{
  "data" : {
    "username" : "sky",
    "name" : "Mas Langit"
  }
}
```

Response Body Error : 

```json
{
  "errors" : "Name length max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :
- Authorization : token

Response Body Success:

```json
{
  "data" : {
    "username" : "sky",
    "name" : "Mochamad Naufal Rizkylk"
  }
}
```

Response Body Error : 

```json
{
  "errors" : "Unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :
- Authorization : token

Response Body Success : 

```json
{
  "data" : "OK"
}
```

Response Body Error : 

```json
{
  "errors" : "Unauthorized"
}
```
