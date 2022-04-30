# SpaceEco: Address

Request Types |
------------------|
[GET ONE](#End-point-Get-Singular-Address)
[POST](#End-point-Add-Singular-Address)


## End-point: Get Singluar Address
This retrieves the address of the user in the HTTP response

### Method: GET
>```
>http://localhost:8080/users/1/address
>```
### 🔑 Authentication bearer

| Param | value | Type |
|-----|-----|-----|
| token | {{ token }} | string |


### Response: 200
```json
{
    "id": 6,
    "addressLineOne": "Huzzah",
    "addressLineTwo": "Windmill Giant",
    "city": "The land",
    "state": "FL",
    "country": "United States",
    "zip": "49417",
    "solarSystem": "solar system",
    "planet": "earth"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Add Singular Address
This sets the address of the user in the HTTP response

### Method: POST
>```
>http://localhost:8080/users/1/address
>```
### Body (**raw**)

```json
{
    "addressLineOne": "Huzzah",
    "addressLineTwo": "Windmill Giant",
    "city": "The land",
    "state": "FL",
    "country": "United States",
    "zip": "49417",
    "solarSystem": "solar system",
    "planet": "earth"
}
```

### 🔑 Authentication bearer

| Param | value | Type |
|-----|-----|-----|
| token | {{ token }} | string |


### Response: 200
```json
{
    "id": 6,
    "addressLineOne": "Huzzah",
    "addressLineTwo": "Windmill Giant",
    "city": "The land",
    "state": "FL",
    "country": "United States",
    "zip": "49417",
    "solarSystem": "solar system",
    "planet": "earth"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
