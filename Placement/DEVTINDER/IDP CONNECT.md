## **1. Express & Routing Basics**

- **What is Express?**
    
- **What is `express.Router()` and why do we use it instead of `app` directly?**
    
- **What are `req` and `res` objects?**
    
- **What is middleware in Express and where could it fit in this code?**
    
- **How would you protect certain routes so only logged-in users can access them?**
    

---

## **2. Authentication Flow & Security**

- **What is JWT and why are we using it instead of sessions?**
    
- **What is inside a JWT payload, and what should _never_ be inside it?**
    
- **How does JWT verification work on the server side?**
    
- **How would you store JWT on the client? Why cookies in this case?**
    
- **What is the difference between storing JWT in cookies vs. localStorage?**
    
- **Why is hashing passwords important?**
    
- **What’s the difference between hashing and encryption?**
    
- **Why use `bcrypt` and what does salt rounds mean?**
    
- **Can someone forge a JWT? How do you prevent that?**
    
- **What is the risk if JWT secret is leaked?**
    

---

## **3. Mongoose & Model Methods**

- **What does `userSchema.methods.validatePassword` do?**
    
- **Why define `validatePassword` as a model method instead of doing bcrypt directly in the route?**
    
- **What is `user.save()` actually doing?**
    
- **What’s the difference between `User.findOne()` and `User.findById()`?**
    
- **Why make `getJWT()` a model method?**
    

---

## **4. Error Handling**

- **How is error handling done in your routes?**
    
- **What happens if `validateSignUpData` fails?**
    
- **What status code should be sent for invalid credentials?**
    
- **How can you send more descriptive error messages without exposing sensitive info?**
    

---

## **5. Deep-Dive / Follow-Up**

If the interviewer wants to push further:

- **How do you invalidate a JWT before its expiry?**
    
- **What happens if a JWT is stolen?**
    
- **How would you handle refresh tokens and access tokens?**
    
- **How would you make this system scale across multiple servers?**
    
- **How would you secure this against CSRF attacks if you’re using cookies?**
    
- **Why is `expires` set to 8 hours, and how would you make it configurable?**
    
- **What happens if `bcrypt.compare` is slow — how would you optimize login performance?**