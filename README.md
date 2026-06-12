
# 🚀 100 Days of Python API Challenge

Build one API every day and gradually move from beginner to advanced topics.

This challenge covers:
- REST APIs
- Databases
- Authentication
- Caching
- External APIs
- AI APIs
- Real-time systems
- Microservices

---

# 👋 Hello World API (FastAPI)

A **Hello World API** is the simplest web API. It introduces the core concepts of API development.

## What you will learn
- Creating an API endpoint
- Handling HTTP requests
- Sending JSON responses
- Running a web server
- Testing APIs

Think of it as:
> The API version of `print("Hello, World!")`

---

## 🔁 How It Works

```

Client (Browser/Postman)
⬇️ HTTP Request
GET /
⬇️
Server (FastAPI)
⬇️ HTTP Response
{
"message": "Hello, World!"
}

```

---

## 📦 Example

### Request
```

GET [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

````

### Response
```json
{
  "message": "Hello, World!"
}
````

---

## 📁 Project Structure

```
hello-world-api/
│
├── app.py
├── requirements.txt
└── main
```

---

## ⚙️ Step 1: Install FastAPI

```bash
pip install fastapi uvicorn
```

Save dependencies:

```bash
pip freeze > requirements.txt
```

---

## 🧠 Step 2: Create `app.py`

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Hello, World!"}
```

---

## ▶️ Step 3: Run Server

```bash
uvicorn app:app --reload
```

Server will run at:

```
http://127.0.0.1:8000
```

---

## 🧪 Step 4: Test API

Open in browser:

```
http://127.0.0.1:8000/
```

Response:

```json
{
  "message": "Hello, World!"
}
```

---

## 📚 Step 5: Swagger Documentation

FastAPI provides automatic API docs.

Swagger UI:

```
http://127.0.0.1:8000/docs
```

ReDoc:

```
http://127.0.0.1:8000/redoc
```

---

# 🛣️ Learning Roadmap

## Level 1 — Basic Endpoint

### Goal

Create one route that returns JSON.

### Learn

* What is an API?
* HTTP Request & Response
* GET method
* JSON response

### Example

```python
@app.get("/")
```

---

## Level 2 — Multiple Endpoints

### Routes

```python
@app.get("/")
@app.get("/about")
@app.get("/contact")
```

### Example Responses

```json
{ "name": "Savindu" }
{ "email": "admin@example.com" }
```

### Learn

* Routing
* Endpoints
* JSON responses

---

## Level 3 — Path Parameters

### Request

```
GET /hello/Savindu
```

### Code

```python
@app.get("/hello/{name}")
def greet(name: str):
    return {"message": f"Hello {name}"}
```

### Response

```json
{
  "message": "Hello Savindu"
}
```

---

## Level 4 — Query Parameters

### Request

```
GET /square?number=5
```

### Code

```python
@app.get("/square")
def square(number: int):
    return {"result": number ** 2}
```

### Response

```json
{
  "result": 25
}
```

---

## Level 5 — POST Request

### Request Body

```json
{
  "name": "Savindu"
}
```

### Response

```json
{
  "message": "Welcome Savindu"
}
```

### Learn

* POST method
* Request body
* Pydantic models

---

## Level 6 — Error Handling

### Code

```python
from fastapi import HTTPException

@app.get("/age/{age}")
def check_age(age: int):
    if age < 0:
        raise HTTPException(
            status_code=400,
            detail="Age cannot be negative"
        )
    return {"age": age}
```

### Learn

* Status codes
* Exception handling

---

## Level 7 — API Documentation

FastAPI automatically generates:

* Swagger UI → `/docs`
* ReDoc → `/redoc`

---

# 🎯 Mini Challenges

## Challenge 1

```
GET /hello
```

Response:

```json
{ "message": "Hello World" }
```

---

## Challenge 2

```
GET /name
```

Response:

```json
{ "name": "Savindu" }
```

---

## Challenge 3

```
GET /hello/{name}
```

Example:

```
/hello/Alice
```

Response:

```json
{ "message": "Hello Alice" }
```

---

## Challenge 4

```
GET /add?a=10&b=20
```

Response:

```json
{ "result": 30 }
```

---

## Challenge 5

```
POST /welcome
```

Input:

```json
{ "name": "Bob" }
```

Response:

```json
{ "message": "Welcome Bob" }
```

---

# 🧠 Skills You’ll Learn

✅ FastAPI basics
✅ HTTP methods (GET, POST)
✅ Routes and endpoints
✅ Path & query parameters
✅ JSON requests & responses
✅ Pydantic models
✅ Error handling
✅ API documentation
✅ Uvicorn server

---

# 🚀 Next Step

After completing this, you’ll be ready for:

* Todo APIs
* Blog APIs
* Authentication systems
* Database-backed APIs
* AI-powered APIs


