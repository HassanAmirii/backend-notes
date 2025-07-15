# SSL/TLS handshake 🤝

This is basically the upgrade patch from HTTP to HTTPs.

#### short history:

SSL (secure socket layer) was the old security layer developed by Netscape Navigator web browser in the 90s, during the surge of e-commerce, a need for a secure layer -- behind the scene security during the communication between a client(browser) and a server(eg amazon.com) was needed to encrypts / secure data during any communication.

later on, some vulnerabilities was discovered in the SSL, which was now upgraded to TLS(transport layer security) by the Internet Engineering Task Force (IETF), for better encryption algorithm + efficient communication between the client and the server.

so most browsers have upgraded to the new system tls;

### The Security Flow Behind HTTPS is Powered by TLS

##### some basic terms to know before we dive in:

**client:** aka browser eg google chrome,

**server:** -- that would be the website been navigated to eg amazon.com, to get content to display on the browser.

##### Now the TLS Analogy to understand the behind the scene:

Say you open up your browser(client) to navigate to a server eg amazon.com;

**step 1: (ssl / tls handshake;):**
browser hello: your browser initiate a communication to the server saying it wants to establish a secure connection. This message includes the version of SSL/TLS it supports and a list of encryption methods it can use.

server hello: the server responds by picking the version of ssl/tls it want to use for encryption and also sends its digital certificate--which contains its public key and other neccesary security details.

**step 2 (Authentication):**
the brower then validate the server's digital certificate-- through its public key, to ensure it's communication with the original server

**step 3 (session key generated):**
After the certificate has been validated, both the client and server create a session key to encrypt any data transmitted

**step 4 (secure connection established):**
After the session key has been succesfully initiated, both client and server can now communicate securely-- you can now use your cards or interact safely with amazon online.

step 5 (closing the connection):
