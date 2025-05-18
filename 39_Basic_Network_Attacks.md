## Digital Signatures and Certificates

**Digital signatures** and **certificates** are two very important technologies that ensure online security and authenticity. These technologies help confirm that online actions are legitimate, secure, and free from fraud or unauthorized activities.

These technologies are crucial in areas such as:

- **Online banking** (when transferring money online)
- **Secure email communication** (when sending confidential emails)
- **Software distribution** (when downloading the genuine version of software without tampering)
- **Electronic document signing** (when signing documents online legally)

These technologies provide **authentication**, **integrity**, and **non-repudiation**.

- **Authentication**: Ensures the data is from the authentic sender.
- **Integrity**: Ensures the data has not been altered.
- **Non-repudiation**: Ensures the sender cannot deny sending the data later.

Thus, digital signatures and certificates protect against fraud, data theft, and unauthorized access.

---

### What is a Digital Signature?

A **digital signature** is a mathematical technique used to validate the **authenticity** and **integrity** of a message, software, or digital document.

In simple terms, when you digitally sign a document or message, you confirm that the document is authentic, unaltered, and exactly as the sender intended it to be.

Let's understand the key features of a digital signature:

---

### 1. **Key Generation Algorithms**

An essential concept behind digital signatures is **key generation**.

A digital signature is a special kind of electronic signature that ensures the message was sent by a specific sender.

When performing digital transactions, two critical aspects are necessary:

- **Authenticity**: Confirming the sender's identity.
- **Integrity**: Ensuring no changes have been made to the data.

If these two aspects are not present, the data could be altered or another person could pretend to be the sender, which is dangerous.

To generate digital signatures, **keys** are created. These keys are mathematically generated and are in two parts:

- **Private Key**: Only the sender possesses this key, and it is kept secret.
- **Public Key**: This key can be available to everyone and is used to verify the signature.

---

### 2. **Signing Algorithms**

Now, let's discuss how a digital signature is created.

A **signing algorithm** is used to sign the data.

The process starts by creating a **hash** of the data or message you want to sign.  
A **hash** is a unique, small code that represents the original data. It is essentially a digital fingerprint of the data.

Next, this hash value is **encrypted** using the **private key**.  
The encrypted hash is what constitutes the **digital signature**.

An important point is that instead of signing the entire data, only the hash is signed. This is more efficient because the hash is much smaller and of fixed size.  
This saves both time and resources.

The digital signature is then attached to the original data and sent to the receiver.

---

### 3. **Signature Verification Algorithms**

When the receiver gets the data along with the digital signature, they need to verify whether the signature is valid or not.

A **verification algorithm** is used for this purpose.

The verification process works as follows:

- The receiver uses the **public key** to decrypt the digital signature and obtain a value.
- Simultaneously, the receiver applies the same hash function to the received data and generates a hash value.

If both hash values match, it means the digital signature is valid, and the data is authentic and unaltered.

If the hashes do not match, the signature is invalid, and it is possible that the data has been tampered with or is fake.

---

### Summary

A **digital signature** is a secure method that:

- Proves the sender's genuine identity (**authentication**)
- Ensures the data remains safe and unaltered (**integrity**)
- Prevents the sender from denying sending the data (**non-repudiation**)

It uses **keys**, **signing algorithms**, and **verification algorithms** to achieve these goals.  
This makes online communications and transactions much more secure.

---

## How Digital Signature Works

The steps to create a **digital signature** are as follows:

### Step 1: Create Message Digest (Apply Hash Function)

The sender first applies a **hash function** on their message.

A **hash function** is a mathematical process that converts the message into a fixed-size smaller code, which is the unique fingerprint of the message.

This small code is called the **message digest**.

In other words, even if the original message is large, the hash function converts it into a smaller, fixed-size number or code.

Then, the sender encrypts this message digest using their **private key**.

The encrypted message digest becomes the **digital signature**.

We can represent it like this:

