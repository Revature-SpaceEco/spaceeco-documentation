# Space Eco Start Up

Table of Contents |
----------------- |
[Backend Start Up](#Backend-Start-Up)
[Frontend Start Up](#Frontend-Start-Up)


## Backend Start Up

1. In terminal, git clone repository

2. Ensure environment variables are set, which include db_username and db_password

3. Ensure there is an existing database in postgresQL, either locally or remotely, named 'spaceeco'

2. Run build.gradle to create jar file and ensure no compile errors.

4. Run SpaceecoBackendApplication.java to start backend of application.


## Frontend Start Up
1. In terminal, git clone repository

2. Navigate to the local folder and run `npm install` in the terminal.
    - You may need to run `npm update` prior to `npm install` in the event that certain packages have vulnerabilities or have become deprecated.

3. The following steps can be completed in any order, dependant on the user's end goal:
    - Run `npm build` to create local dist folder for application
    - Run `npm test` or `npm run coverage` to run the tests create for the application
    - Run `npm run watch` to start the development environment for the application
    - Run `npm run server` to start the application with the associated db.json file seeding the database
    - Run `npm start` to start the production environment for the application