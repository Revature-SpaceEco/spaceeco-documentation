# SpaceEco: Billing Details 


Request Types |
------------------|
[GET ONE FOR USER](#End-point-Singular-Billing-Detail-As-User)
[POST](#End-point-Add-Billing-Detail-For-User)
[UPDATE](#End-point-Update-Billing-Detail)
[DELETE](#End-point-Delete-Billing-Detail)
|


## End-point: Singular Billing Detail As User
Retrieves a billing details

### Method: GET
>```
>http://localhost:8080/users/1/billing/1
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 1,
    "billingCardType": "Visa",
    "billingCardNumber": 1234456778971547,
    "billingSecurityNumber": 142,
    "billingName": "John",
    "billingAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Add Billing Detail For User
Adds a new billing details

### Method: POST
>```
>http://localhost:8080/users/1/billing
>```
### Body (**raw**)

```json
{
    "billingCardType": "American Express",
    "billingCardNumber": 555555555555,
    "billingSecurityNumber": 555,
    "billingName": "Homer Simpson",
    "billingAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    }
}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 5,
    "billingCardType": "American Express",
    "billingCardNumber": 555555555555,
    "billingSecurityNumber": 555,
    "billingName": "Homer Simpson",
    "billingAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Update Billing Detail
Updates an existing billing details

### Method: PATCH
>```
>http://localhost:8080/users/1/billing/1
>```
### Body (**raw**)

```json
{
    "billingCardType": "Master Card",
    "billingCardNumber": 9999999999999999,
    "billingSecurityNumber": 142,
    "billingName": "Homer Simpson",
    "billingAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    }
}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 1,
    "billingCardType": "Master Card",
    "billingCardNumber": 9999999999999999,
    "billingSecurityNumber": 142,
    "billingName": "Homer Simpson",
    "billingAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Delete Billing Detail
Deletes a billing details.

### Method: DELETE
>```
>http://localhost:8080/users/1/billing/5
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
true
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
