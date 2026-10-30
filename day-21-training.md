# Day 21 — Cryptography Introduction

**Environment:** Kali Linux  
**Main Topic:** Cryptography Introduction  
**Focus:** Plaintext, Ciphertext, Encryption, and Hashing

## 1. Learning Notes

Today I learned the basic concepts of cryptography and how it helps protect information from unauthorized access.

**1. Plaintext**

Plaintext is the original, readable information before encryption.

Example:

`Hello, this is a secret message.`

**2. Ciphertext**

Ciphertext is the unreadable or transformed information produced after encryption. It can be converted back into plaintext through the correct decryption process when the encryption method supports it.

**3. Encryption and Decryption**

Encryption converts readable information into ciphertext using an algorithm and a key. Decryption converts the ciphertext back into readable information using the appropriate key.

There are two common types of encryption:

- **Symmetric encryption:** The same secret key is used for encryption and decryption.
- **Asymmetric encryption:** A public key and a private key are used for related cryptographic operations.

Encryption helps protect sensitive information, including files and communications.

**4. Hashing**

Hashing converts input data into a fixed-length output called a hash or digest.

Important characteristics:
- A secure cryptographic hash function is designed to make it difficult to recover the original input.
- The same input produces the same hash when using the same algorithm.
- A small change in the input usually produces a very different digest.
- Hashing is generally one-way, unlike encryption.

For example, SHA-256 is a commonly used cryptographic hash function.

A hash can help verify whether a file has changed. However, hashing alone does not encrypt or hide the original file.

**5. Encryption vs. Hashing**

- Encryption is designed to protect information while allowing authorized decryption.
- Hashing produces a digest that can be used for integrity checking and other security purposes.
- Passwords should generally be stored using dedicated password-hashing methods, such as Argon2id, rather than ordinary fast hashes alone.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the basic principles of cryptography, including plaintext, ciphertext, encryption, decryption, and hashing. I have not confirmed performing an encryption or hashing exercise during this session.

**Tools actually used:**  
No specific cryptography tools are confirmed as used during this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No practical screenshots, generated hashes, or encryption results are confirmed.

## 3. Key Takeaways

- Plaintext is the original readable information.
- Ciphertext is the encrypted form of information.
- Encryption protects information and can be reversed through authorized decryption.
- Hashing creates a fixed-length digest and is not the same as encryption.
- SHA-256 is a widely used cryptographic hash function.
- Strong key management is essential for secure encryption.

**Important principle:** Use encryption when information needs to be protected and later recovered. Use an appropriate cryptographic hash when checking data integrity.

## 4. Challenges and Questions

One concept I want to understand better is the difference between encryption and hashing, because both transform data but serve different purposes.

Questions for further study:
- How does symmetric encryption work?
- What is the difference between public and private keys?
- Why is SHA-256 commonly used?
- How can a file's hash help verify its integrity?
- Why should passwords use dedicated password-hashing algorithms?

## 5. Reflection

Today I learned that cryptography plays an important role in protecting digital information. Encryption helps keep information confidential, while hashing helps verify data integrity and supports secure password storage when appropriate methods are used.

I want to review symmetric and asymmetric encryption and understand how cryptographic keys are generated and protected. These concepts will help me understand how secure applications and file-protection systems work.

## 6. Safety

All cryptography experiments will be performed using sample data in an environment I own or have permission to use. I will never publish real passwords, encryption keys, private keys, personal information, or sensitive files in my GitHub repository.