Digital signature = encryption(private key of sender, message digest)
Message digest = message digest algorithm(message)


This step is crucial because only the sender has their **private key**, which is kept secure.

---

### Step 2: Sender Sends Message and Digital Signature to Receiver

The sender sends both the original message and the digital signature to the receiver.

Thus, the receiver receives two things:

1. The **original message**.
2. The **digital signature** (which is the encrypted message digest).

---

### Step 3: Receiver Decrypts the Digital Signature

The receiver decrypts the **digital signature** using the sender's **public key**.

This works because:

- The digital signature was created using the sender's **private key**.
- Therefore, only the sender's **public key** can decrypt it.

This allows the receiver to confirm that the signature was indeed created by the sender, which proves the **authenticity**.

---

### Step 4: Receiver Now Has the Message Digest

When the receiver decrypts the digital signature, they obtain the **message digest** (the one created by the sender).

---

### Step 5: Receiver Computes Their Own Message Digest

The receiver then applies the same **hash function** to the received **original message**.

This generates the **receiver's own message digest**.

---

### Step 6: Compare Both Message Digests

Now, the receiver has two message digests:

1. The one received after decrypting the digital signature (from the sender).
2. The one the receiver has calculated by applying the hash function to the original message.

If both message digests match, it means:

- The message has not been altered (ensuring **integrity**).
- The message was sent by the **authentic sender** (confirming **authenticity**).

If the digests do not match, it means the message or signature might have been tampered with, or the data is not genuine.

---

### Role of Message Digest and One-way Hash Function

The hash function used to create the **message digest** is a **one-way hash function**.

This means:

- It is easy to generate the **hash** (message digest) from the message.
- However, it is difficult or impossible to reverse the hash value back to the original message.

This makes the hash function secure and ensures the safety of the digital signature.

---

### Summary

Here’s how a **digital signature** works:

1. The sender creates a unique small code (message digest) using a hash function on the message.
2. The sender encrypts the message digest using their **private key**, creating the **digital signature**.
3. The sender sends the original message and digital signature to the receiver.
4. The receiver decrypts the digital signature using the sender’s **public key**, retrieving the message digest.
5. The receiver computes their own message digest from the original message.
6. If both message digests match, the message is considered **authentic** and **safe**.

Thus, digital signatures ensure both **authenticity** and **integrity** of a message.

---

## Digital Signature vs. Electronic Signature

First, let’s understand what both terms mean:

### Electronic Signature (E-signature):

An **electronic signature** is a broad term. It refers to any electronic method used by a person to indicate their agreement or consent on a document or message.

Common examples include:

- Typing your name in an email or document.
- Clicking a button to "I Agree" or "Sign."
- Scanning a handwritten signature and adding it to a digital document.
- Signing with a finger on a touchscreen.

The main purpose of an electronic signature is to provide proof that "I accepted this document or that my signature is on it."

However, the security or authentication level of electronic signatures can vary. This means it is not guaranteed that the signature was made by the actual person or that the message has not been altered.

### Digital Signature:

A **digital signature** is a specific, advanced type of electronic signature.

It uses **cryptography** (mathematical encryption) with the help of **public** and **private keys** to create a digital signature.

A digital signature not only confirms that a document or message has been signed but also ensures that:

- The message or document is authentic and has not been altered (integrity).
- Only the original sender could have created the signature (authenticity).
- The sender cannot deny having signed the document (non-repudiation).

It uses a mathematically encrypted **hash** (message digest), which makes it very secure.

---

### Key Differences

| **Point**               | **Electronic Signature**                               | **Digital Signature**                                       |
|-------------------------|--------------------------------------------------------|------------------------------------------------------------|
| **Definition**           | Any electronic method to show agreement (like typing, clicking, scanning) | A specific cryptographic method using keys to verify authenticity and integrity |
| **Security Level**       | Low to medium, depends on the method used              | High, cryptographically secure                              |
| **Authentication**       | General proof of signing, but not always verified     | Strong verification using public/private key               |
| **Integrity Check**      | Usually not present, meaning the message can be altered | Present, changes in the message are detected               |
| **Use Case**             | Simple agreements, non-sensitive transactions         | Banking, legal documents, software signing                 |
| **Non-repudiation**      | Weak or none                                           | Strong, the signer cannot deny having signed                |

