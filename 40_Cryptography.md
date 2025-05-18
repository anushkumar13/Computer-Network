## What is Cryptography?

**Cryptography** is both a science and an art that involves securing messages or data so that only authorized individuals can understand them, while unauthorized people cannot access or read the information. This process includes two main actions: **encryption** (transforming data into a code) and **decryption** (converting the coded data back to its original message).

---

## What is the Main Purpose of Cryptography?

- **Confidentiality of Data**: Ensuring that data being sent is hidden from unauthorized parties.
  
- **Integrity of Data**: Making sure that the data remains unchanged during transmission, without any modifications.

- **Authentication**: Confirming the identity of the person sending the data, ensuring that the data comes from the claimed source.

- **Non-repudiation**: Preventing the sender from later denying that they sent the message, and ensuring the receiver cannot deny receiving it.

---

## How Does Cryptography Work?

Cryptography relies on two main processes:

1. **Encryption**: This process converts data into a code that cannot be understood without the correct key. This transformed data is called **ciphertext**.

2. **Decryption**: This process takes the **ciphertext** and converts it back into the original message (**plaintext**) that can be understood.

Both processes require special **algorithms** and **keys**.

---

## Types of Cryptography

1. **Symmetric Key Cryptography**: The same key is used for both encryption and decryption.

2. **Asymmetric Key Cryptography**: This involves two different keys:
   - **Public Key**: Available to everyone and used to encrypt data.
   - **Private Key**: Kept secret by the owner and used to decrypt data.

---

## Why is Cryptography Important?

In today's digital age, when we share personal data, banking details, emails, and other sensitive information over the internet, cryptography ensures that:

- Data remains **secure**.
- **Hackers** or attackers cannot steal or misuse the data.
- Communication remains **confidential** and **trustworthy**.
- **Online transactions** are kept secure.

---

## Summary

Cryptography is essentially a method by which we keep our information **safe**, **private**, and **authentic** so that only authorized people can access it. Without cryptography, the concepts of privacy and security in the digital world would not be possible.

---

## What Does "Crypt" Mean?

The word **"crypt"** comes from the Greek language, meaning **"hidden"** or **"secret"**. This term is related to things that are kept hidden or secret.

---

## 1. What is Cryptography?

**Cryptography** means **"secret writing"**. It is the practice of writing or converting messages in a way that only authorized individuals can understand them.

Cryptography is a technique used to secure data so that it cannot be stolen, altered, or accessed by unauthorized parties. It ensures that the information reaches only the intended recipient.

---

## 2. What is Cryptology?

**Cryptology** means **"knowledge of secrecy"**, or the science or theory of understanding secret information.

While **cryptography** focuses on the practical aspect of writing secret messages, **cryptology** is the theory, concepts, and research behind it.

However, in everyday usage, people often use **cryptography** and **cryptology** interchangeably, treating them as one concept.

---

## 3. What is Encryption?

**Encryption** means **"making secret"**, or converting a message into a form that cannot be understood without proper permission.

Plaintext (the original readable message) is converted into ciphertext (an unreadable encrypted message) using an algorithm.

Encryption is an important part of cryptography, but cryptography as a whole involves more than just encryption — it also includes digital signatures, hashing, and more.

---

## How Does Encryption Work?

Encryption involves two key components:

1. **Algorithm**: This is the method or formula used to encrypt the message.

2. **Key**: This is a secret piece of information, usually a number, that tells the algorithm how to apply the encryption to the message.

The **key** controls the algorithm to ensure that the message is securely encrypted.

---

## Key Point

Even if an attacker knows the encryption algorithm, they cannot decrypt the encrypted message without the **key**. Therefore, keeping the key secret is **extremely important**.

---

## Summary

- **Cryptography**: The practical method of writing secret messages.
- **Cryptology**: The theory and knowledge behind secret messages.
- **Encryption**: The process of converting a message into a secret form.

Encryption is a crucial part of cryptography, but cryptography itself is a much broader field that includes many other aspects like digital signatures and hashing.

---

## Principles of Cryptography

The main objective of **cryptography** is to secure data, meaning to hide information in such a way that only authorized individuals can understand it. There are several basic principles upon which the entire system relies. These principles ensure that communication remains **safe**, **private**, and **trustworthy**.

---

### 1. **Confidentiality**

Confidentiality means that data is only visible to authorized individuals.

**Unauthorized individuals**, such as hackers or attackers, should not be able to read the data.

**Encryption** works on this principle — it encodes data in such a way that without a key, it becomes difficult to understand.

**Example:** When you log in to an online banking system, your password and transactions are encrypted so that no one else can read them.

---

### 2. **Integrity**

Integrity means that no unauthorized changes or tampering should occur with the data.

