# Day 22 — Symmetric and Asymmetric Encryption

**Environment:** Kali Linux  
**Main Topic:** Symmetric and Asymmetric Encryption  
**Focus:** Shared Keys and Public/Private Keys

## 1. Learning Notes

Today I learned about the two main types of encryption: symmetric encryption and asymmetric encryption. Both help protect information, but they use keys differently.

**1. Symmetric Encryption**

Symmetric encryption uses the same secret key to encrypt and decrypt information.

For example:
- A sender encrypts a message using a secret key.
- The receiver uses the same key to decrypt the message.
- Both parties must keep the key private.

**Advantages:**
- Generally fast and efficient.
- Suitable for encrypting large amounts of data.
- Useful for protecting files and stored information.

**Challenge:** The secret key must be shared securely between the people or systems that need it.

**2. Asymmetric Encryption**

Asymmetric encryption uses a pair of related keys:

- **Public key:** Can be shared with others.
- **Private key:** Must be kept secret by its owner.

For example, when someone encrypts information using a recipient's public key, the corresponding private key can be used to decrypt it.

Asymmetric cryptography can also support digital signatures, which help verify the origin and integrity of information.

**Advantages:**
- Helps establish secure communication without first sharing a secret encryption key.
- Supports digital signatures and identity verification.
- Makes secure key exchange possible.

**3. Main Differences**

| Feature | Symmetric Encryption | Asymmetric Encryption |
|---|---|---|
| Keys | One shared secret key | Public and private key pair |
| Speed | Generally faster | Generally slower |
| Key sharing | Secret key must be shared securely | Public key can be shared openly |
| Common use | File and data encryption | Key exchange and digital signatures |
| Example | AES | RSA |

**4. Hybrid Encryption**

Modern secure communication often combines both approaches.

For example, asymmetric cryptography can help establish or protect a temporary symmetric session key. Symmetric encryption is then used to protect the actual communication because it is generally more efficient for large amounts of data.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the differences between symmetric and asymmetric encryption, including shared secret keys, public/private key pairs, and hybrid encryption. I have not confirmed generating keys or performing an encryption exercise during this session.

**Tools actually used:**  
No specific encryption tools are confirmed as used during this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No generated keys, encryption results, screenshots, or practical test results are confirmed.

## 3. Key Takeaways

- Symmetric encryption uses one shared secret key.
- Asymmetric encryption uses a public/private key pair.
- Private keys must always be protected.
- Public keys can be shared, but their authenticity should be verified.
- Symmetric encryption is generally faster for large amounts of data.
- Hybrid encryption combines the strengths of both approaches.

**Important principle:** Never share a private key or expose a symmetric secret key publicly.

## 4. Challenges and Questions

One challenge is understanding how two people can communicate securely without sharing a secret key beforehand.

Questions for further study:
- How are public and private keys generated?
- How does RSA encryption work at a basic level?
- How does AES protect files?
- How can someone verify that a public key belongs to the correct person?
- How does hybrid encryption work in HTTPS?

## 5. Reflection

Today I learned that symmetric and asymmetric encryption solve related but different security problems. Symmetric encryption is efficient for protecting data, while asymmetric cryptography helps with key exchange and digital signatures.

I want to review how AES and RSA work at a beginner level and understand how both methods are combined in real-world secure communication.

## 6. Safety

All cryptography experiments will use sample data and systems I own or have permission to use. I will keep private keys and secret encryption keys secure. I will never publish passwords, private keys, personal data, or sensitive files in my GitHub repository.
