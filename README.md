# restful-booker.herokuapp.com

This is for practice.Perform CRUD operation.Use POSTMAN for testing this API.




## Roadmap

- Go to any browser 

- Find POSTMAN, SignUp account and download required desktop version.


## Overview
Used two request 

    1.Collection
    2.Environment
In Collection, Here perform

    1. Create Request -> Use POST method
    2. Get Request    -> Use GET  method
    3. PUT Request    -> Use PUT  method
    4. AUTH Request   -> Use POSt method 
    5. DELETE Request -> Use DEL  method

In Environment, Here Use

    1. BaseUrl -> https://restful-booker.herokuapp.com
    2. id      -> Dynamically control from Collection Create Request
    3. token   -> Dynamically control from Collection Auth Request

## Steps for CRUD operation

    1. Create Request : Method POST
       -In Environment use variable and value for BaseUrl.
       -Use url variable on PATH section in collection. like: {{variable}}/given_path
       -Use data on Body section in JSON format and send request.
       -Dynamically take id from response and set it to Environment

    2. Get Request : Method GET
       -Use this ID on PATH section in collection. like: {{variable}}/given_path/{{id}}
       -Send request.

    3. Auth Request : Method POST
       -Dynamically take token from response and set it to Environment
       -Use data on Body section in JSON format and send request.

    4. Put Request : Method PUT
       -In Environment use cookie and value for token.
       -Use url variable on PATH section in collection. like: {{variable}}/given_path/{{id}}
       -Use update data on Body section in JSON format and send request.

    5. Delete Request : Method DEL 
       -In Environment use cookie and value for token.
       -Use url variable on PATH section in collection. like: {{variable}}/given_path/{{id}}
       -Send request.

  

## Steps for Report 
From Collection & Environment export the result and save it.Install Node.js for report generation.Install newman library using CMD.

    npm install -g newman
Now newman can run our Collection & Environment export file.Open CMD to write the new command

    newman run restfulbooker_2_041022_auto.postman_collection.json
    newman run restfulbooker_2_041022_auto.postman_collection -e restfulbooker_2_041022_auto.postman_environment_collection.json

Report format will be in html or htmlextra format.Now install this format using CMD.

    npm install -g newman-reporter-html
    npm install -g newman-reporter-htmlextra

Now it's time to generate graphical Overview of this project. Use this command on CMD
    
    newman run restfulbooker_2_041022_auto.postman_collection -e restfulbooker_2_041022_auto.postman_environment_collection.json -r html
    newman run restfulbooker_2_041022_auto.postman_collection -e restfulbooker_2_041022_auto.postman_environment_collection.json -r htmlextra
## Documentation
For any kind of information use this [Site.](https://www.javatpoint.com/postman)




