# SpaceEco: Authentication

Request Types |
------------------|
[LOGIN](#End-point:-Authenticate-User)
|


## End-point: Authenticate User
Used to login users by sending credentials along with one-time password set-up using TOTP algorithm. On success returns a JSON object containing web token.

### Method: POST
>```
>localhost:8080/authenticate
>```
### Body (**raw**)

```json
{
    "username": "shrimp",
    "password": "password",
    "mfaCode": "88881811"
}
```

### Response: 200
```json
{
    "jwt": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJidXllcjEiLCJleHAiOjE2NTM1MjIyMjYsInVzZXJJZCI6MSwiaWF0IjoxNjUwOTMwMjI2fQ.A38Mg-96kQLnFdGAeSKCaTfQN5RQHpBGApMytpbXNgU"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
