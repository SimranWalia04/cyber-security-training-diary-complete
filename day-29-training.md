# Day 29 — Key Management

**Environment:** Kali Linux  
**Main Topic:** Key Management  
**Focus:** Key Secrecy, Nonce Uniqueness, and Secret Storage

## 1. Learning Notes

Today I learned about key management and why protecting encryption keys is just as important as choosing a strong encryption algorithm.

Key management involves generating, storing, using, protecting, and replacing cryptographic keys safely.

**1. Key Secrecy**

An encryption key is sensitive information used to encrypt and decrypt data.

Important practices include:
- Generate keys using a secure random number generator.
- Keep secret keys private.
- Never publish keys in GitHub repositories.
- Avoid placing keys directly inside source code.
- Restrict access to keys to authorized users.

For my AES project, the encryption key must remain secret because someone who obtains it may be able to decrypt protected files.

**2. Nonce Uniqueness**

A nonce is a value used during encryption. AES-GCM requires a unique nonce for every encryption performed with the same key.

Important points:
- A nonce does not need to be secret.
- Nonces must be stored so that decryption can use the correct value.
- Reusing a nonce with the same AES-GCM key can seriously weaken security.
- A new nonce should be generated for each encryption operation.

**3. Secure Secret Storage**

Secret storage means keeping sensitive information away from unauthorized access.

Examples of good practices:
- Use environment variables or a suitable secret-management system when appropriate.
- Restrict file permissions for sensitive key files.
- Avoid committing secret files to GitHub.
- Keep secure backups of important keys.
- Do not print secret keys in terminal output or application logs.

A `.gitignore` file can help prevent sensitive files from being accidentally added to a Git repository.

Example:

```gitignore
.env
*.key
secrets/
```

This is a preventive measure, not a replacement for checking what is included in a commit.

**4. Key Backup and Recovery**

If an encryption key is lost, encrypted files may become permanently inaccessible.

Therefore:
- Important keys need secure backups.
- Backups should have restricted access.
- Recovery procedures should be considered before encrypting important files.
- Keys should not be stored alongside encrypted data without appropriate protection.

## 2. Practical Work and Tools

**What I actually did:**  
I studied key secrecy, AES-GCM nonce uniqueness, secure secret storage, and the importance of key backups. I have not confirmed changing key-storage settings or implementing a key-management system during this session.

**Tools actually used:**
- Kali Linux — learning environment.
- AES-GCM — encryption method discussed in the project.
- Git and `.gitignore` — concepts reviewed for protecting repository contents; actual configuration changes are not confirmed.

**Evidence:**  
These learning notes document key-management principles. No key-generation output, storage configuration screenshots, or new commits are confirmed.

## 3. Key Takeaways

- Encryption keys must remain secret.
- Secure random generation is important for cryptographic keys.
- AES-GCM nonces must be unique for each encryption under the same key.
- Nonces are generally not secret but must be available for decryption.
- Secret keys should never be committed to GitHub.
- Key backups are important because losing a key can mean losing access to encrypted data.
- `.gitignore` helps prevent accidental inclusion of sensitive files.

**Important principle:** Protect the key, never reuse an AES-GCM nonce with the same key, and plan secure key recovery.

## 4. Challenges and Questions

One challenge is understanding how to store encryption keys securely while still allowing an authorized application to use them.

Questions for further study:
- What is the safest way to generate an AES key?
- How should encryption keys be backed up?
- What happens if an AES-GCM nonce is reused?
- How do environment variables help protect secrets?
- What is the difference between key storage and key backup?
- How can I check that a repository does not contain sensitive information?

## 5. Reflection

Today I learned that secure encryption depends on proper key management. Even a strong algorithm such as AES-GCM cannot protect information if its secret key is exposed or handled carelessly.

I also understood the importance of nonce uniqueness and why encryption keys should not be published in source code or GitHub repositories. I want to review secure key generation, storage, and backup methods before completing my AES project.

## 6. Safety

All key-management experiments will use sample data and systems I own or have permission to use. I will never publish real encryption keys, passwords, API tokens, private information, or sensitive configuration files. I will review repository contents before committing or uploading files to GitHub.
