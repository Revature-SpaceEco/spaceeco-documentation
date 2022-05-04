# SpaceEco: Payment

Request Types |
------------------|
[GET ONE FOR USER](#End-point-Get-Singular-Payment-As-User)
[POST](#End-point-Add--Singular-Payment-As-User)
[PATCH](#End-point-Update-Payment)
[DELETE](#End-point-Delete-Payment)


## End-point: Get Singular Payment As User
Retrieves a payment

### Method: GET
>```
>http://localhost:8080/users/1/payments/1
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 1,
    "billingDetails": {
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
    },
    "status": "Pending"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Add Singular Payment As User
Adds a payment for an order

### Method: POST
>```
>http://localhost:8080/users/1/payments
>```
### Body (**raw**)

```json
{
    "id": 0,
    "billingDetails": {
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
    },
    "status": "Pending"
}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 3,
    "billingDetails": {
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
    },
    "status": "Pending"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Update Payment
Updates the state of a payment.

### Method: PATCH
>```
>http://localhost:8080/users/1/payments
>```
### Body (**raw**)

```json
{
    "id": 3,
    "billingDetails": {
        "id": 1,
        "billingCardType": "Master Card",
        "billingCardNumber": 9999999999999999,
        "billingSecurityNumber": 999,
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
    },
    "status": "Pending"
}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 3,
    "billingDetails": {
        "id": 1,
        "billingCardType": "Master Card",
        "billingCardNumber": 9999999999999999,
        "billingSecurityNumber": 999,
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
    },
    "status": "Pending"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Delete Payment
Removes a payment

### Method: DELETE
>```
>http://localhost:8080/users/1/payments/3
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

