# Day 27 — AES File Encryption

**Environment:** Kali Linux  
**Main Topic:** AES File Encryption  
**Focus:** Python File Encryption Workflow

## 1. Learning Notes

Today I learned how AES encryption can be used in a Python program to protect files. File encryption converts readable file contents into ciphertext so that unauthorized people cannot easily understand the information.

My project uses **AES-GCM**, which provides both confidentiality and authentication.

**1. Reading a File**

The first step in file encryption is reading the original file.

Python supports binary file reading using `rb` mode.

Example:

```python
with open("example.txt", "rb") as file:
    data = file.read()
```

Binary mode is useful because encryption programs may need to handle text documents, images, PDFs, and other file types.

**2. Generating an Encryption Key**

AES requires a secret key.

AES supports key sizes of 128, 192, and 256 bits. A secure random key should be generated using a trusted cryptographic library.

The key must be protected because anyone who obtains it may be able to decrypt the files.

**3. Encrypting File Contents**

The encryption workflow includes:

1. Read the original file.
2. Generate or securely obtain an AES key.
3. Generate a unique nonce for AES-GCM.
4. Encrypt the file contents.
5. Store the nonce together with the encrypted data.
6. Save the encrypted output in a separate file.

The nonce is not secret, but it must be unique for every encryption performed with the same key.

**4. Decrypting a File**

Decryption reverses the encryption process when the correct key is available.

The workflow includes:
- Read the encrypted file.
- Extract the stored nonce.
- Use the correct secret key.
- Verify the authentication tag.
- Recover the original contents only if authentication succeeds.

If the encrypted data has been modified or the wrong key is used, AES-GCM authentication should fail.

**5. Protecting Original Files**

A safe encryption program should write encrypted data to a separate output file rather than immediately replacing the original.

This helps prevent accidental data loss during development and testing.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the Python file encryption workflow using AES-GCM, including reading files, generating keys and nonces, encrypting data, and saving encrypted output. I have not confirmed writing or executing the encryption code during this particular session.

**Tools actually used:**
- Kali Linux — learning environment.
- Python 3 — programming language selected for the project.
- AES-GCM — encryption method selected for the project.

No additional tool execution is confirmed for this session.

**Evidence:**  
These learning notes document the encryption workflow. No new terminal output, encryption screenshots, or commits are confirmed.

## 3. Key Takeaways

- AES is a symmetric encryption algorithm.
- AES-GCM protects confidentiality and detects unauthorized modifications.
- Python can read and write files in binary mode.
- Encryption requires a securely generated secret key.
- AES-GCM requires a unique nonce for each encryption under the same key.
- The nonce must be stored with the ciphertext.
- Decrypted data should only be accepted after successful authentication.

**Important Python example:**

```python
with open("example.txt", "rb") as file:
    data = file.read()
```

**Important principle:** Never reuse an AES-GCM nonce with the same encryption key.

## 4. Challenges and Questions

One challenge is understanding how the program should store the nonce and encrypted data so that the decryption process can recover the original file correctly.

Questions for further study:
- How should a secure AES key be generated?
- How does AES-GCM produce an authentication tag?
- Why must the nonce be unique?
- How should the program handle incorrect keys?
- How can the program prevent accidental overwriting of original files?

## 5. Reflection

Today I learned how Python file handling and AES encryption work together to protect digital information. I understood that file encryption involves more than converting plaintext into ciphertext. The program must also manage keys, generate unique nonces, store encrypted data correctly, and verify authentication during decryption.

I want to review the complete encryption and decryption workflow and understand how to handle errors safely. This will help me improve the AES file encryption project in my cybersecurity repository.

## 6. Safety

All encryption experiments will use sample files that I own or have permission to use. I will preserve original files during testing, use trusted cryptographic libraries, and protect generated encryption keys. I will never publish passwords, keys, personal data, or private system details in my GitHub repository.
