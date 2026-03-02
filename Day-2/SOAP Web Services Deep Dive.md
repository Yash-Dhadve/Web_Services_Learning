# 📅 Day 2 – SOAP Web Services Deep Dive

---

## 1️⃣ What is SOAP?

**SOAP (Simple Object Access Protocol)** is a protocol used to exchange structured information between applications over a network.

### Key Points

* Uses **XML**
* Works over **HTTP**
* Platform independent
* Language independent
* Standardized communication format

👉 Think of SOAP as a **standard XML envelope** that carries your method call over the network.

---

## 2️⃣ SOAP Message Structure

A SOAP message has 4 main parts:

```xml
<Envelope>
    <Header> (Optional) </Header>
    <Body>
        <Fault> (Optional) </Fault>
    </Body>
</Envelope>
```

---

## 🧱 SOAP Structure Overview

* **Envelope** → Root element
* **Header** → Metadata (optional)
* **Body** → Actual data
* **Fault** → Error information (optional)

---

## 3️⃣ SOAP Envelope

The **Envelope** is the root element of every SOAP message.

It defines:

* SOAP version
* XML namespace

### Example

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
</soap:Envelope>
```

👉 Without Envelope, the message is not a valid SOAP message.

---

## 4️⃣ SOAP Header (Optional)

The **Header** carries metadata about the message.

### Used For:

* Security (WS-Security)
* Authentication
* Transactions
* Routing
* Session management

### Example

```xml
<soap:Header>
   <auth>
      <username>yash</username>
   </auth>
</soap:Header>
```

👉 Header is optional but very important in enterprise systems.

---

## 5️⃣ SOAP Body (Main Part)

The **Body** contains:

* Actual method call
* Parameters
* Business data

### Example – Factorial Request

```xml
<soap:Body>
   <getFactorial>
      <number>5</number>
   </getFactorial>
</soap:Body>
```

---

## 6️⃣ SOAP Response Example

```xml
<soap:Body>
   <getFactorialResponse>
      <result>120</result>
   </getFactorialResponse>
</soap:Body>
```

👉 Server always returns response inside `<soap:Body>`.

---

## 7️⃣ SOAP Fault (Error Handling)

If an error occurs, SOAP returns a **Fault** element.

### Example

```xml
<soap:Fault>
   <faultcode>soap:Client</faultcode>
   <faultstring>Invalid Input</faultstring>
</soap:Fault>
```

### Important Fault Elements

* **faultcode** → Type of error
* **faultstring** → Error description

🔥 Very important for exams and viva.

---

## 🔄 How SOAP Works (Flow)

1️⃣ Client creates SOAP XML
2️⃣ Client sends request via **HTTP POST**
3️⃣ Server processes request
4️⃣ Server returns SOAP XML response

---

## 🆚 RPC Style vs Document Style

---

### 🔹 RPC Style

Looks like a method call.

```xml
<getBalance>
   <accNo>101</accNo>
</getBalance>
```

* Method-centric
* Operation focused

---

### 🔹 Document Style

Structured XML document.

```xml
<bankRequest>
   <account>
      <number>101</number>
   </account>
</bankRequest>
```

* Document-centric
* More flexible
* Used in modern SOAP services

👉 Most modern SOAP implementations use **Document Style**.

---

## ⚡ SOAP Characteristics (Exam Points)

* ✔ XML based
* ✔ Language independent
* ✔ Platform independent
* ✔ Uses WSDL
* ✔ Supports WS-Security
* ✔ Works over HTTP
* ✔ Slower than REST
* ✔ Strict messaging format

---

## 🧠 Important Viva Questions

1. What is SOAP?
2. What are parts of a SOAP message?
3. Difference between SOAP Header and SOAP Body?
4. What is SOAP Fault?
5. What is namespace in SOAP?
6. Difference between RPC and Document style?

---

## 🧪 Practical Task

Do this manually in Notepad:

1️⃣ SOAP request for Celsius → Fahrenheit
2️⃣ SOAP response with result
3️⃣ SOAP Fault for invalid temperature

👉 Focus on correct XML structure.

---

## 📊 Study Plan (4 Hours)

| Task                       | Duration |
| -------------------------- | -------- |
| SOAP Theory                | 1.5 hr   |
| Write SOAP XML Manually    | 1 hr     |
| RPC vs Document Comparison | 30 min   |
| Revise Day 1 + Day 2       | 1 hr     |

---

## 🔜 Coming Next (Day 3 Preview)

* WSDL Deep Dive
* Elements of WSDL
* How SOAP + WSDL connect
* Binding and Port types
* Real service definition understanding
