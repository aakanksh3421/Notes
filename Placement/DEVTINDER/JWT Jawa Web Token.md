### **Why Do u need JWT in ur proj ?**

"In my application, JWT is used on every API request to protected routes. The client stores the token (usually in cookies), and each time it calls a protected API, the token is sent along. The server verifies the token, extracts the user ID, fetches the user from the database, and only then allows the request to proceed. This way, we make sure the user is authenticated before accessing sensitive operations."

### **Why did you put `getJWT()` inside the user model instead of writing it in the route?”**, you can give a clear, simple answer like this:


**Answer:**

> I made `getJWT()` a method on the user model so that token creation is tied directly to the user object. This way, whenever I have a user instance, I can easily generate a token without repeating code in multiple routes.  
> It also keeps the logic organized — the model handles user-related operations, while the routes just handle requests and responses. This follows the idea of keeping business logic inside models and keeping controllers/routes clean.

---

If they push further, you can add:

> Also, since `getJWT()` is on the model, it can directly access that specific user’s properties using `this`, like the user’s `_id`, when creating the token.

## Possible Questions

- **What is JWT and why are you using it here?**
    
- **What information does your JWT payload contain in this project?**
    
- **Where is the JWT stored on the client side? Why?**
    
- **How does the server verify the token?**
    
- **What happens if the token is missing or expired?**
    
- **Why do you fetch the user from the database after decoding the token?**
    
- **Why are you using `_id` from the token instead of the email?**
    
- **What is the purpose of `req.user` in `userAuth` middleware?**
    
- **Can someone change the JWT on the client side and still get access? Why or why not?**
    
- **How would you handle token expiration in your application?**

### WIth answers 

- **What is JWT and why are you using it here?**  
    → JWT is a digital token to identify a logged-in user without storing session data on the server.
    
- **What information does your JWT payload contain in this project?**  
    → It contains the user’s `_id` from the database.
    
- **Where is the JWT stored on the client side? Why?**  
    → In cookies, so it’s sent automatically with each request.
    
- **How does the server verify the token?**  
    → By using the `jwt.verify()` function with the secret key.
    
- **What happens if the token is missing or expired?**  
    → The server sends a "Please Login" or error response.
    
- **Why do you fetch the user from the database after decoding the token?**  
    → To make sure the user still exists and has up-to-date details.
    
- **Why are you using `_id` from the token instead of the email?**  
    → `_id` is unique and never changes, while an email can change.
    
- **What is the purpose of `req.user` in `userAuth` middleware?**  
    → To pass the logged-in user’s details to the next route handler.
    
- **Can someone change the JWT on the client side and still get access? Why or why not?**  
    → No, because the signature will break if the token is tampered with.
    
- **How would you handle token expiration in your application?**  
    → By setting an expiry when creating the token and asking the user to log in again when it expires.