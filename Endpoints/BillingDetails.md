# SpaceEco: Billing Details 


Table of Contents |
------------------|
[Request Types](#Request-Types)
[GET](#GET)
[PATCH](#PATCH)
[POST](#POST)
[DELETE](#DELETE)
|


## Request Types

### GET
`/users/{userId}/billing/{billing_id}`

    Input Parameter: userId (number), billingId (number)
    Return: billingDetails

    Uses the path parameter to return the billing details of the specified user.


### POST
`/users/{userId}/billing`

    Input Parameter: userId (number)
    Return: billingDetails

    Uses the path parameter to create new billing details for a user.


### PATCH
`/users/{userId}/billing/{billing_id}`

    Input Parameter: userId, billingId (number), billingDetailsDto
    Return: billingDetails

    Uses the path parameter to update an existing billing details entry for the specified user.
    
    
### DELETE
`/users/{userId}/billing/{billing_id}`

    Input Parameter: userId (number), billingId (number)
    Return: Boolean

    Takes in the request and deletes the billingId specified for the userId specified. Returns a boolean value to the user after deletion.
