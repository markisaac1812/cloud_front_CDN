<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# APIs with Lambda + API Gateway

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-api)

**Author:** Mark Isaac  
**Email:** markisaac695@gmail.com

---

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-compute-api_c9d0e1f2)

---

## Introducing Today's Project!

In this project, I will demonstrate the application layer or what is know by Backend in three tier architecture .I'm doing this project to learn how like an actual webiste from elements and styling to querying from a database actual deployed in the real world

### Tools and concepts

Services I used were API gateway as well as lambda function. Key concepts I learnt include Lambda functions about how can i run a code when action is triggered like in my case when someone enter an ID and click on the button , a GET request will be sent to lambda to process 

### Project reflection

This project took me approximately 1 hour. The most challenging part was understand lamda proxy integration in API gateway.

I chose to do this project today because i wanted how an actual website is made starting from simple html elements to querying data from a database..

---

## Lambda functions

AWS Lambda is SERVERLESS computing service . which means in simple words running a code in response to some event on a server you dont buy or manadge. I'm using Lambda in this project to fetch some data about user from a database via API gateway

The code I added to my function will set up a Lambda function that retrieves data from a DynamoDB table.

It looks for specific user data based on a 'userId' and returns that data. If there's an error e.g. the userId doesn't exist in the database, it returns an error message

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-compute-api_a1b2c3d5)

---

## API Gateway

APIs are Application Programming Interface  that enable diffrent pieces of software to talk to each other. There are different types of APIs, like GraphQL My API is on the other hand is REST .

Amazon API Gateway is like a Front door for all my backend apis in my case it is my lambda function. I'm using API Gateway in this project so it can recieves requests and route it to the appropiate lambdas function to execute the code and handle back the response to display in UI

When a user makes a request the api gateway takes that request and pass it to the appropiate lambda function . then the lamdba function process that request execute the code and handle back the resposne to the api gateway

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-compute-api_m3n4o5p6)

---

## API Resources and Methods

API resources are individual endpoints within your API that handle different parts of its functionality.

Each resource consists of methods, which are GET for retrieving data (insecure btw) , POST for adding new data , PUT or PATCH for updating existing data and finally DELETE for deleting existing data.

I created a GET method . so now when user enter an ID , it sent this request to an API gateway using get request because it wants to RETRIEVE data then it maps this request to my lambda function to process the get request

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-compute-api_c9d0e1f2)

---

## API Deployment

When you deploy an API, you deploy it to a specific stage. A stage is a stage is a snapshot of your API at a specific point in time. I deployed it to production stage but normally in teams they usually have dev ,test,prod stages of APIs

To visit my API, I go to invoke URL .  The API displayed an error because i have not set up my dynamo DB yet

![Image](http://learn.nextwork.org/vibrant_pink_mysterious_chico/uploads/aws-compute-api_3ethryj2)

---

## API Documentation

---

---