---

### Simple Example:

- **Electronic signature**: You type your name in an online form and submit it. This is a form of electronic signature.
  
- **Digital signature**: When you sign a transaction in your bank's software, it is an encrypted digital signature that confirms the transaction is legitimate and that you signed it.

---

### Summary

An **electronic signature** is an umbrella term covering a simple and wide range of electronic signing methods, but its security level can vary.

A **digital signature** is a strong, secure, cryptography-based electronic signature that ensures **authenticity**, **integrity**, and **non-repudiation**.

---

## What Are the Assurances of Digital Signatures?

When a **digital signature** is used, it provides several important promises or guarantees that make it reliable and secure. These promises are known as **assurances**. These assurances ensure that any document or message signed using a digital signature is trustworthy.

### 1. Authenticity (Guarantee of Authenticity)

This means that the identity of the signer has been verified. It confirms that the signature on the document was actually made by the person whose name appears on it.

**Example:** If you place your digital signature on a bank document, authenticity ensures that the signature is truly yours and was not altered or forged by someone else.

**How is this possible?** Digital signatures are created using a **private key**, which only the signer possesses, and are verified using the **public key**. This makes it very difficult for someone else to sign a document under the signer's name.

---

### 2. Integrity (Protection of Content and No Changes)

When a document is digitally signed, it means that no one can alter the content of the document after it has been signed.

If any changes occur, the digital signature will no longer be valid.

**This means that the digital signature guarantees:**

- The document that was signed remains unchanged.
- The document is original and exactly as the signer intended it to be.

**Example:** If you digitally sign a contract, it will remain exactly the same, without any changes, after the signature is applied.

---

### 3. Non-repudiation (Cannot Deny)

Non-repudiation means that the signer cannot later claim, "I did not sign this" or "This is not my signature."

This is a legal concept that ensures the signer cannot deny their involvement in the signing process.

**Why is this important?** If any dispute arises, non-repudiation provides proof that the signer did, in fact, sign the document and is responsible for it.

---

### 4. Notarization (Legally Certified)

In certain conditions, if a document (such as one created in Microsoft Word, Excel, or PowerPoint) is digitally signed and the signature is time-stamped by a secure time-stamp server, the signature is considered legally **notarized**.

A **time-stamp server** is a trusted server that certifies the exact time the signature was applied.

**Benefit:** This provides not only proof of the document's authenticity but also verification of the time the signature was applied, which is crucial for legal purposes.

---

### Summary

A **digital signature** provides four important assurances:

- **Authenticity**: Confirms the signer’s identity.
- **Integrity**: Guarantees the document has not been altered.
- **Non-repudiation**: Ensures the signer cannot deny their signature.
- **Notarization**: In certain conditions, it is considered legally notarized with a time-stamp.

These assurances make digital signatures highly secure and trustworthy in legal and professional environments.

---

## Benefits of Digital Signatures

### 1. Legal Documents and Contracts
Digital signatures are legally binding. This means that any document or contract signed digitally holds full legal weight.

- The identity of the signer is verified.
- No changes can be made to the document without detection.
- The authenticity of the document is guaranteed.

Therefore, digital signatures are perfect for legal documents where the authenticity of the signature and the security of the document are crucial.

---

### 2. Sales Contracts
Digital signatures are also very useful in sales contracts.

- Both the seller and the buyer’s identities are verified.
- Both parties are assured that the signatures are authentic and legally binding.
- The terms of the agreement cannot be changed without detection.

This makes business transactions more secure and trustworthy.

---

### 3. Financial Documents
Digital signatures are commonly used in the finance department for documents such as invoices.

