# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Request Body :

```json
{
  "street" : "Jl.Babakan Limusnunggal",
  "city" : "Kota Sukabumi",
  "province" : "Jawa Barat",
  "country" : "Indonesia",
  "postal_code" : "43165"
}
```

Response Body Success :

```json
{
  "data" : {
    "id" : 1,
    "street" : "Jl.Babakan Limusnunggal",
    "city" : "Kota Sukabumi",
    "province" : "Jawa Barat",
    "country" : "Indonesia",
    "postal_code" : "43165"
  }
}
```

Response Body Error :

```json
{
  "errors" : "Country is required" 
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Request Body :

```json
{
  "street" : "Jl.Babakan Limusnunggal",
  "city" : "Kota Sukabumi",
  "province" : "Jawa Barat",
  "country" : "Indonesia",
  "postal_code" : "43165"
}
```

Response Body Success :

```json
{
  "data" : {
    "id" : 1,
    "street" : "Jl.Babakan Limusnunggal",
    "city" : "Kota Sukabumi",
    "province" : "Jawa Barat",
    "country" : "Indonesia",
    "postal_code" : "43165"
  }
}
```

Response Body Error :

```json
{
  "errors" : "Country is required"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success :

```json
{
  "data" : {
    "id" : 1,
    "street" : "Jl.Babakan Limusnunggal",
    "city" : "Kota Sukabumi",
    "province" : "Jawa Barat",
    "country" : "Indonesia",
    "postal_code" : "43165"
  }
}
```

Response Body Error :

```json
{
  "errors" : "contact is not found"
}
```

## List Addresses API

Endpoint : GET /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Response Body Success :

```json 
{
  "data" : [
    {
      "id" : 1,
      "street" : "Jl.Babakan Limusnunggal",
      "city" : "Kota Sukabumi",
      "province" : "Jawa Barat",
      "country" : "Indonesia",
      "postal_code" : "43165"
    },
    {
      "id" : 1,
      "street" : "Jl.Babakan Limusnunggal",
      "city" : "Kota Sukabumi",
      "province" : "Jawa Barat",
      "country" : "Indonesia",
      "postal_code" : "43165"
    }
  ]
}
```

Response Body Error :

```json
{
  "errors" : "contact is not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

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
  "errors" : "address is not found"
}
```
