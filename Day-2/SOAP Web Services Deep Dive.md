📅 Day 2 – SOAP Web Services Deep Dive
1️⃣ What is SOAP?

SOAP (Simple Object Access Protocol) is a protocol used to exchange structured information between applications over a network.

Key Points

Uses XML

Works over HTTP

Platform independent

Language independent

Standardized communication format

👉 Think of SOAP as a standard XML envelope that carries your method call over the network.

2️⃣ SOAP Message Structure

A SOAP message has 4 main parts:

<Envelope>
    <Header> (Optional) </Header>
    <Body>
        <Fault> (Optional) </Fault>
    </Body>
</Envelope>
🧱 SOAP Structure Overview

Envelope → Root element

Header → Metadata (optional)

Body → Actual data

Fault → Error information (optional)

3️⃣ SOAP Envelope

The Envelope is the root element of every SOAP message.

It defines:

SOAP version

XML namespace

Example
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
</soap:Envelope>

👉 Without Envelope, the message is not a valid SOAP message.

4️⃣ SOAP Header (Optional)

The Header carries metadata about the message.

Used For:

Security (WS-Security)

Authentication

Transactions

Routing

Session management

Example
<soap:Header>
   <auth>
      <username>yash</username>
   </auth>
</soap:Header>

👉 Header is optional but very important in enterprise systems.

5️⃣ SOAP Body (Main Part)

The Body contains:

Actual method call

Parameters

Business data

Example – Factorial Request
<soap:Body>
   <getFactorial>
      <number>5</number>
   </getFactorial>
</soap:Body>
6️⃣ SOAP Response Example
<soap:Body>
   <getFactorialResponse>
      <result>120</result>
   </getFactorialResponse>
</soap:Body>

👉 Server always returns response inside <soap:Body>.

7️⃣ SOAP Fault (Error Handling)

If an error occurs, SOAP returns a Fault element.

Example
<soap:Fault>
   <faultcode>soap:Client</faultcode>
   <faultstring>Invalid Input</faultstring>
</soap:Fault>
Important Fault Elements

faultcode → Type of error

faultstring → Error description

🔥 Very important for exams and viva.

🔄 How SOAP Works (Flow)

1️⃣ Client creates SOAP XML
2️⃣ Client sends request via HTTP POST
3️⃣ Server processes request
4️⃣ Server returns SOAP XML response

🆚 RPC Style vs Document Style
🔹 RPC Style

Looks like a method call.

<getBalance>
   <accNo>101</accNo>
</getBalance>

Method-centric

Operation focused

🔹 Document Style

Structured XML document.

<bankRequest>
   <account>
      <number>101</number>
   </account>
</bankRequest>

Document-centric

More flexible

Used in modern SOAP services

👉 Most modern SOAP implementations use Document Style.

⚡ SOAP Characteristics (Exam Points)

✔ XML based

✔ Language independent

✔ Platform independent

✔ Uses WSDL

✔ Supports WS-Security

✔ Works over HTTP

✔ Slower than REST

✔ Strict messaging format

🧠 Important Viva Questions

What is SOAP?

What are parts of a SOAP message?

Difference between SOAP Header and SOAP Body?

What is SOAP Fault?

What is namespace in SOAP?

Difference between RPC and Document style?

🧪 Practical Task

Do this manually in Notepad:

1️⃣ SOAP request for Celsius → Fahrenheit
2️⃣ SOAP response with result
3️⃣ SOAP Fault for invalid temperature

👉 Focus on correct XML structure.

📊 Study Plan (4 Hours)
Task	Duration
SOAP Theory	1.5 hr
Write SOAP XML Manually	1 hr
RPC vs Document Comparison	30 min
Revise Day 1 + Day 2	1 hr