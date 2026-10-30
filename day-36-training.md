# Day 36 — Cryptography and AES Review

**Environment:** Kali Linux

## Topics
- **Main topic:** Cryptography and AES Review
- **Focus:** Review keys, nonces, authentication

## Learning Notes

Today I reviewed the important cryptography concepts covered during my AES encryption project.

### 1. Encryption Keys

An encryption key is a secret value used by an encryption algorithm to protect information.

In my AES project, the key is used to encrypt sample files and must also be available for authorized decryption.

Important points:
- Keep encryption keys private.
- Never publish keys in a GitHub repository.
- Use securely generated keys.
- Protect backups of important keys.

### 2. Nonces

A nonce is a value used once in a cryptographic operation. AES-GCM uses a nonce alongside the encryption key.

Important points:
- A nonce does not need to be secret.
- It must be unique for each encryption operation when using the same AES-GCM key.
- Reusing a nonce with the same key can seriously weaken security.
- The nonce can be stored alongside the encrypted data so it is available during decryption.

### 3. Authentication

Authentication helps verify that encrypted data has not been modified.

AES-GCM provides authenticated encryption. During decryption, it checks the authentication information before accepting the plaintext.

For example, if someone changes the encrypted sample file or supplies an incorrect key, the authentication check should fail.

### 4. AES-GCM Project Review

My project uses AES-GCM as its encryption approach.

The main process is:

1. Generate or obtain a secure encryption key.
2. Generate a fresh nonce.
3. Encrypt the sample file using AES-GCM.
4. Store the nonce with the encrypted data.
5. During decryption, use the correct key and stored nonce.
6. Accept the plaintext only if authentication succeeds.

## Practical Work and Tools

- **What I actually did:** I reviewed encryption keys, nonce uniqueness, authentication, and the AES-GCM process used in my project. I have not confirmed performing new encryption or decryption tests today.
- **Tools actually used:** Kali Linux is the training environment. Python and the AES-GCM cryptography library are relevant to the project, but I have not confirmed using them for practical work today.
- **Evidence:** No new screenshots, test results, or GitHub commits have been confirmed.

## Key Takeaways

- An encryption key must remain secret.
- An AES-GCM nonce must be unique for every encryption under the same key.
- A nonce is not the same thing as an encryption key.
- AES-GCM provides confidentiality and authentication.
- Modified ciphertext or an incorrect key should cause authentication failure.
- **Important lesson:** Never reuse an AES-GCM nonce with the same key.

## Challenges and Questions

One concept I want to review further is the difference between a nonce and an authentication tag. I also want to understand how the project stores the nonce with ciphertext and how authentication failures are handled safely.

## Reflection

Today I reviewed the main cryptography concepts from my AES project. I understand better why keys must remain secret, why nonces must not be reused with the same key, and why authentication is necessary during decryption. I want to continue reviewing AES-GCM and make sure I understand the complete encryption and decryption process.

## Safety

Only test systems and files that I own or have explicit permission to assess. Never publish passwords, encryption keys, private data, or confidential project information in GitHub repositories or screenshots.