It ensures that the data remains exactly the same when it travels from the sender to the receiver, without any alteration.

If any changes happen to the data, the receiver should be able to detect it.

**Hash functions** and **message digests** are used to ensure integrity.

**Example:** If you digitally sign a document, and someone later alters it, the digital signature will fail, indicating that the document has been tampered with.

---

### 3. **Authentication**

Authentication means verifying identity.

It confirms that the person or system you are communicating with is indeed who they claim to be.

**Digital certificates**, **passwords**, and **digital signatures** are examples of authentication methods.

**Example:** When you log in to your email, the system verifies that you are the legitimate user.

---

### 4. **Non-repudiation**

Non-repudiation ensures that neither the sender nor the receiver can later deny having sent or received a message.

It means that the sender cannot deny sending the message, and the receiver cannot deny receiving it.

This principle is critical for legal transactions and contracts.

**Digital signatures** are an essential tool for ensuring non-repudiation.

**Example:** If you digitally sign an online contract, you cannot later claim that you did not sign it.

---

### 5. **Access Control**

Access control ensures that only authorized users can access a system or data.

Without access control, confidential data could fall into the hands of unauthorized individuals.

This principle is enforced through methods like **passwords**, **biometric systems**, and **role-based access control**.

---

### 6. **Key Management**

In cryptography, keys play a crucial role in encryption and decryption.

**Key management** involves securely generating, storing, distributing, and revoking keys.

If keys are compromised, the entire system becomes insecure.

Therefore, protecting keys is essential for the security of the cryptographic system.

---

### 7. **Availability**

Availability ensures that authorized users can access data or systems whenever they need to.

It means that data or services should not be down or inaccessible due to attacks (such as DoS attacks).

Without availability, security loses its meaning.

---

## Summary

These **cryptographic principles** together ensure that data remains **safe**, **trusted**, and only accessible by the correct individuals:

- **Confidentiality**: Keeps data hidden.
- **Integrity**: Ensures the data remains exactly as it was sent.
- **Authentication**: Verifies the identity.
- **Non-repudiation**: Prevents denial by sender and receiver.
- **Access Control**: Allows only authorized users to access.
- **Key Management**: Secures the keys.
- **Availability**: Ensures data and services are always available.

---

## Cryptography Examples and Techniques

Cryptography involves various techniques and algorithms used to secure data. These techniques are primarily divided into three categories:

- **Encryption Algorithms**
- **Hash Functions**
- **Digital Signatures**

Let’s dive into each of them in detail.

---

### 1. **Encryption Algorithms**

Encryption algorithms are responsible for converting plaintext (readable data) into ciphertext (unreadable data) to ensure that unauthorized individuals cannot understand the information.

There are two main types of encryption techniques:

- **Symmetric Key Encryption**: Uses the same key for both encryption and decryption.
- **Asymmetric Key Encryption**: Uses a public and a private key pair for encryption and decryption.

**Examples of Encryption Algorithms:**

- **AES (Advanced Encryption Standard)**: This is a symmetric key algorithm considered highly secure and fast. It is widely used in modern applications.
  
- **DES (Data Encryption Standard)**: An older symmetric encryption algorithm that is no longer considered secure because of its small key size.
  
- **RSA (Rivest–Shamir–Adleman)**: An asymmetric key algorithm in which data is encrypted using the public key and decrypted with the private key. RSA is essential for secure internet communications.
  
- **ECC (Elliptic Curve Cryptography)**: Another asymmetric key technique that provides strong security with shorter keys compared to RSA.

---

### 2. **Hash Functions**

Hash functions take a message or data and convert it into a fixed-size unique string, known as a hash value or message digest. The main goal of hash functions is to verify the integrity of data, meaning they check if the data has been altered in any way.

**Examples of Hash Functions:**

- **MD5**: An older hash algorithm that is fast but not secure enough for modern use.
  
- **SHA-1**: A better version of MD5, but still has some vulnerabilities and is no longer considered highly secure.
  
- **SHA-256**: The most secure hash algorithm today. It is widely used, including in cryptocurrency technologies like Bitcoin.

---

### 3. **Digital Signatures**

Digital signatures are used to verify the authenticity and integrity of a message. In this process, the sender encrypts the message hash with their private key, creating a digital signature. The receiver can then verify the signature using the sender’s public key, ensuring that the message was sent by the rightful sender and hasn’t been tampered with.

**Digital Signature Process:**

1. The **sender** creates a hash of the message (message digest).
2. The **sender** encrypts the hash using their **private key** to generate the digital signature.
3. The **sender** sends the message along with the digital signature to the **receiver**.
4. The **receiver** uses the **sender’s public key** to decrypt the digital signature and retrieve the hash.
5. The **receiver** then applies the same hash function to the message and compares the result with the decrypted hash. If both hashes match, the message is authentic and unchanged.

