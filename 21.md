# What is REST?

**REST** stands for **Representational State Transfer**. It was first described by **Roy Fielding** in his famous research paper. In that paper, he presented his idea of an ideal software architecture designed specifically for the World Wide Web.

REST is not a strict standard or an official rulebook; rather, it is an **architecture style**. This means it is a design approach used for **distributed hypermedia systems** — systems built for large, interconnected environments like the internet.

Roy Fielding explained that if we build our systems following the **RESTful architecture style**, they will be perfect for large networks such as the internet. This is because RESTful systems have specific features that make them **scalable**, **flexible**, and **efficient**.

### In simple terms:
REST is a concept that guides how to design web systems so they can grow big and complex while still communicating easily. It doesn’t enforce hard rules but acts more like a **best practice** for designing modern web architectures.

---

# Core Concept of RESTful Systems: Resources

The main concept behind **RESTful systems** is **resources**. These resources are the entities or things managed within the system. They can be anything, such as a web page, a video stream, or an image. Resources can also be abstract, like a list of all users in a database or a weather forecast for a specific location.

### Key Points About Resources in REST:

- **Uniquely Identifiable:**  
  Every resource in the system must be uniquely identifiable. This means each resource has its own unique address or ID, allowing it to be clearly recognized and accessed.

- **Multiple Representations:**  
  A resource can have multiple representations. This means the same resource can be presented in different formats, such as HTML, JSON, or XML. For example, a web page resource can be viewed as HTML or retrieved as JSON data.

### Client-Server Model in REST:

REST uses a **client-server architecture** where:

- The **server** manages the state of the resource, i.e., it controls the current status or data of the resource.
- The **client** has the choice to select which representation (format) of the resource it wants to use or interact with.

### Summary:

In REST, resources are uniquely identifiable and can exist in multiple formats (representations). The server maintains the resource’s state, while the client chooses the preferred representation to interact with the resource.

---

# Uniform Interface: A Key Feature of RESTful Systems

One important feature of **RESTful systems** is the **Uniform Interface**. This means that clients must use a standard set of operations to access every resource.

No matter which resource you are accessing — whether it’s user data or product information — you always use the same set of operations, which are the standard HTTP methods: **GET**, **POST**, **PUT**, and **DELETE**.

### Benefits of Uniform Interface:

- **Simplicity and Flexibility:**  
  Because of this uniformity, the implementation becomes simple and flexible. Server-side developers can evolve or change their services without affecting clients, meaning they can make changes without worrying about breaking the client’s usage.

### Drawbacks of Uniform Interface:

- **Possible Restrictions:**  
  Sometimes, this uniform interface can impose unnecessary restrictions on certain systems.  
- **Performance Overhead:**  
  The server may take more time or resources to perform some tasks because it uses only standardized operations instead of specialized ones tailored for specific needs.

### Summary:

The uniform interface in REST means that all resources are accessed through the same standardized operations, making development easier and the system more flexible. However, this can sometimes cause slower performance or impose restrictions due to its generalized nature.

---

# Statelessness in RESTful Systems

In a **RESTful system**, being **stateless** is very important. This means that every operation or request a client sends to the server is **self-contained** and complete on its own. The server should **not depend on any previous request** or any shared state (i.e., information stored between the client and server).

### What does this mean?

Whenever a client sends a request to the server, that request must include **all the information** the server needs to process it. The server does **not need to remember** any previous requests or maintain any session data.

---

### Benefits of Statelessness:

- **Visibility:**  
  Each request can be individually inspected and analyzed, making it easier to monitor system health and response times.

- **Reliability:**  
  If a failure occurs, recovery is easier because the server does not store any previous state or data.

- **Scalability:**  
  When the number of requests increases, new servers can be added easily since they don’t need to share any prior state.

---

### Trade-offs:

Since every request is self-contained, requests may become larger and often include **repeated data**, especially when the client interacts with the server multiple times.

---

### Summary:

Statelessness in REST means every request is independent. This design makes the system more reliable, scalable, and easier to monitor, but sometimes it causes requests to be bigger and more repetitive.

---

# Understanding HTTP and Its Relationship with REST

**HTTP** stands for **HyperText Transfer Protocol**, which is a standard protocol with well-defined rules and constraints. HTTP is the communication protocol that powers our everyday interactions on the internet, such as:

- Loading a webpage in a web browser  
- Streaming a video  
- Controlling smart devices like home lights via a mobile app  

---

### Are REST and HTTP the Same?

The short answer is **No**.

- **HTTP** is a **protocol** maintained by the Internet Engineering Task Force (IETF).  
- **REST** is an **architectural style** or design approach.  

Interestingly, Roy Fielding, who defined REST, also contributed to writing the HTTP RFCs (Request for Comments).

---

### Important Point:

A **RESTful system does not necessarily require HTTP**, but HTTP follows many of REST’s principles, making it a good foundation for building RESTful systems.

