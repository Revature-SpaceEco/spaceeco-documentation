# SpaceEco Backend Security

## Overview
The backend API is secured at the application level using [Spring Security](https://spring.io/projects/spring-security).  Authorization per endpoint is applied via Roles which are defined in the `user_roles` table.  Authentication is stateless and JWTs are used to authenticate access to specific urls.  The authentication rules for each endpoint are specified in the `configure(HttpSecurity http)` method of the `SecurityConfiguration` class.  Upon login, a user enters their username/password, a call is made to the `/authenticate` endpoint and a JSON object is returned with a single property `jwt` containing the user's JWT.  This token is stored in the local storage of the browser.  It expires 30 days from the time of login, unless the user specifically logs out (clears the token from their local storage. 

No extra code is required when writing the controller mappings.  Just construct the endpoints as you normally would.  Do not need to include the `Authorization` header value.

When consuming the endpoints in the frontend, all that is required is to include the JWT in the request header as `Authorization: Bearer {jwt}`.  Spring security will automatically manage authorization by decoding claims in the token.  Front-end developers (except for login/registration) should assume that a user's JWT will be in the local storage of the browser.  

# Endpoint Rules
- `/authenticate` : No auth required
- `/register` : No auth required
- `/products` : No auth required
- `/users/{id}/**` : Requires user ID to be same as logged in user
- `/admin/**` : Requires admin role
