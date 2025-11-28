
# HTTP Basics — Interview Questions & Answers

## Q1 — What is HTTP?
**Short answer:**  
HTTP (HyperText Transfer Protocol) is the foundation for communication between client and server on the web. 
HTTP defines how requests (from client) and responses (from server) are transferred.  
It is **stateless**, meaning each request is independent — server doesn’t remember previous ones.

---

## Q2 — What is the difference between HTTP and HTTPS?
**Short answer:**  
HTTPS = HTTP with encryption using SSL/TLS.

**HTTPS provides:**
- **Encryption** → data cannot be read by attackers  
- **Authentication** → ensures you're talking to the real server  
- **Integrity** → data can’t be modified in transit  

---

## Q3 — What is a Request Method in HTTP?
Methods tell the server **what action** the client wants.

**Common methods:**
- **GET** → fetch data  
- **POST** → send data/create  
- **PUT** → update whole resource  
- **PATCH** → partial update  
- **DELETE** → delete resource  

---

## Q4 — What is a Status Code?
A 3-digit number that tells the result of the request.

**Categories:**
- **1xx** → Informational  
- **2xx** → Success  
- **3xx** → Redirect  
- **4xx** → Client error  
- **5xx** → Server error  

Examples:  
- **200 OK** → request successful  
- **201 Created** → resource created  
- **400 Bad Request** → client sent invalid data  
- **401 Unauthorized** → no valid auth  
- **404 Not Found** → resource not found  
- **500 Internal Server Error** → server crashed  

---

## Q5 — What are HTTP Headers?
Headers are extra information sent along with request or response.

**Examples:**
- `Content-Type: application/json`  
- `Authorization: Bearer <token>`  
- `Cookie: session_id=123`  
- `Cache-Control: no-cache`  

---

## Q6 — What is the difference between PUT and PATCH?
- **PUT** → replaces the entire resource  
- **PATCH** → updates only the specific fields  

Example:  
Updating only the email → PATCH  
Updating name + email + age → PUT  

---

## Q7 — What is a Query Parameter vs Path Parameter?

### **Path parameter (/:id)**
Identifies a specific resource.  
Example:  
`/users/10` → user with ID 10

### **Query parameter (?key=value)**
Used for filtering, sorting, searching.  
Example:  
`/users?limit=10&page=2`

---

## Q8 — What is a Request Body?
The data sent inside a POST/PUT/PATCH request.

Example:
```json
{
  "email": "test@example.com",
  "password": "1234"
}
