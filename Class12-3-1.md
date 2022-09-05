# Status Codes Based On REST Methods

## In your own words, describe what each group of status code represents:

100's =These are informational status codes; they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.

200's = These are the success codes. They tell the client that its request was accepted. 

300's = These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore

400's = These are the client error codes. They are all about invalid requests a client sent to a server.

500's = These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies.

## What is a status code 202?
Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. 

## What is a status code 308?
This tells the client to use another URL to access the resource and not use the current URL anymore. 

## What code would you use if an update didn't return data to a client?
204 

## What code would you use if a resource used to exist but no longer does? 
409

## What is the 'Forbidden' status code?
HTTP 403

## Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

## Why do we need to pull our MongoDB database string out of our server and put it into our .env?
To be hidden so that other people don't use it and when deploying the service can change the path easy.

## What is middleware?

 is software that provides common services and capabilities to applications outside of what's offered by the operating system.
People also ask

## What does app.use(express.json()) do?

it parses incoming JSON requests and puts the parsed data in req.

## What does the /:id mean in a route?

is a unique identifier assigned to every order that is protected by Route Package Protection.

## What is the difference between PUT and PATCH?
PUT HTTP Request: PUT is a method of modifying resources where the client sends data that updates the entire resource.

PATCH HTTP Request: Unlike PUT Request, PATCH does partial update e.g. Fields that need to be updated by the client, only that field is updated without modifying the other field.

## How do you make a default value in a schema?

Your schemas can define default values for certain paths. If you create a new document without that path set, the default will kick in.

## What does a 500 error status code mean?

is a generic error response. It means that the server encountered an unexpected condition that prevented it from fulfilling the request.

## What is the difference between a status 200 and a status 201?
200 OK - It’s the basic status code to tell the client everything went good.
201 Created - The most fitting for Create operations.

## Things I want to know more about

Mongoose
MongoDB
