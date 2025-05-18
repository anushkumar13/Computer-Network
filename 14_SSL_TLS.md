# What is SSL/TLS?

**SSL (Secure Sockets Layer)** and **TLS (Transport Layer Security)** are cryptographic protocols that secure communication over the internet. When you send or receive sensitive data online (like credit card details), SSL/TLS encrypts this data to protect it.

---

## How Does SSL/TLS Work?

SSL/TLS uses certificates to create an encrypted link between the server and the client. This link ensures that data is transferred securely without anyone in between being able to read it.

This process is called the **SSL/TLS handshake**, which involves several steps:

1. The client (like your browser) requests access to a protected resource on the server (e.g., a login page).
2. The server sends its SSL certificate, which contains its public key.
3. The client verifies if the certificate is valid and trusted to confirm the server’s authenticity.
4. The client generates a symmetric session key and encrypts it using the server’s public key, then sends it to the server.
5. The server decrypts the session key using its private key.
6. Both client and server now use this symmetric session key to encrypt and decrypt all further communication.

This handshake creates a secure encrypted channel between both parties, keeping the data safe.

---

## What is the Role of Keys in SSL/TLS?

Two types of encryption keys are used:

- **Asymmetric Keys:** These are the public and private key pairs. The public key is included in the certificate and is available to everyone, while the private key is kept secret by the server. They are used to establish the encrypted session securely.

- **Symmetric Session Keys:** These are temporary keys generated for each connection. They are used to encrypt and decrypt data because symmetric encryption is faster.

---

## Common Use of SSL/TLS

The most common use of SSL/TLS is **HTTPS**, which secures website traffic. When a website runs on HTTPS, it uses SSL/TLS to encrypt the data between your browser and the server.

You can see a padlock icon in the browser and the URL starting with "https://", indicating the connection is secure.

---

## How to Obtain an SSL Certificate?

To secure your website, you need to get an SSL/TLS certificate from a trusted **Certificate Authority (CA)**. The process is:

1. Generate a **CSR (Certificate Signing Request)** on the server, which contains your public key and domain information.
2. Send the CSR to the CA, which verifies your identity.
3. After verification, the CA issues the certificate.
4. Install the certificate on your server to enable HTTPS on your website.

---

## Summary

SSL/TLS secures internet communication by encrypting data exchanged between client and server. It uses asymmetric keys to exchange symmetric session keys, which then encrypt and decrypt the data. HTTPS is the most common form of SSL/TLS, making web browsing safe. Getting a trusted certificate from a CA is crucial to ensure users know the website is authentic and data is protected.

---

