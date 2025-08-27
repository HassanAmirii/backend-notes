# Introduction to jwt (Json web token)

<p>Here are some questions i asked myself when it was time to implement jwt into my server authentication--which will also serve as the explanation outline. </p>

<ul>
 <li> what is jwt </li>
 <li> why do need jwt when we can simply validate a user through a database</li>
 <li> how does jwt works</li>
 <li> how to implement jwt into a server authentication </li>
 
 </ul>

### 1. What is jwt?

"JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA."

- source jwt.io

In my own words, **jwt is a digital identification holder.**

### 2. Why do need jwt when we can simply validate a user through a database?

Well, turns out hitting the database everytime to validate a user is not scalable when the user-base start growing, and it introduces performance issues such as latency, botttle neck etc.

### 3. How does jwt works?

I will be rephrasing this heading title as how does jwt serves as a digital identity holder?

when a user registers an account, their information is stored in the db, Now when it is time to log in the jwt is attached to it because it needs to collect certain details to form the identification holder which it will auto tender to the server upon subsequent requests, so the user does not have to keep inputting their credentials to access secured routes.

There are three essentials that jwt contains.

- header
- payload
- signed token
  <br>

1. The **header** contains meta-data about the token such as the token type, hashing algorithm, etc.

 <br>

2. The **payload** contains information such as the user_id, username.

 <br>

3. The **signed token** is formed by mixing and hashing the header, payload, and the server's secret key.

 <br>

Upon subsequent requests, the server just have to re-hash (server's secret key, payload, header). and compare it with the tendered one by jwt if it matches and the jwt's token has'nt expired then the user get authorized.
else the server returns error 401: unauthorized, and probably reroute the user to relogin to re-create a jwt token.

### 4. how to implement jwt into server auth?
