# 📅 Day 1 – Introduction to Web Services & SOA

---

## 1️⃣ What is a Web Service?

A **Web Service** is a software component that enables communication between two applications over a network using standard protocols like:

* HTTP
* XML
* JSON

It allows:

* Java ↔ .NET communication
* Different platforms to interact
* Platform-independent integration

### 💡 Example

A bank server exposes:

```
getBalance(accountNo)
```

Clients such as:

* Mobile App
* Website
* ATM

can call this service over the network.

---

## 2️⃣ Why Do We Need Web Services?

### Before Web Services

* Applications were tightly coupled
* Platform dependent
* Hard to integrate
* Poor reusability

### Web Services Provide

* ✔ Interoperability
* ✔ Platform Independence
* ✔ Loose Coupling
* ✔ Reusability

---

## 3️⃣ What is SOA (Service Oriented Architecture)?

**SOA** is an architectural style where applications are built using reusable services.

Instead of building one large system:

* Break system into small services
* Each service performs one specific task
* Services communicate over a network

---

## 🏗 SOA Basic Architecture

### Components:

1. **Service Provider**

   * Creates the service
   * Publishes service details

2. **Service Consumer (Client)**

   * Finds the service
   * Invokes the service

3. **Service Registry (UDDI)**

   * Stores service information
   * Helps consumers discover services

---

## 🔄 SOA Interaction Flow

1. Provider publishes service in registry
2. Consumer searches registry
3. Consumer binds and invokes service

---

## 4️⃣ Web Service Architecture Layers

```
Client
   ↓
SOAP / REST Message
   ↓
HTTP Protocol
   ↓
Web Server (Tomcat)
   ↓
Business Logic (Java Code)
```

### Explanation:

* Client sends request
* Request formatted as SOAP (XML) or REST (JSON/XML)
* HTTP carries the message
* Server processes request
* Business logic executes
* Response returned

---

## 5️⃣ Types of Web Services

---

### A) SOAP Web Services

* Uses XML only
* Strict standard
* Uses WSDL
* Protocol based
* High security (WS-Security)
* More complex

Used in:

* Banking systems
* Enterprise applications
* Government systems

---

### B) RESTful Web Services

* Uses JSON (mostly)
* Lightweight
* Uses HTTP methods
* Simple and fast
* Easy to implement

Used in:

* Mobile apps
* Web applications
* Microservices
* Cloud APIs

---

## 🔥 SOAP vs REST Comparison

| Feature       | SOAP               | REST                |
| ------------- | ------------------ | ------------------- |
| Format        | XML only           | JSON / XML          |
| Speed         | Slower             | Faster              |
| Security      | High (WS-Security) | Moderate            |
| Complexity    | High               | Simple              |
| WSDL Required | Yes                | No                  |
| Protocol Type | Protocol           | Architectural style |

---

## 6️⃣ Basic Web Technologies Revision

---

### ✔ HTTP Methods

* **GET** → Retrieve data
* **POST** → Send new data
* **PUT** → Update data
* **DELETE** → Remove data

---

### ✔ XML Basics

```xml
<student>
   <name>Yash</name>
   <marks>85</marks>
</student>
```

---

## 🧠 Important Concepts

### 🔹 Interoperability

Ability of different systems (Java, .NET, Python) to communicate.

### 🔹 Loose Coupling

Services are independent.
Changing one service does not break others.

---

## 🧪 Practice Tasks

Draw in your notebook:

1. SOA diagram
2. Web service request–response flow
3. SOAP message structure (Envelope + Body)

---

## 🎯 Study Plan (4 Hours)

| Task                | Duration |
| ------------------- | -------- |
| Theory Reading      | 1.5 hr   |
| Diagram Practice    | 1 hr     |
| XML + HTTP Revision | 1 hr     |
| Concept Revision    | 30 min   |

---

## 🚀 Why This Is Important

This foundation connects directly with:

* Spring Boot APIs
* Microservices
* Backend system design
* Cloud deployment
* Distributed systems
* API-based architectures

---

## 📌 Interview Questions

1. What is a Web Service?
2. What is SOA?
3. Difference between SOAP and REST?
4. What is interoperability?
5. What is loose coupling?