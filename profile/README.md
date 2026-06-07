<h1 align="center">BulkSMSOnline</h1>
<p align="center">
  <strong>Global Bulk SMS Platform : Web, REST API & HTTP API</strong><br>
  Send marketing campaigns, alerts, OTPs, and notifications to 200+ countries.
</p>

<p align="center">
  <a href="https://bulksmsonline.com">
    <img src="https://img.shields.io/badge/Website-bulksmsonline.com-blue?style=flat-square" alt="Website" />
  </a>
  <a href="https://bulksmsonline.com/developers">
    <img src="https://img.shields.io/badge/Docs-API%20Reference-green?style=flat-square" alt="API Docs" />
  </a>
  <a href="https://github.com/BulkSMSOnline">
    <img src="https://img.shields.io/github/stars/BulkSMSOnline?style=flat-square" alt="GitHub Stars" />
  </a>
</p>

---

## 🚀 What is BulkSMSOnline?

A lightweight yet powerful bulk SMS platform built for **developers**, **marketers**, and **growing businesses**. Send thousands of messages instantly, track delivery in real time, and integrate using our modern REST APIs, all without telecom headaches.

---

## 🌐 API Endpoints

All API requests are made over HTTPS to `https://api.bulksmsonline.com`. The following endpoints are available:

| Endpoint          | Base URL                                             | Description                                                        |
| ----------------- | ---------------------------------------------------- | ------------------------------------------------------------------ |
| Send SMS          | `https://api.bulksmsonline.co/rest/api/v1/sms/send/` | Send single or bulk SMS (up to 30 numbers per request)             |
| Check Balance     | `https://api.bulksmsonline.co/balance`               | Query your current account credit balance                          |
| MNP Lookup        | `https://api.bulksmsonline.co/mnp`                   | check mobile number portability, roaming status and other HLR info |
| Number Validation | `https://api.bulksmsonline.co/mnv`                   | Validate format, country, operator, and line type of a number      |

All endpoints support **GET** and **POST** methods. HTTPS is enforced to ensure secure communication via SSL encryption.

For full parameter references, response formats, error codes, and code examples, visit the official [API Documentation](https://bulksmsonline.com/developers).

---

## 💥 Quick Start: Send Your First SMS

Send an SMS in seconds using the HTTP API. Replace `your_username` and `your_password` with your BulkSMSOnline account credentials.

### cURL

```bash
curl -X POST https://api.bulksmsonline.co/rest/api/v1/sms/send \
  -d "username=your_username" \
  -d "password=your_password" \
  -d "to=12345678900" \
  -d "from=MyBrand" \
  -d "text=Hello%20from%20BulkSMSOnline" \
  -d "type=0"
```

### Python

```bash
import http.client
import urllib.parse

params = urllib.parse.urlencode({
    'username': 'your_username',
    'password': 'your_password',
    'to': '12345678900',
    'from': 'MyBrand',
    'text': 'Hello from BulkSMSOnline',
    'type': '0'
})

headers = {'Content-Type': 'application/x-www-form-urlencoded'}

conn = http.client.HTTPSConnection("api.bulksmsonline.com")
conn.request("POST", "/rest/api/v1/sms/send", params, headers)
res = conn.getresponse()
print(res.read().decode("utf-8"))
```

### PHP

```bash
<?php
$curl = curl_init();

curl_setopt_array($curl, array(
    CURLOPT_URL => 'https://api.bulksmsonline.com/rest/api/v1/sms/send',
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_CUSTOMREQUEST => 'POST',
    CURLOPT_POSTFIELDS => 'username=your_username&password=your_password&to=12345678900&from=MyBrand&text=Hello%20from%20BulkSMSOnline&type=0',
    CURLOPT_HTTPHEADER => array('Content-Type: application/x-www-form-urlencoded'),
));

$response = curl_exec($curl);
curl_close($curl);
echo $response;
?>
```

### Successful Response:

```bash
OK: a1b2c3d4-e5f6-7890-abcd-ef1234567890
```
More code examples in C#, Java, Node.js, and other languages are available in the [Developer Hub](https://bulksmsonline.com/developers).

---

## 🧩 Integration Methods
BulkSMSOnline supports multiple protocols to fit any tech stack or architecture:

| Method        | Best For                                        | Documentation                                                         |
| ------------- | ----------------------------------------------- | --------------------------------------------------------------------- |
| HTTP(S) API   | Simple integrations, web apps, scripts          | [HTTP API Docs](https://bulksmsonline.com/developers#http-api)        |
| REST API (v1) | Modern applications, token-based authentication | [REST API Docs](https://bulksmsonline.com/developers#rest-api)        |
| Webhook (DLR) | Real-time delivery receipt callbacks            | [Webhook Docs](https://bulksmsonline.com/developers#delivery-reports) |

---

## ✨ Key Features

- 🌍 **Global reach** : Direct connections to carriers in 200+ countries
- ⚡ **Three sending modes** : Web portal, REST API, or HTTP API
- 📊 **Real‑time reports** : Delivery status, click tracking, and webhook callbacks
- 🧩 **Easy integration** : Ready‑to‑use Postman collections, OpenAPI specs, and SDK snippets
- 🔒 **Secure & compliant** : HTTPS, data encryption, and GDPR‑friendly
- 💰 **Pay‑as‑you‑go** : No setup fees, transparent pricing, volume discounts

---

## 🤝 Why choose us?
Small team, big impact : direct access to the engineers who build the platform

Reliable infrastructure : carrier‑grade delivery with 99.9% uptime

Transparent & honest : clear pricing, no hidden limits, real support

---

## 📫 Get in touch
🌐 Website: <a href="https://bulksmsonline.com">bulksmsonline.com</a>

📧 Email: help@bulksmsonline.com

💬 Live chat on the <a href="https://bulksmsonline.com">website</a> for instant help 
