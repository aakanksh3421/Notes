## PHP

In PHP 7, type declarations were added. This gives us an option to specify the expected data type when declaring a function, and by adding the `strict` declaration, it will throw a "Fatal Error" if the data type mismatches.

## GET vs. POST

Both GET and POST create an array (e.g. array( key1 => value1, key2 => value2, key3 => value3, ...)). This array holds key/value pairs, where keys are the names of the form controls and values are the input data from the user.

Both GET and POST are treated as $_GET and $_POST. These are superglobals, which means that they are always accessible, regardless of scope - and you can access them from any function, class or file without having to do anything special.

$_GET is an array of variables passed to the current script via the URL parameters.

$_POST is an array of variables passed to the current script via the HTTP POST method.

---

### When to use GET?

Information sent from a form with the GET method is **visible to everyone** (all variable names and values are displayed in the URL). GET also has limits on the amount of information to send. The limitation is about 2000 characters. However, because the variables are displayed in the URL, it is possible to bookmark the page. This can be useful in some cases.

GET may be used for sending non-sensitive data.

**Note:** GET should NEVER be used for sending passwords or other sensitive information!

---

### When to use POST?

Information sent from a form with the POST method is **invisible to others** (all names/values are embedded within the body of the HTTP request) and has **no limits** on the amount of information to send.

Moreover POST supports advanced functionality such as support for multi-part binary input while uploading files to server.

However, because the variables are not displayed in the URL, it is not possible to bookmark the page.

**Developers prefer POST for sending form data.**

| Aspect                    | GET in PHP                                          | POST in PHP                                                                 |
| ------------------------- | --------------------------------------------------- | --------------------------------------------------------------------------- |
| **Superglobal**           | `$_GET[]`                                           | `$_POST[]`                                                                  |
| **Where data comes from** | URL query string                                    | Request body                                                                |
| **Size limit**            | Limited (~2000 chars, browser/server dependent)     | Much larger (depends on `post_max_size` in `php.ini`)                       |
| **Security**              | Exposed in URL, stored in browser history and logs  | Hidden from URL but still visible in request (use HTTPS for sensitive data) |
| **When to use**           | Passing parameters, search filters, page navigation | Form submissions, file uploads, sensitive data                              |


## Cookiee
A cookie is often used to identify a user. A cookie is a small file that the server embeds on the user's computer. Each time the same computer requests a page with a browser, it will send the cookie too. With PHP, you can both create and retrieve cookie values.
A cookie is created with the `[setcookie()]

#### Syntax

setcookie(_name, value, expire, path, domain, secure, httponly_);

#### Delete a Cookie

To delete a cookie, use the `[setcookie()](https://www.w3schools.com/php/func_network_setcookie.asp)` function with an expiration date in the past:


## PHP Sessions



A session is a way to store information (in variables) to be used across multiple pages.

Unlike a cookie, the information is not stored on the users computer.

When you work with an application, you open it, do some changes, and then you close it. This is much like a Session. The computer knows who you are. It knows when you start the application and when you end. But on the internet there is one problem: the web server does not know who you are or what you do, because the HTTP address doesn't maintain state.

Session variables solve this problem by storing user information to be used across multiple pages (e.g. username, favorite color, etc). By default, session variables last until the user closes the browser.

So; Session variables hold information about one single user, and are available to all pages in one application.

# XML
![[Pasted image 20250812010843.png]]
### XML Naming Rules

XML elements must follow these naming rules:

- Element names are case-sensitive
- Element names must start with a letter or underscore
- Element names cannot start with the letters xml (or XML, or Xml, etc)
- Element names can contain letters, digits, hyphens, underscores, and periods
- Element names cannot contain spaces

### Attributes

Some things to consider when using attributes are:

- attributes cannot contain multiple values (elements can)
- attributes cannot contain tree structures (elements can)
- attributes are not easily expandable (for future changes
- 
### **PDATA (Parsed Character Data)**

- **Full form**: _Parsed Data_
    
- This is **normal text** in XML.
    
- The XML parser **parses it** — meaning it checks for tags, entities, and interprets them.
    
- Special characters like `<`, `>` and `&` **must** be escaped.
    
    - `<` becomes `&lt;`
        
    - `>` becomes `&gt;`
        
    - `&` becomes `&amp;`
        

**Example (PData)**:



`<message>Hello &lt;World&gt;</message>`

The XML parser will read the value as:



`Hello <World>`

---

## **2. CDATA (Character Data)**

- **Full form**: _Character Data_ section.
    
- Used when you want the parser **NOT** to interpret anything inside.
    
- Everything between `<![CDATA[` and `]]>` is treated as **raw text** — no parsing, no entity replacement.
    
- Useful for including code snippets, HTML, or special characters.
    

**Example (CDATA)**:



`<message><![CDATA[Hello <World> & Goodbye]]></message>`

| Feature       | PData                | CData                                           |
| ------------- | -------------------- | ----------------------------------------------- |
| Parsing       | Parsed by XML parser | Not parsed — stored as raw text                 |
| Special chars | Must be escaped      | Can be written as-is                            |
| Use case      | Normal text content  | Embed code, HTML, scripts, or text with symbols |

## DTD

## XML Schemas Support Data Types

One of the greatest strength of XML Schemas is the support for data types.

- It is easier to describe allowable document content
- It is easier to validate the correctness of data
- It is easier to define data facets (restrictions on data)
- It is easier to define data patterns (data formats)
- It is easier to convert data between different data types

---

## XML Schemas use XML Syntax

Another great strength about XML Schemas is that they are written in XML.

- You don't have to learn a new language
- You can use your XML editor to edit your Schema files
- You can use your XML parser to parse your Schema files
- You can manipulate your Schema with the XML DOM
- You can transform your Schema with XSLT

XML Schemas are extensible, because they are written in XML.

With an extensible Schema definition you can:

- Reuse your Schema in other Schemas
- Create your own data types derived from the standard types
- Reference multiple schemas in the same document