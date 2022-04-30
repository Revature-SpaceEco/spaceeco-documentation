# SpaceEco: User

Request Types |
------------------|
[GET ONE](#End-point-Get-Singular-User)
[POST](#End-point-Add-Singular-User)
|


## End-point: Get Singular User
This endpoint is for getting a user by id using a GET request.

### Method: GET
>```
>http://35.232.101.198:8080/users/1
>```
### 🔑 Authentication bearer

| Param | value | Type |
|-----|-----|-----|
| token | {{ token }} | string |


### Response: 200
```json
{
    "id": 1,
    "username": "buyer1",
    "email": "buyer@email.com",
    "firstName": "John",
    "lastName": "Doe",
    "userRole": {
        "id": 1,
        "role": "ROLE_BUYER"
    },
    "primaryAddress": {
        "id": 1,
        "addressLineOne": "9194 North College Ave",
        "addressLineTwo": "512 South Pennsylvania St",
        "city": "Grand Haven",
        "state": "MI",
        "country": "United States",
        "zip": "49417",
        "solarSystem": "solar system",
        "planet": "earth"
    },
    "primaryBilling": {
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
    "imageUrl": "www.profileimage.com/1.jpg",
    "active": true
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Add Singular User
This endpoint is for creating a user using a POST request.

### Method: POST
>```
>http://35.232.101.198:8080/users
>```
### Body (**raw**)

```json
{
    "id":"0",
    "username":"deva77", 
    "password":"password123",
    "email":"deva777817@loki.com", 
    "firstName":"Deva", 
    "lastName":"Sakthi", 
    "userRole" : {
        "id":1,
        "role":"ROLE_BUYER"
    },
    "active":true

}
```

### 🔑 Authentication bearer

| Param | value | Type |
|-----|-----|-----|
| token | {{ token }} | string |


### Response: 200
```json
User created successfully.
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

