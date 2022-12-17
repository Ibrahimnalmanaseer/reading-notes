# Authentication & Production Server

## JSON Web Tokens

### What is JSON Web Token?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

### When should you use JSON Web Tokens?

- **Authorization** : Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.
- **Information Exchange**: securely transmitting information between parties,using public/private key pairs—you can be sure the senders are who they say they are.

### What is the JSON Web Token structure?

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

- Header
- Payload
- Signature

**As below format:**

`xxxxx.yyyyy.zzzzz`



### How do JSON Web Tokens work?

Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the `Authorization` header using the `Bearer` schema.
The content of the header should look like the following:

`Authorization: Bearer <token>`


The server's protected routes will check for a valid JWT in the `Authorization` header, and if it's present, the user will be allowed to access protected resources. 

The following diagram shows how a JWT is obtained and used to access APIs or resources:

![client-credentials-grant](https://user-images.githubusercontent.com/62019258/208265046-559b802f-0068-44f6-a083-25455cea86ff.png)


  