---

### HTTP Features that Align with REST Principles

HTTP includes features such as:

- Standard methods like GET, POST, PUT, DELETE which correspond to resource operations in REST  
- Stateless communication where each request is independent  
- Use of URIs to uniquely identify resources  
- Support for multiple representations of resources (like HTML, JSON, XML)  

Because of these features, HTTP closely matches many REST principles and is widely used to implement RESTful APIs.

---

# Resources in the World of HTTP

In the HTTP world, **resources** are often files located on a remote server, such as HTML, CSS, JavaScript, images, and all the other files that make up modern web pages. Each file is considered a separate resource with its own unique URL that can be addressed.

---

### Resources Are More Than Just Files

HTTP resources are not limited to files alone. A resource can be **any kind of data** stored on a remote server, such as:

- Customer details  
- Product information  
- Configuration settings  
- And much more  

Because of this flexibility, HTTP has become extremely popular for building modern APIs. It provides a **consistent and predictable way** to access and manipulate remote data.

---

### Multiple Representations of Resources

One of the key features of HTTP is that it allows clients to choose different **representations** of a resource. This is achieved through HTTP headers and **media types**.

- **Media types** are standard formats that specify how data is represented, such as HTML, JSON, XML, etc.

For example, a weather website might provide the same weather forecast resource in two different formats:

- An **HTML** format that is easy to view in a web browser  
- A **JSON** format that is more useful for another system that stores historical weather data  

---

### Summary

HTTP uniquely identifies resources, presents them in multiple formats, and gives clients the flexibility to choose the representation they need according to their use case.

---

# HTTP and REST Principles: Standard Methods

HTTP follows REST principles, which is why it provides a **uniform set of methods** for every resource. Although HTTP defines about 12 methods, most services primarily use **4 main methods** that correspond closely to CRUD operations:

- **POST**  
- **GET**  
- **PUT**  
- **DELETE**  

---

### Why These 4 Methods?

These four operations are well-known and standardized, making it easier to build client applications that interact with web services. Unlike other protocols such as SOAP, where operations can be customized and unlimited, HTTP keeps the set of operations **minimal and consistent** so that they behave the same way everywhere.

---

### Real-World Usage

Some web services might restrict certain methods for specific resources or require authentication for sensitive data. However, the **HTTP methods themselves are universally known** and do not vary from one website to another.

---

### Summary

Because of this fixed set of HTTP methods, interactions between clients and servers remain **simple, predictable, and standardized**, which helps maintain consistency across different web services.

---

# HTTP and RESTful Principles: Where HTTP Can Break REST Rules

HTTP implements many RESTful principles, but there are ways in which HTTP can **violate** these principles.

---

### 1. Protocol vs Architectural Style

First of all, REST is **not a communication protocol**, whereas HTTP **is a protocol**. This fundamental difference means that HTTP has some constraints that might not always align perfectly with REST.

---

### 2. Violation of Statelessness with Cookies and Sessions

One of the most controversial issues is that modern web servers often use **cookies** and **sessions** to store state information on the server side. When the server relies on these to maintain state between requests, it **violates REST’s statelessness principle**, which requires that each request be independent and not depend on any previous server state.

---

### 3. URLs Breaking Uniform Interface

Sometimes, the way URLs are used (as defined by IETF) can break the **uniform interface principle**. For example, consider this URL: https://www.foo.com/api/v1/customers?id=17&action=clone


Here, the HTTP predefined method (like GET) must be used to make the request, but the query parameter `action=clone` specifies an extra operation that is **not part of the standard HTTP methods**. This operation might not be clearly available for every resource, and it becomes hard to predict what the response will be without knowing the service’s internal details.

---

### Summary

Because of these reasons, HTTP is **not 100% RESTful** in every situation, since it can violate some core REST principles such as statelessness and uniform interface.

---

# Understanding the Difference Between REST and HTTP

Many people often confuse **REST** and **HTTP** as the same thing, but in reality, they are quite different.

---

### What is REST?

REST (Representational State Transfer) is an **architectural style**. It defines a set of constraints and principles that help design software systems in a particular way. REST focuses on how resources are identified, represented, and manipulated in distributed systems.

---

### What is HTTP?

HTTP (HyperText Transfer Protocol) is a **clearly defined communication protocol** used for transferring data over the internet. It is a language or set of rules that governs how messages are formatted and transmitted between clients and servers.

---

### How are REST and HTTP related?

HTTP implements many of REST’s principles, which is why it is often called a **RESTful protocol**. HTTP provides the methods and structure that align well with REST architecture, making it a popular choice for building RESTful systems.

---

### Key Point

- **REST** is a **design style** or approach to building systems.
- **HTTP** is a **protocol** or language used for communication on the web.
- While HTTP follows REST principles to a large extent, **they are not the same thing**.

---