- Customers are assured that the payment request came from the legitimate seller.
- No attacker or fraudster can use a fraudulent account to send payment requests.
- This helps protect the payer from fraud.

Digital signatures ensure that financial transactions are safe and secure.

---

### 4. Health Data
In the healthcare industry, privacy is extremely important, whether it’s patient records or research data.

Digital signatures ensure that:

- Any confidential information transmitted has not been modified or tampered with.
- Both parties (doctor, patient, researchers) trust the authenticity of the data.
- Patient privacy is protected.

This is why the use of digital signatures in healthcare is increasing.

---

## Drawbacks of Digital Signatures

### 1. Dependency on Technology
Digital signatures are entirely dependent on technology.

- If the system or software is not secure, the chances of hacking or cyber-attacks increase.
- Businesses need to keep their digital signature systems up to date with the latest security patches and upgrades.
- If security is weak, attackers can modify documents or commit fraud.

---

### 2. Complexity
Setting up and using digital signatures can be complex, especially for people who are new to technology.

- Mistakes or errors may occur, which can reduce the system's effectiveness.
- For senior citizens or people less familiar with technology, using digital signatures can be challenging.
- Training and awareness are required to ensure everyone uses the system correctly.

---

### 3. Limited Acceptance
In countries like India, digital signatures are not yet fully widespread.

- It takes time to replace manual signatures with digital ones.
- Technology is not easily available everywhere.
- As a result, the acceptance of digital signatures is limited, particularly in smaller or rural areas.

---

## Summary
The **benefits** of digital signatures include:

- Securing legal and financial documents.
- Verifying identities.
- Maintaining privacy and data integrity.

However, there are also **challenges** such as:

- Dependence on technology and potential security risks.
- Complexity, which may make it difficult for beginners.
- Limited acceptance, especially in developing countries like India.

---

## What is a Digital Certificate?

A **digital certificate** is a digital document issued by a trusted third party, called a **Certificate Authority (CA)**. It proves the identity of the sender to the receiver and the identity of the receiver to the sender. In simple terms, both parties can verify each other’s authenticity.

The main purpose of a digital certificate is to associate a **public key** with a specific individual or entity to enable secure communication.

---

## What is Included in a Digital Certificate?

A digital certificate contains several important pieces of information, such as:

1. **Certificate Holder's Name**: The name of the person or organization who holds the certificate.
2. **Serial Number**: A unique number assigned to each certificate, which uniquely identifies it.
3. **Expiration Dates**: The validity period of the certificate. After this period, the certificate expires and needs to be renewed.
4. **Public Key**: The public key used to decrypt messages or verify digital signatures.
5. **Digital Signature of the Certificate Authority (CA)**: The CA's digital signature certifies that the certificate is valid and that the certificate holder's identity is authentic.

---

## How is a Digital Certificate Used?

When a message or digital signature is sent, the sender also sends their digital certificate along with the message. The receiver can then verify whether the message or signature is authentic, as the CA has verified the sender’s identity and issued the certificate.

---

## Advantages of Digital Certificates

### 1. Network Security
In modern cybersecurity systems, multiple layers are used to protect systems from attackers. Digital certificates provide an essential layer of security, protecting networks from man-in-the-middle attacks and hacking attempts. This reduces the risk of data manipulation or interception.

### 2. Verification
Digital certificates enhance authentication. When access to sensitive data is required, certificate-based authentication ensures that only authorized individuals can access it. This method is more flexible and reliable than other methods such as biometrics or OTPs.

### 3. Buyer Trust
When visiting a website, users need to ensure that the site is trustworthy. Digital certificates issued by trusted Certificate Authorities (CAs) are recognized by user browsers. This acts as a strong indicator that the website is authentic and safe to interact with.

---

## Disadvantages of Digital Certificates

### 1. Phishing Attacks
Attackers can create fake websites and obtain digital certificates for them, making them appear as legitimate sites. As a result, users may unknowingly provide sensitive information (like login credentials) to these fraudulent sites, which attackers can misuse.

