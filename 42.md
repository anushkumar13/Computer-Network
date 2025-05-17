# Cryptographic Algorithms Overview

### 1. **AES (Advanced Encryption Standard)**

AES is a **symmetric key encryption algorithm**, meaning the same key is used for both encryption and decryption. It is the most widely used modern encryption standard, adopted by the **US National Institute of Standards and Technology (NIST)** in 2001.

- **Block size**: 128 bits, meaning data is encrypted/decrypted in 128-bit blocks.
- **Key sizes**: AES supports three key sizes: 128 bits, 192 bits, and 256 bits. These are commonly referred to as AES-128, AES-192, and AES-256.
- **Efficiency and Security**: AES is known for being fast, secure, and efficient, which is why it is used in a wide range of applications such as mobile apps, banking systems, VPNs, Wi-Fi security, and more.
- **Symmetric encryption**: Since AES is a symmetric algorithm, both parties must securely share the encryption key. If the key is compromised, the security of the system is at risk.

### 2. **DES (Data Encryption Standard)**

DES is also a **symmetric key encryption algorithm**, and it was widely used in the past.

- **Block size**: 64 bits.
- **Key size**: 56 bits.
- **History**: DES became a standard in 1977. However, it is now considered weak due to the fact that modern computers can easily perform brute-force attacks on its 56-bit key.
- **Current use**: DES is almost obsolete today, with **3DES (Triple DES)** being an improved version that encrypts data three times with DES. However, even 3DES is now considered outdated and less secure.
- **Security**: DES is no longer sufficient for securing modern systems due to its vulnerability to attacks.

### 3. **RSA (Rivest-Shamir-Adleman)**

RSA is an **asymmetric key encryption algorithm**, meaning it uses different keys for encryption and decryption — a **public key** (which can be shared with anyone) and a **private key** (which is kept secret).

- **Key exchange**: RSA is mainly used for secure key exchange rather than directly encrypting large amounts of data.
- **Mathematics**: The algorithm relies on the difficulty of factorizing large prime numbers. The security of RSA depends on the size of the key, with common sizes being 2048-bit or 4096-bit keys.
- **Applications**: RSA is widely used in **digital signatures**, **secure email**, **SSL/TLS** (web security), and **public key infrastructure (PKI)**.
- **Security**: RSA's strength is directly related to the key size; larger key sizes provide greater security.

### 4. **MD5 Hashing (Message-Digest Algorithm 5)**

MD5 is a **hash function** that converts input data into a fixed-size 128-bit hash value (also called a digest).

- **Output**: The result of the MD5 algorithm is a 32-character hexadecimal number.
- **Usage**: MD5 is used to check data integrity, ensuring that the data hasn't been altered during transmission or storage.
- **Weakness**: Although MD5 was widely used in the past, it is now considered weak due to its vulnerability to **collision attacks**. A collision occurs when two different inputs produce the same hash value, undermining the algorithm's integrity.
- **Current use**: Modern systems have moved away from MD5 in favor of stronger hashing algorithms like **SHA-2**.

## Summary

- **AES**: A fast, secure symmetric encryption algorithm with a 128-bit block and key sizes of 128, 192, or 256 bits.
- **DES**: An older symmetric encryption algorithm with a 64-bit block and a 56-bit key; now considered weak.
- **RSA**: An asymmetric encryption algorithm using public and private keys, based on prime factorization, commonly used for secure key exchange.
- **MD5**: A hashing algorithm that produces a fixed 128-bit hash used for data integrity; now considered weak and replaced by stronger hashing algorithms like SHA-2.

---