---

## Techniques Summary:

- **Symmetric Encryption**: Uses the same key for encryption and decryption. It's fast but comes with risks if the key is compromised.
  
- **Asymmetric Encryption**: Uses a public key for encryption and a private key for decryption. It’s more secure but slower than symmetric encryption.
  
- **Hashing**: Converts data into a fixed-size unique string for data integrity verification.
  
- **Digital Signature**: Ensures message authenticity and non-repudiation by confirming the sender’s identity and preventing denial of message transmission.

---

## Real-life Examples of Cryptography Use:

- **HTTPS Websites**: Websites that start with "https://" use SSL/TLS encryption. This involves both asymmetric and symmetric encryption to secure the communication between the user and the website.
  
- **Email Encryption**: Email services like ProtonMail use asymmetric encryption to send secure messages.
  
- **Messaging Apps**: Apps like WhatsApp and Signal use end-to-end encryption, ensuring that messages remain encrypted while being transmitted between the sender and receiver.
  
- **Digital Payments**: Online payment systems use cryptography to ensure secure transactions, protecting users’ financial information during the payment process.

---

# The Difference Between Encryption, Hashing, and Salting

In the world of cybersecurity, three terms are often used: **encryption**, **hashing**, and **salting**. While they may sound similar, they each serve a different purpose and are used in different scenarios.

Let’s break down the differences in a clear and structured way.

---

## What is Encryption?

**Encryption** is the process of converting readable data (plaintext) into an unreadable format (ciphertext) using a specific algorithm and a **key**. The purpose of encryption is to protect the confidentiality of data by making it unreadable to unauthorized users.

- **Reversible**: Encrypted data can be converted back to its original form using the correct key (decryption).
- **Key-based**: Encryption uses either symmetric (same key) or asymmetric (public/private key pair) cryptographic algorithms.
- **Use case**: Protecting data during transmission (e.g., HTTPS), file storage, email communication, etc.

**Example**:
A message like `Hello123` is encrypted using a key and becomes something like `Xj93#x1!`. Only someone with the correct key can decrypt it.

---

## What is Hashing?

**Hashing** is the process of converting input data into a fixed-size string of characters, which is typically a hash value. Hashing is used to **verify data integrity** and **secure password storage**.

- **Irreversible**: Once data is hashed, it cannot be converted back to its original form.
- **Fixed output size**: No matter how large the input is, the hash output is of a fixed size.
- **Unique output**: Even a tiny change in input data results in a completely different hash.
- **Use case**: Verifying the integrity of data, storing passwords securely in databases.

**Example**:
The password `mypassword` might be hashed to:
`5f4dcc3b5aa765d61d8327deb882cf99`  
This string is stored in the database instead of the actual password.

---

## What is Salting?

**Salting** is an additional layer of security added to hashing. It involves adding a **random string (called a "salt")** to the input (e.g., a password) before hashing.

- **Purpose**: To make hashes unique even if two users have the same password.
- **Defense against attacks**: Helps protect against dictionary attacks and rainbow table attacks.
- **Unique salt per user**: Each user gets a different salt value, so the same password will result in different hashes.

**Example**:
Password = `mypassword`  
Salt = `x1y2z3`  
Hash of `mypasswordx1y2z3` = `6fa9344bd85bb761...`  
Even if someone else has `mypassword`, their salt will be different, so their hash will also be different.

---

## Summary Table

| Feature        | Encryption                         | Hashing                              | Salting                         |
|----------------|-------------------------------------|---------------------------------------|---------------------------------|
| Purpose        | Protect confidentiality of data     | Ensure data integrity and uniqueness  | Strengthen hashed data          |
| Reversible     | Yes (with key)                      | No                                    | No                              |
| Key Required   | Yes                                 | No                                    | No                              |
| Output Length  | Variable or fixed (depends on algo) | Fixed (depends on hash function)      | Fixed (but result changes)      |
| Use Cases      | Secure transmission, storage        | Password storage, data integrity      | Secure password hashing         |

---

## Real-Life Analogy

- **Encryption** is like locking your message in a box with a key. The recipient uses the same (or matching) key to unlock it.
- **Hashing** is like turning your message into a unique fingerprint. You can't turn the fingerprint back into the message.
- **Salting** is like mixing a secret ingredient into your fingerprint before it's created, so even identical messages look completely different.

---

## Final Thoughts

- **Encryption** is best used when you want to retrieve the original data later.
- **Hashing** is used when you need a secure, unique representation of the data that never needs to be decrypted.
- **Salting** is a method to add randomness to the hashing process to protect against certain types of cyber attacks.

Understanding these three concepts is critical for implementing secure systems and protecting sensitive information in the digital world.

---