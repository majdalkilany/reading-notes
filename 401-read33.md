# Introduction to JSON Web Tokens

### What is JSON Web Token?



JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact 
and self-contained way for securely transmitting information between 
parties as a JSON object. This information can be verified and trusted 
because it is digitally signed. JWTs can be signed using a secret (with 
the HMAC algorithm) or a public/private key pair using RSA or ECDSA.



#### When should you use JSON Web Tokens?

* Authorization: This is the most common scenario for using JWT. Once the 
user is logged in, each subsequent request will include the JWT, allowing 
the user to access routes, services, and resources that are permitted with 
that token. Single Sign On is a feature that widely uses JWT nowadays, 
because of its small overhead and its ability to be easily used across 
different domains



* Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.


#### What is the JSON Web Token structure?
 
 In its compact form, JSON Web Tokens consist of three parts separated by 
 dots (.), which are:


* Header
* Payload
* Signature



###### Header

The header typically consists of two parts: the type of the token, which 

is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

* **Public claims**: These can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.

* **Private claims**: These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.

