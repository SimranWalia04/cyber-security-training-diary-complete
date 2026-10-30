# Day 28 — AES File Decryption

**Environment:** Kali Linux  
**Main Topic:** AES File Decryption  
**Focus:** Recovering Original File Content

## 1. Learning Notes

Today I learned how AES decryption works and how encrypted files can be converted back into their original readable form using the correct secret key.

Decryption is an important part of my AES file encryption project because it allows authorized users to recover their protected information.

**1. What Is Decryption?**

Decryption is the process of converting ciphertext back into plaintext using the appropriate decryption algorithm and key.

For AES, the same secret key used for encryption is required for decryption.

**2. Reading the Encrypted File**

The first step is to read the encrypted file in binary mode.

Example:

```python
with open("encrypted_file.bin", "rb") as file:
    encrypted_data = file.read()
```

Binary mode is important because encrypted data may contain arbitrary byte values rather than ordinary readable text.

**3. Retrieving the Nonce**

AES-GCM requires the nonce used during encryption.

In my project design, the nonce is stored together with the ciphertext. During decryption, the program retrieves the nonce and separates it from the encrypted content.

The nonce is not a secret key, but it must match the value used during encryption.

**4. Decrypting with AES-GCM**

The program uses the secret key and stored nonce to attempt decryption.

AES-GCM also verifies the authentication tag. This helps detect:
- An incorrect encryption key.
- Modified ciphertext.
- An incorrect nonce.
- Invalid authenticated data.

If authentication fails, the program must reject the result rather than treating the decrypted data as valid.

**5. Recovering the Original File**

After successful authentication, the program can write the recovered plaintext to a new output file.

For example:

```python
with open("recovered_file.txt", "wb") as file:
    file.write(decrypted_data)
```

The original file should be preserved during testing to avoid accidental data loss.

**6. Verifying the Result**

A successful decryption should recover the original file contents exactly.

A useful way to verify this is to compare the SHA-256 hashes of the original and recovered files. Matching hashes provide strong evidence that their contents are identical.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the AES-GCM decryption workflow, including reading encrypted files, retrieving nonces, checking authentication, and recovering original file contents. I have not confirmed executing a separate decryption test during this session.

**Tools actually used:**
- Kali Linux — learning environment.
- Python 3 — programming language selected for the project.
- AES-GCM — encryption method selected for the project.

No additional tool execution is confirmed for this session.

**Evidence:**  
These learning notes document the decryption process. No recovered files, hash comparisons, screenshots, or new commits are confirmed.

## 3. Key Takeaways

- Decryption converts ciphertext back into plaintext.
- AES uses the same secret key for encryption and decryption.
- AES-GCM requires the correct nonce and authentication information.
- Authentication must succeed before recovered data is accepted.
- Binary file handling is useful for encrypted files.
- Comparing SHA-256 hashes can help verify file recovery.
- Original files should be preserved during testing.

**Important Python example:**

```python
with open("recovered_file.txt", "wb") as file:
    file.write(decrypted_data)
```

**Important principle:** Never accept decrypted data as valid unless AES-GCM authentication succeeds.

## 4. Challenges and Questions

One challenge is understanding how the program identifies an incorrect key or modified ciphertext during decryption.

Questions for further study:
- How does AES-GCM verify the authentication tag?
- What happens when the wrong key is provided?
- Why must the original nonce be available during decryption?
- How can SHA-256 verify that a recovered file matches the original?
- How should a program handle corrupted or incomplete encrypted files?

## 5. Reflection

Today I learned that secure file encryption also requires a reliable decryption process. Recovering the original file depends on the correct secret key, nonce, and successful authentication.

I also understood that comparing file hashes can help confirm whether the recovered content matches the original. I want to review authentication failure handling and file verification so that my AES project can safely handle incorrect keys and damaged encrypted files.

## 6. Safety

All decryption experiments will use sample files that I own or have permission to use. I will preserve original files, protect encryption keys, and avoid accepting data when authentication fails. I will never publish passwords, keys, personal data, or private system details in my GitHub repository.
