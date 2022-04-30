# SpaceEco: Orders 


Request Types |
------------------|
[GET ALL](#End-point:-All-Orders-As-Admin)
[GET ONE FOR USER](#End-point:-All-Orders-As-User)
[GET ONE FOR USER](#End-point:-Singular-Order-As-User)
[POST](#End-point:-Add-Order-For-User)
[DELETE](#End-point:-Delete-Order-For-User)
|


## End-point: All Orders As Admin
Retrieves an array of all orders.

### Method: GET
>```
>http://localhost:8080/admin/orders
>```
### Response: 200
```json
[
    {
        "id": 1,
        "orderDate": "2022-04-20T12:26:24.166+00:00",
        "orderStatus": "Pending",
        "shippingAddressId": {
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
        "payment": {
            "id": 1,
            "billingDetailsDto": null,
            "status": "Pending"
        }
    },
    {
        "id": 2,
        "orderDate": "2022-04-20T12:30:24.166+00:00",
        "orderStatus": "Approved",
        "shippingAddressId": {
            "id": 2,
            "addressLineOne": "14 East Jefferson Court",
            "addressLineTwo": "",
            "city": "Fairhope",
            "state": "AL",
            "country": "United States",
            "zip": "36532",
            "solarSystem": "solar system",
            "planet": "earth"
        },
        "payment": {
            "id": 2,
            "billingDetailsDto": null,
            "status": "Pending"
        }
    }
]
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Orders As User
Retrieves an array of orders for a specific user
### Method: GET
>```
>http://localhost:8080/users/1/orders
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
[
    {
        "id": 1,
        "orderDate": "2022-04-20T12:26:24.166+00:00",
        "orderStatus": "Pending",
        "shippingAddressId": {
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
        "payment": {
            "id": 1,
            "billingDetailsDto": null,
            "status": "Pending"
        }
    }
]
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Singular Order As User
Retrieves a specific order for a user.

### Method: GET
>```
>http://localhost:8080/users/1/orders/1
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
{
    "id": 1,
    "orderDate": "2022-04-20T12:26:24.166+00:00",
    "orderStatus": "Pending",
    "shippingAddressId": {
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
    "payment": {
        "id": 1,
        "billingDetailsDto": null,
        "status": "Pending"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Add Order For User
Adds an order for a user.

### Method: POST
>```
>http://localhost:8080/users/1/orders
>```
### Body (**raw**)

```json
{
    "id": 0,
    "buyer": {
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
    },
    "orderDate": "2022-04-20T12:26:24.166+00:00",
    "orderStatus": "Pending",
    "shippingAddressId": {
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
    "payment": {
        "id": 1,
        "billingDetailsDto": null,
        "status": "Pending"
    },
    "items": [
        {
            "id": 1,
            "name": "reach",
            "description": "A wonderful planet",
            "cost": 150,
            "category": null,
            "image": "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg",
            "sellerInfo": null
        },
        {
            "id": 2,
            "name": "eridanus II",
            "description": "A wonderful planet",
            "cost": 100,
            "category": null,
            "image": "www.image.com/eridanusII.jpg",
            "sellerInfo": null
        }
    ]
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
    "buyer": {
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
            "addressLineOne": null,
            "addressLineTwo": null,
            "city": null,
            "state": null,
            "country": null,
            "zip": null,
            "solarSystem": null,
            "planet": null
        },
        "primaryBilling": {
            "id": 1,
            "billingCardType": null,
            "billingCardNumber": 0,
            "billingSecurityNumber": 0,
            "billingName": null,
            "billingAddress": {
                "id": 1,
                "addressLineOne": null,
                "addressLineTwo": null,
                "city": null,
                "state": null,
                "country": null,
                "zip": null,
                "solarSystem": null,
                "planet": null
            }
        },
        "imageUrl": "www.profileimage.com/1.jpg",
        "active": true
    },
    "items": [
        {
            "id": 1,
            "name": "reach",
            "description": "A wonderful planet",
            "cost": 150,
            "category": null,
            "image": "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg",
            "sellerInfo": null
        },
        {
            "id": 2,
            "name": "eridanus II",
            "description": "A wonderful planet",
            "cost": 100,
            "category": null,
            "image": "www.image.com/eridanusII.jpg",
            "sellerInfo": null
        }
    ],
    "orderDate": "2022-04-29T17:01:26.933+00:00",
    "orderStatus": "Pending",
    "shippingAddressId": {
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
    "payment": {
        "id": 1,
        "billingDetailsDto": null,
        "status": "Pending"
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Delete Order For User
Removes an order for a user.

### Method: DELETE
>```
>http://localhost:8080/users/1/orders
>```
### Body (**raw**)

```json
{
    "id": 3,
    "buyer": {
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
    },
    "orderDate": "2022-04-20T12:26:24.166+00:00",
    "orderStatus": "Pending",
    "shippingAddressId": {
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
    "payment": {
        "id": 1,
        "billingDetailsDto": null,
        "status": "Pending"
    },
    "items": [
        {
            "id": 1,
            "name": "reach",
            "description": "A wonderful planet",
            "cost": 150,
            "category": null,
            "image": "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg",
            "sellerInfo": null
        },
        {
            "id": 2,
            "name": "eridanus II",
            "description": "A wonderful planet",
            "cost": 100,
            "category": null,
            "image": "www.image.com/eridanusII.jpg",
            "sellerInfo": null
        }
    ]
}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|{{token}}|string|


### Response: 200
```json
true
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