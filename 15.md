# What is a Reverse Proxy?

A **reverse proxy** is a server that sits in front of web servers and forwards client requests (like those from your web browser) to those web servers. It is mainly used to improve website security, performance, and reliability.

---

## What is a Proxy Server?

There are two types of proxy servers:

- **Forward Proxy** (normal proxy)
- **Reverse Proxy**

Let’s first understand the forward proxy.

---

### What is a Forward Proxy?

A **forward proxy** is a server that sits in front of clients. When a client (like your computer) tries to access a website on the internet, the request goes first to the forward proxy. The proxy then sends that request to the website’s server.

**Example:**

- Computer A: Your home computer (client)
- Server B: Forward proxy server
- Server C: Website’s origin server (where the actual website data resides)

Normally, A sends a request directly to C and receives a response.

But with a forward proxy:

- A sends the request to B,
- B forwards the request to C,
- C sends the response back to B,
- B then forwards the response to A.

---

### Why Use a Forward Proxy?

- To bypass internet restrictions found in places like schools, offices, or certain countries.
- To block certain content, like Facebook or social media.
- To provide online anonymity by hiding your real IP address.

---

## What is the Difference Between a Forward Proxy and a Reverse Proxy?

A **reverse proxy** is also a proxy server, but it sits **in front of the web servers**, not the clients.

- Forward proxy sits in front of **clients**.
- Reverse proxy sits in front of **servers**.

This means:

- When a client sends a request to a website’s origin server,
- The request first reaches the reverse proxy,
- The reverse proxy forwards the request to the origin server,
- The origin server sends the response to the reverse proxy,
- The reverse proxy then forwards the response to the client.

---

### Reverse Proxy Example:

- D: Many users’ computers (clients)
- E: Reverse proxy server
- F: Origin server(s)

Normally, D communicates directly with F.

With a reverse proxy:

- D sends the request to E,
- E sends the request to F,
- F sends the response to E,
- E forwards the response to D.

---

## Benefits of a Reverse Proxy

- **Load Balancing:** If a website has a lot of traffic, the reverse proxy distributes traffic across multiple servers to prevent any one server from being overloaded.
- **Attack Protection:** The origin server’s real IP address is hidden. Attackers can only target the reverse proxy, which usually has better security. This helps protect against attacks like DDoS.
- **Global Server Load Balancing (GSLB):** If website servers are located in different countries, the reverse proxy connects clients to the nearest server, speeding up loading times.
- **Caching:** The reverse proxy can temporarily store (cache) some content. For example, a user in Paris can get website data from a Paris-based reverse proxy instead of a server in L.A., making the site load faster.
- **SSL Encryption:** The reverse proxy handles encryption and decryption, reducing the load on the origin server and saving its resources.

---

## How to Implement a Reverse Proxy?

Building a reverse proxy yourself requires significant software and hardware resources.

Because of this, many companies use CDN (Content Delivery Network) services like **Cloudflare CDN**, which provide all reverse proxy features — security, performance, and reliability.

---

## Summary in Simple Words

- **Forward proxy** sits in front of clients and protects clients.
- **Reverse proxy** sits in front of servers and protects servers.
- A reverse proxy manages web traffic, prevents server overload, provides faster access, and protects against attacks.

---