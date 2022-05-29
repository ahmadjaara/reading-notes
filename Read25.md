# Introduction to JSON Web Tokens

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. 

## When should you use JSON Web Tokens?

### Authentication

Authentication is done when a client successfully proves its identity via a login endpoint. If it's successful, the server will create JSON Web Token and send it in response to the client.

The client will use this JWT on every request for a protected resource.

### Authorization

A server built on JWT for authorization will create a JWT when a client logs in. This JWT is signed, so any other party can’t alter it.

Each time the client has access to protected resources, the server will verify that the JWT’s signature matches its payload and header to determine that the JWT is valid.

Then if the JWT is successfully verified, it can grant or deny access to the resource.

### Data Exchanges

JWT is also a great way to secure information transmission between parties — two servers, for example — and because you can verify the validity of the token (signature, structure, or the standards claimed in the JWT). 

## When Not to Use JWT Authentication?


### Sensitive Information

JWT is usually signed to protect against data manipulation or alteration. With this, the data can be easily read or decoded.

So, you can’t include sensitive information such as the user’s record or any identifier because the data is not encrypted.


## What is the JSON Web Token structure?

In its compact form, JSON Web Tokens consist of three parts separated by dots ( . ) , which are:

- Header
- Payload
- Signature

### Header

The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

### Payload

Its contain the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims

### Signature

The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.

To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

## How do JSON Web Tokens work?

In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.

Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.
