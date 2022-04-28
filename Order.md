# SpaceEco: Orders 


Table of Contents |
------------------|
Requests
[GET](#GET)
[POST](#POST)

## Possible Response Codes
400
    
    Possible causes: Order is missing data

404
    
    Possible causes: User Not Found, Order Not Found,  

## Request Types

### GET
/user/{userId}/orders

    Input Parameter: userId
    Return: List<OrderDto> orders

    Using the path variable userId as an input parameter this endpoint retireves an ArrayList of orders.

    Using a model mapper each order is the list is converted into an OrderDto.


/users/{userId}/orders/{orderId}

    Input Parameter: orderId
    Return: OrderDto

    Uses the path variable orderId as an input parameter and retireves the Order from the repository.  

    Using a model mapper converts the Order into a OrderDto. 

### POST
/users/{userId}/orders

    Input Parameter: orderDto
    Return: OrderDto

    Uses the request body as an input parameter to create a new order.

    Once saved to the repository a model mapper will convert an Order object to an OrderDto.


### PATCH
/users/{userId}/orders/{orderId}

    Input Parameter: orderDto
    Return: OrderDto

    Uses the request body as an input parameter submit changes to an order.

    Once saved to the repository a model mapper will convert an Order object to an OrderDto.

### DELETE
/users/{userId}/orders/{orderId}

    Input Parameter: orderDto
    Return boolean

     Uses the request body as an input parameter submit changes to an order.

    Once removed from the repository a response will be sent back to the client with a boolean value.