### 2. Weak Encryption
Some older digital certificate systems use weak encryption methods that hackers can easily break or intercept data. This reduces the security level of such certificates.

### 3. Misconfiguration
If digital certificates are not correctly configured, they may not function properly. Incorrect setup can make websites vulnerable to attacks, leaving them open to exploitation by hackers.

---

## Summary
A **digital certificate** is issued by a trusted third party (CA) and is used to verify the identity of both the sender and the receiver.

It contains the certificate holder's name, a unique serial number, expiration date, public key, and the CA’s digital signature.

Digital certificates improve network security, strengthen authentication, and provide trust to users.

However, challenges like phishing attacks, weak encryption, and misconfiguration exist.

---

## Digital Certificate vs Digital Signature

### 1. **Definition**
- **Digital Certificate**: 
A **digital certificate** is an electronic document issued by a trusted third party, called a **Certificate Authority (CA)**. Its role is to verify the identity of an individual, organization, or device and link its public key to the name. Essentially, it confirms that the public key truly belongs to the specific entity or individual.

- **Digital Signature**: 
A **digital signature** is a cryptographic technique that verifies the authenticity (genuineness) and integrity (no alterations) of a message or document. When a sender signs a message with their private key, the receiver can verify the digital signature using the sender's public key.

---

### 2. **Purpose**
- **Digital Certificate**: 
The main purpose of a **digital certificate** is to verify identity and certify a public key. It guarantees that the public key you are using truly belongs to the intended individual or entity, not to an attacker.

- **Digital Signature**: 
The main purpose of a **digital signature** is to ensure the authenticity (that the message was sent by the genuine sender) and integrity (that the message has not been altered) of a message or document.

---

### 3. **Issuer**
- **Digital Certificate**: 
A **digital certificate** is issued by a trusted third party known as the **Certificate Authority (CA)**, which is globally recognized.

- **Digital Signature**: 
A **digital signature** is created by the sender using their private key. It does not require any third party.

---

### 4. **Use Case**
- **Digital Certificate**: 
Digital certificates are mainly used in secure communication channels, such as **HTTPS websites**, **VPNs**, **email encryption**, where verifying the public key is essential. Without it, verifying a digital signature becomes difficult because the receiver needs to receive the sender's public key in a trusted manner.

- **Digital Signature**: 
Digital signatures are used for **document signing**, **email verification**, **legal contracts**, **software distribution**, and anywhere the authenticity and integrity of a message are important.

---

### 5. **Components**
- **Digital Certificate**: 
A **digital certificate** contains:
  - Sender's name
  - Serial number
  - Expiration date
  - Public key
  - CA's digital signature

- **Digital Signature**: 
A **digital signature** contains:
  - A message digest (created by a hash function)
  - The digest encrypted with the sender’s private key.

---

### 6. **Verification Process**
- **Digital Certificate**: 
The receiver verifies the **digital certificate** by checking the CA's public key to ensure the certificate is valid. If valid, the receiver trusts the public key of the sender.

- **Digital Signature**: 
The receiver decrypts the **digital signature** using the sender's public key and compares it with the original message digest. If they match, the message is considered authentic and unaltered.

---

### 7. **Security Aspect**
- **Digital Certificate**: 
A **digital certificate** acts as a trust mechanism, indicating that the public key is legitimate. If the certificate is from a trusted CA, the public key is trusted.

- **Digital Signature**: 
A **digital signature** proves that the message was sent by the signer (non-repudiation) and ensures that the message hasn't been tampered with.

---

### **Summary in Simple Words**
- **Digital Certificate**: Think of it as a **digital ID card** that tells you whose public key you are using, and it's issued by a trusted authority like a CA.

- **Digital Signature**: Think of it as a **digital sign** that the sender places using their private key so that the receiver can confirm the message is authentic and hasn't been altered.

---

## What is Encryption?

