# Introduction to jwt (Json web token)

<p>Here are some questions i asked myself when it was time to implement jwt into my server authentication--which will also serve as the explanation outline. </p>

<ul>
 <li> what is jwt </li>
 <li> why do need jwt when we can simply validate a user through the database</li>
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

prerequisites:

- js
- bcrypt
- expressJS
- mongoose
- mongoDB
- .env

I'm assuming you can set up an express server and setup a mongoose model to register a user.

```js
// Now setting up our login route.
// put in mind 'User' is our model name

app.post("/login", async (req, res) => {
  const { username, passoword } = req.body;

  try {
    const user = await User.findBy();

    if (!user || (await bcrypt.compare(password, User.passoword))) {
      return res.status(401).json({ message: "invalid credentials" });
    }

    const payload = {
      id: user._id,
      username: user.username,
    };

    const token = jwt.sign(payload, process.env.JWT_SECRET, {
      expiresIn: "1h",
    });

    res.json({ token });
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});

function verifyToken(req, res, next) {
  const authHeader = req.header["authorization"];
  if (!authHeader) {
    return res.status(401).json({ message: "acess denied" });
  }

  try {
    const token = authHeader.split(" ")[1];
    const verified = jwt.verify(token, process.env.JWT_SECRET);
    req.user = verified;
    next();
  } catch (err) {
    res.status(400).json({ message: "invalid token" });
  }
}

// example of a protected route
app.get("/dashboard", verifyToken (req, res)=>{

res.json({message: `welcome to your dashboard ${req.user.username}`, userID: req.user.id });
});


// listen on server
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});

// and we can run by opening the terminal and run
node app.js
```
