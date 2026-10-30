# Day 24 — AES Modes and Authentication

**Environment:** Kali Linux  
**Main Topic:** AES Modes and Authentication  
**Focus:** Modes, Nonce/IV Handling, and Authenticated Encryption

## 1. Learning Notes

Today I learned that AES needs a mode of operation to determine how data is encrypted. Different modes provide different security properties, and choosing the correct mode is important.

**1. AES Modes of Operation**

Some common AES modes include:

- **ECB (Electronic Codebook):** Encrypts each block independently. Repeated plaintext patterns can produce repeated ciphertext patterns, so it is generally unsuitable for sensitive information.
- **CBC (Cipher Block Chaining):** Each plaintext block is combined with the previous ciphertext block before encryption. It requires an initialization vector (IV) and appropriate padding.
- **CTR (Counter Mode):** Uses a counter to generate a stream of encrypted data. Counter values must never be reused with the same key.
- **GCM (Galois/Counter Mode):** Provides authenticated encryption, protecting confidentiality and helping detect unauthorized changes.

**2. Nonce and Initialization Vector (IV)**

A nonce or IV is an additional value used by certain encryption modes.

Its purpose depends on the mode, but it helps ensure that encrypting the same information does not always produce the same ciphertext.

Important points:
- A nonce is generally not secret.
- Some modes require unique nonces for each encryption under the same key.
- Reusing a nonce with the same key in AES-GCM can seriously compromise security.
- IV and nonce requirements depend on the encryption mode.

**3. Authenticated Encryption**

Encryption protects confidentiality, but confidentiality alone does not guarantee that encrypted information has not been modified.

Authenticated encryption provides two important protections:

- **Confidentiality:** Prevents unauthorized people from reading the information.
- **Integrity and authenticity:** Helps detect changes and verify that the encrypted data is valid.

AES-GCM is an example of an authenticated encryption mode.

It produces an authentication tag that is checked during decryption. If the ciphertext or associated authenticated data has been modified, authentication should fail.

**4. Associated Authenticated Data (AAD)**

Some authenticated encryption modes, including AES-GCM, support additional authenticated data.

AAD is information that is authenticated but not encrypted.

For example, an application might authenticate a file identifier or metadata while keeping the actual file contents encrypted.

## 2. Practical Work and Tools

**What I actually did:**  
I studied AES modes of operation, nonce and IV handling, and the purpose of authenticated encryption. I also reviewed why nonce reuse is dangerous in AES-GCM. I have not confirmed performing a separate encryption or authentication test during this session.

**Tools actually used:**  
No specific encryption or testing tools are confirmed as used during this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No encryption outputs, authentication tags, screenshots, or practical test results are confirmed.

## 3. Key Takeaways

- AES modes determine how the block cipher is used.
- ECB can reveal patterns and should generally be avoided.
- Nonces and IVs must follow the requirements of their encryption mode.
- AES-GCM provides confidentiality and authentication.
- Reusing a nonce with the same AES-GCM key is dangerous.
- Authentication tags help detect unauthorized modifications.
- Sensitive keys must remain secret, even though nonces and IVs are generally not secret.

**Important principle:** Use a trusted authenticated encryption mode such as AES-GCM and follow its nonce requirements carefully.

## 4. Challenges and Questions

One concept I want to understand better is why nonce reuse can cause serious security problems in AES-GCM.

Questions for further study:
- What is the exact difference between a nonce and an IV?
- Why must AES-GCM nonces be unique for a given key?
- What happens if an authentication tag does not match?
- What is the purpose of associated authenticated data?
- How should an application store and manage nonces?

## 5. Reflection

Today I learned that selecting AES alone is not enough to guarantee secure encryption. The mode of operation, nonce or IV handling, and authentication are all important parts of protecting information.

I understood why AES-GCM is useful for protecting both confidentiality and integrity. I want to review nonce management and authentication tags further so I can better understand how secure file encryption works.

## 6. Safety

All cryptography experiments will use sample data and systems I own or have permission to use. I will use trusted cryptographic libraries and follow their documented nonce requirements. I will never publish passwords, secret keys, private information, or sensitive encrypted files in my GitHub repository.