**Encryption** is a process where we transform our original electronic data into a form called **ciphertext**. This ciphertext is unreadable without proper authorization. In other words, encryption converts data in such a way that if an unauthorized person or hacker sees it, they won’t be able to understand what the original message is.

The main purpose of encryption is to provide **data security**, ensuring that sensitive information such as usernames, passwords, bank details, or any confidential message remains protected and is not accessed by unauthorized individuals.

---

## What is Decryption?

**Decryption** is the reverse process of encryption. In this process, ciphertext is converted back to its original data form. This means that when the sender sends an encrypted message, the receiver can decrypt it to retrieve the original readable message.

This process ensures that only the authorized receiver can understand the message, and if the message is intercepted during transmission, it cannot be read by unauthorized individuals.

---

## How Do Encryption and Decryption Work?

When a sender wants to send a message that needs to be secured, they encrypt the message using an encryption algorithm. The job of this algorithm is to convert the data into a form that is difficult to understand.

When this encrypted message reaches the receiver, they use a decryption algorithm to decrypt the ciphertext and retrieve the original message.

---

### Example:

Imagine you are sending your password over the internet. If you send the password directly, any hacker who intercepts the data can read your password.

To prevent this, you encrypt your password. After encryption, the password becomes ciphertext, which appears as an unreadable and strange form. Even if a hacker intercepts it, they won't be able to read it.

When the receiver gets the message (ciphertext), they can decrypt it and retrieve the original password.

---

## Summary:

**Encryption** and **decryption** together secure data. Encryption transforms data into a secure form, while decryption brings it back to a readable form. This ensures that the data only reaches authorized individuals, maintaining its security.

---

## What is Encryption?

**Encryption** is a process where we convert our original information (called **plaintext**) into a code that only authorized people can understand. This code is known as **ciphertext**.

In other words, when data is encrypted, it is transformed into a form that is difficult or impossible to understand without a secret password or key.

---

## Plaintext and Ciphertext

- **Plaintext**: This is the original data, such as your actual message, password, or document. It is the data that we can normally read.
  
- **Ciphertext**: When plaintext is encrypted, it turns into ciphertext. Ciphertext is strange, unreadable data that cannot be understood without the secret key or password.

---

## Main Purpose of Encryption

In today's business and online world, **data security** is becoming increasingly important. A lot of sensitive information is shared, such as bank details, personal information, contracts, etc.

Encryption is a very popular and effective method to protect data. It transforms data in such a way that only authorized individuals can understand it. For everyone else, it appears as meaningless code.

---

## How Does Encryption Work?

In encryption, a special **decryption key** is created, which is either generated during the encryption process or beforehand. This key or password is used when encrypting the data.

The resulting ciphertext can only be transformed back into plaintext using the same secret key or password.

---

## Summary:

- **Encryption** means converting your original data (**plaintext**) into an encrypted form (**ciphertext**).
  
- Ciphertext cannot be understood without the secret key.

- Encryption ensures the **secrecy** and **confidentiality** of data.

- In the business world, encryption has become an essential part of **data security**.

---

## What is Symmetric Encryption?

**Symmetric Encryption** is a process in which the same key is used for both **encrypting** (locking) and **decrypting** (unlocking) the message. In other words, both the sender and receiver share the same **secret key** that is used to secure the message and read it back.

---

## How Symmetric Encryption Works?

When the sender wants to send a message, they use their **secret key** to encrypt the message. This means the message is transformed into a code that cannot be understood without the key.

When the receiver gets the encrypted message, they use the same secret key to **decrypt** it and retrieve the original message.

---

## Key Points of Symmetric Encryption:

- The same key is used for both **encryption** and **decryption**.
- If someone else gets hold of the key, they can read the message. Hence, keeping the key secure is very important.
- This method is **fast**, making it suitable for encrypting large amounts of data.
- The challenge is securely sending the key from the sender to the receiver.

---

## What is Asymmetric Encryption?

