# Day 12 — Wireshark Introduction

**Environment:** Kali Linux

## Topics
- **Main Topic:** HTTP and HTTPS
- **Focus:** Requests, Responses, and TLS

## Learning Notes

HTTP stands for **Hypertext Transfer Protocol**. It is a communication protocol that allows web browsers and web servers to exchange information.

When I visit a website, my browser sends an HTTP request to the web server. The server processes the request and sends back an HTTP response.

### 1. HTTP Requests

An HTTP request is a message sent by a client, such as a web browser, to a web server.

Common HTTP request methods include:

- **GET:** Requests information from a server.
- **POST:** Sends information to a server.
- **PUT:** Creates or replaces a resource.
- **DELETE:** Requests removal of a resource.

For example, when opening a webpage, a browser commonly sends a GET request to retrieve its content.

### 2. HTTP Responses

An HTTP response is the message returned by a web server after receiving a request.

It usually contains:
- A status code.
- Response headers.
- A response body, which may contain HTML, JSON, or other data.

Common HTTP status codes include:

| Status code | Meaning |
|---|---|
| 200 | OK – Request succeeded |
| 301 | Moved permanently |
| 400 | Bad request |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Internal server error |

### 3. HTTPS

HTTPS stands for **Hypertext Transfer Protocol Secure**. It is HTTP communication protected using TLS (Transport Layer Security).

TLS provides three important protections:

- **Encryption:** Helps prevent unauthorized parties from reading transmitted data.
- **Authentication:** Uses digital certificates to help verify a server's identity.
- **Integrity:** Helps detect unauthorized changes to data during transmission.

HTTPS commonly uses TCP port 443, while ordinary HTTP commonly uses TCP port 80.

### 4. HTTP and HTTPS Comparison

| HTTP | HTTPS |
|---|---|
| Does not provide TLS protection by itself | Uses TLS protection |
| Commonly uses port 80 | Commonly uses port 443 |
| Data is not protected by TLS | Data is encrypted in transit using TLS |
| Less suitable for sensitive communication | Preferred for secure web communication |

## Practical Work and Tools

- **What I actually did:** Studied HTTP requests, responses, common status codes, and the purpose of TLS in HTTPS. Specific practical web requests have not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No specific web inspection tools are confirmed.
- **Evidence:** Learning notes comparing HTTP and HTTPS and explaining common request methods and response codes.

## Key Takeaways

- HTTP allows browsers and servers to communicate.
- Requests are sent by clients, and responses are returned by servers.
- GET and POST are common HTTP methods.
- Status codes indicate the result of a request.
- HTTPS uses TLS to protect communication.
- TLS provides encryption, authentication, and integrity protections.

**Commands to remember:**

```bash
curl -I https://example.com
curl -X GET https://example.com
```

The first command requests response headers. The second sends a GET request and displays the response body.

## Challenges and Questions

I am still learning how HTTP headers, status codes, and TLS certificates work together. I want to understand how a browser verifies a website's certificate and how HTTPS protects information during communication.

## Reflection

Today, I learned about HTTP and HTTPS and how browsers communicate with web servers through requests and responses. I understood that HTTP methods perform different actions and that status codes describe the outcome of requests. I also learned that HTTPS uses TLS to provide encryption, authentication, and integrity. I want to review HTTP status codes and understand the TLS certificate verification process more clearly.

## Safety

Only inspect websites and systems I own or have explicit permission to assess. I will use public example websites for basic learning, avoid submitting private information to unknown websites, and never include passwords, keys, personal data, or private system details in my training diary.
