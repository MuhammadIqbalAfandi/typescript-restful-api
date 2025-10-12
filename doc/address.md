# Address API Spec

## Create Address

Endpoint : POST /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Street name",
  "city": "City",
  "province": "Province / State",
  "country": "Country",
  "postal_code": "Postal code"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street name",
    "city": "City",
    "province": "Province / State",
    "country": "Country",
    "postal_code": "Postal code"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "city is required"
}
```

## Get Address

Endpoint : GET /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street name",
    "city": "City",
    "province": "Province / State",
    "country": "Country",
    "postal_code": "Postal code"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "City is not found"
}
```

## Update Address

Endpoint : PUT /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Street name",
  "city": "City",
  "province": "Province / State",
  "country": "Country",
  "postal_code": "Postal code"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street name",
    "city": "City",
    "province": "Province / State",
    "country": "Country",
    "postal_code": "Postal code"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "city is required"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "ok"
}
```

Response Body (Failed) :

```json
{
  "errors": "Address is not found"
}
```

## List Address

Endpoint : GET /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "street": "Street name",
      "city": "City",
      "province": "Province / State",
      "country": "Country",
      "postal_code": "Postal code"
    },
    {
      "id": 2,
      "street": "Street name",
      "city": "City",
      "province": "Province / State",
      "country": "Country",
      "postal_code": "Postal code"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors": "City is not found"
}
```
