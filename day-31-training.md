# Day 31 — File Integrity and Errors

**Environment:** Kali Linux

## Topics
- **Main topic:** File Integrity and Errors
- **Focus:** Authentication failures and safe error handling

## Learning Notes

Today I studied file integrity and how an AES encryption program should respond when something goes wrong.

File integrity means ensuring that data has not been changed unexpectedly. AES-GCM provides authenticated encryption, which helps detect whether encrypted data has been modified.

Important concepts:

1. **Authentication failure:** If the encrypted data has been changed or the wrong key is used, AES-GCM authentication should fail.
2. **Safe error handling:** The program should report that decryption failed without exposing secret information.
3. **Preventing invalid output:** The program must not treat unauthenticated or partially decrypted data as a successful result.
4. **File validation:** The program should handle missing files, empty files, and invalid input appropriately.

For example, if someone changes a byte in an encrypted sample file, AES-GCM should reject the data during decryption instead of returning it as trusted plaintext.

A useful distinction is that a cryptographic hash such as SHA-256 can help check file integrity, but a hash by itself does not encrypt a file or prove who created it.

## Practical Work and Tools

- **What I actually did:** I reviewed how AES-GCM detects modified encrypted data and studied safe responses to authentication and file-handling errors. I have not confirmed running these tests or changing the project code today.
- **Tools actually used:** Kali Linux is the training environment. AES-GCM and Python are relevant technologies from the project, but I have not confirmed using them for practical tests today.
- **Evidence:** No screenshot, test output, or GitHub commit has been confirmed.

## Key Takeaways

- Authentication helps detect modified encrypted data.
- A wrong key should result in an authentication failure.
- Decryption failures must not be treated as successful operations.
- Error messages should explain the problem without revealing keys or other secrets.
- **Important lesson:** Never trust decrypted data unless its authentication check succeeds.

## Challenges and Questions

One challenge is understanding how to handle authentication errors without accidentally creating an incomplete output file. I also want to review how Python handles missing files, invalid input, and exceptions during file operations.

## Reflection

Today I learned that file integrity is an important part of secure encryption. It is not enough to encrypt and decrypt data; the program must also detect unexpected changes and handle failures safely. I want to review Python exception handling and practise these cases with harmless sample files in my local training environment.

## Safety

Only test systems and files that I own or have explicit permission to assess. Never include passwords, encryption keys, personal data, or private system details in GitHub screenshots, logs, or commits.