**Asymmetric Encryption** (also known as **public-key cryptography**) uses two different keys:

- **Public Key**: This key is available to everyone and can be freely shared.
- **Private Key**: This key is kept secret by one person and is never shared.

---

## How Asymmetric Encryption Works?

When the sender wants to send a message, they use the **receiver’s public key** to encrypt it. This means the message is secured using the public key.

When the receiver gets the encrypted message, they use their **private key** to decrypt it and retrieve the original message.

---

## Key Points of Asymmetric Encryption:

- There are two keys: **public key** (shared with everyone) and **private key** (kept secret by the owner).
- Only the **private key** can decrypt a message that was encrypted using the **public key**.
- Sharing the **public key** is safe because, without the **private key**, no one can read the encrypted message.
- This method is a bit **slower** than symmetric encryption, so it is typically used for encrypting smaller amounts of data or keys.
- It is **very secure** and is widely used for **online transactions** and **digital signatures**.

---

## Summary:

- **Symmetric Encryption**: Uses the same key for both encrypting and decrypting. It is fast but has the challenge of securely sharing the key.
  
- **Asymmetric Encryption**: Uses two keys — one public and one private. The public key encrypts the message, and the private key decrypts it. It’s secure and solves the key sharing problem, but it is slower.

---

## 1. What is Public Key?

A **public key** is a key that is openly available to everyone. It can be shared widely so that others can use it to send secure messages to the person it belongs to. 

For example, if person A’s public key is `7`, this information can be known to everyone. The purpose of the public key is to allow others to send encrypted messages to the person who owns it.

---

## 2. What is Private Key?

A **private key** is a key that only the person who owns it has access to. It is kept completely secret and should never be shared with anyone. 

The private key is used to **decrypt** messages that have been encrypted using the corresponding **public key**. The protection of the private key is extremely important for maintaining security.

---

## 3. What is Authentication?

**Authentication** is the process by which a system verifies that the user attempting to log in or gain access is indeed who they claim to be. 

In simple terms, authentication ensures the **identity** of the user is correct. Common methods of authentication include:
- Checking a **username and password**.
- **Biometric scans** (like fingerprints or facial recognition).
- Verifying **digital certificates**.

---

## 4. What is Non-repudiation?

**Non-repudiation** ensures that neither the sender nor the receiver can deny their actions in a communication process. In other words, the sender cannot deny sending the message, and the receiver cannot deny receiving it.

This concept is crucial in **digital transactions**, where it helps establish trust and accountability. Non-repudiation prevents parties from later claiming that the message wasn’t sent or received, thus confirming the **authenticity** of the communication.

---

## 5. What is Integrity?

**Integrity** refers to the assurance that the message has not been altered or tampered with during its transmission. 

When a message is sent, the receiver should receive the **exact** message as it was originally sent, without any modifications. If any changes occur to the message during transmission, the integrity of the message is compromised.

Ensuring integrity is vital to maintain the **authenticity** of the data.

---

## 6. What is Message Digest?

A **message digest** is a unique digital fingerprint of a message, created by applying a special algorithm called a **one-way hash function**. 

This process converts the original message into a fixed-length string of characters (numbers and letters). The message digest is so unique that even the smallest change in the message would result in a completely different digest. This makes it useful for verifying data **integrity**.

---

### Connection Between Message Digest and Digital Signature:

When the sender encrypts the message digest using their **private key**, it forms a **digital signature**. 

A **digital signature** serves as an electronic form of authentication, confirming that the message was indeed sent by the sender and that it has not been altered during transmission. It ensures the **authenticity** of the message and verifies its **integrity**.

---

## Summary:

These terms work together to create a secure communication system where:

- **Public and private keys** enable secure message encryption and decryption.
- **Authentication** ensures the identity of the users.
- **Non-repudiation** guarantees that neither party can deny their actions.
- **Integrity** ensures the message remains unchanged during transmission.
- A **message digest** verifies the integrity of the message, and a **digital signature** authenticates it.

---