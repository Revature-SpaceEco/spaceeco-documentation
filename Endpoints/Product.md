# SpaceEco: Products 

Request Types |
------------------|
[GET ALL](#End-point-Get-All-Products)
[GET ONE](#End-point-Get-Singular-Product)


## End-point: Get All Products
Endpoint displays all of the products available in spaceEco.

### Method: GET
>```
>http://localhost:8080/products
>```
### Response: 200
```json
[
    {
        "id": 1,
        "name": "reach",
        "description": "A wonderful planet",
        "cost": 150,
        "category": {
            "id": 1,
            "name": "planets"
        },
        "image": "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg",
        "sellerInfo": {
            "id": 3,
            "username": "seller1",
            "email": "seller@email.com",
            "firstName": "Jane",
            "active": true
        }
    },
    {
        "id": 2,
        "name": "eridanus II",
        "description": "A wonderful planet",
        "cost": 100,
        "category": {
            "id": 1,
            "name": "planets"
        },
        "image": "www.image.com/eridanusII.jpg",
        "sellerInfo": {
            "id": 3,
            "username": "seller1",
            "email": "seller@email.com",
            "firstName": "Jane",
            "active": true
        }
    },
    {
        "id": 3,
        "name": "Pilar of autumn",
        "description": "A powerful rocket",
        "cost": 50,
        "category": {
            "id": 2,
            "name": "vehicles"
        },
        "image": "www.image.com/pillar.jpg",
        "sellerInfo": {
            "id": 3,
            "username": "seller1",
            "email": "seller@email.com",
            "firstName": "Jane",
            "active": true
        }
    }
]
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get Singular Product
Endpoint displays a single product once selected by its ID from the list of all the products.

### Method: GET
>```
>http://localhost:8080/products/1
>```
### Response: 200
```json
{
    "id": 1,
    "name": "reach",
    "description": "A wonderful planet",
    "cost": 150,
    "category": {
        "id": 1,
        "name": "planets"
    },
    "image": "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__480.jpg",
    "sellerInfo": {
        "id": 3,
        "username": "seller1",
        "email": "seller@email.com",
        "firstName": "Jane",
        "active": true
    }
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
_________________________________________________
Powered By: [postman-to-markdown](https://github.com/bautistaj/postman-to-markdown/)
