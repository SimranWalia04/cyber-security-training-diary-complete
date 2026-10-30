# Day 23 — AES Overview

**Environment:** Kali Linux  
**Main Topic:** AES Overview  
**Focus:** AES as a Symmetric Block Cipher

## 1. Learning Notes

Today I learned about **AES (Advanced Encryption Standard)**, a widely used symmetric encryption algorithm that protects digital information.

**1. What Is AES?**

AES is a symmetric block cipher. This means it encrypts and decrypts data using the same secret key and processes information in fixed-size blocks.

AES uses a block size of 128 bits (16 bytes).

**2. AES Key Sizes**

AES supports three key sizes:

- **AES-128:** Uses a 128-bit key.
- **AES-192:** Uses a 192-bit key.
- **AES-256:** Uses a 256-bit key.

All three use a 128-bit block size, but they differ in key length and number of encryption rounds.

| AES Version | Key Size | Encryption Rounds |
|---|---:|---:|
| AES-128 | 128 bits | 10 |
| AES-192 | 192 bits | 12 |
| AES-256 | 256 bits | 14 |

**3. How AES Works**

At a high level, AES transforms plaintext into ciphertext through several rounds of mathematical operations.

The main operations include:

- **SubBytes:** Replaces bytes using a substitution table.
- **ShiftRows:** Rearranges rows of the data.
- **MixColumns:** Combines data within columns.
- **AddRoundKey:** Combines the data with a round key derived from the original key.

These operations help make the encrypted output difficult to understand without the correct key.

**4. AES Modes of Operation**

AES is a block cipher, so a mode of operation determines how it is used to encrypt data.

Some common modes include:

- **ECB:** Encrypts blocks independently; it can reveal patterns and should generally be avoided.
- **CBC:** Uses chaining between blocks and requires careful handling of initialization vectors and padding.
- **CTR:** Uses a counter to generate a stream of encrypted data.
- **GCM:** Provides authenticated encryption, helping protect both confidentiality and integrity.

AES-GCM is especially useful because it can detect unauthorized changes to encrypted data.

**5. Real-World Uses**

AES is used in many areas of technology, including:
- File encryption.
- Secure network communication.
- Database protection.
- Device and storage security.
- Backup protection.

## 2. Practical Work and Tools

**What I actually did:**  
I studied AES as a symmetric block cipher, its key sizes, basic encryption operations, and common modes of operation. I have not confirmed performing a separate AES encryption exercise during this session.

**Tools actually used:**  
No specific AES tools are confirmed as used during this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No AES command output, screenshots, or practical test results are confirmed.

## 3. Key Takeaways

- AES is a symmetric block cipher.
- AES always uses a 128-bit block size.
- AES supports 128-bit, 192-bit, and 256-bit keys.
- The same secret key is used for encryption and decryption.
- AES-GCM provides both encryption and authentication.
- ECB mode is generally unsuitable for protecting sensitive data because it can reveal patterns.

**Important principle:** Choosing a secure encryption mode and managing keys properly are just as important as choosing a strong encryption algorithm.

## 4. Challenges and Questions

One concept I want to understand better is how AES processes data through multiple rounds and how its different modes affect security.

Questions for further study:
- Why does AES always use a 128-bit block size?
- What is the difference between AES-128 and AES-256?
- Why should ECB mode generally be avoided?
- What is an initialization vector or nonce?
- How does AES-GCM detect modified ciphertext?

## 5. Reflection

Today I learned that AES is an important encryption standard used to protect digital information. I understood that it uses a shared secret key and supports different key sizes and modes of operation.

I want to review AES-GCM in more detail and understand how nonces, authentication tags, and encryption keys work together. This will help me understand secure file encryption and the cryptography project in my training repository.

## 6. Safety

All encryption experiments will use sample data in systems I own or have permission to use. I will use established cryptographic libraries rather than designing my own encryption algorithm. I will never publish secret keys, passwords, personal data, or sensitive files in my GitHub repository.
