# Day 26 — AES Project Planning

**Environment:** Kali Linux  
**Main Topic:** AES Project Planning  
**Focus:** Requirements, File I/O, and Test Cases

## 1. Learning Notes

Today I learned how to plan a small cybersecurity project before starting the implementation. Planning helps identify what the program should do, what tools it needs, and how its functionality will be tested.

My project focuses on building an educational file encryption and decryption program using AES.

**1. Project Requirements**

Requirements describe the features and behavior expected from a project.

The main requirements for my AES file encryption project include:

- Encrypt a selected file.
- Decrypt an encrypted file using the correct key.
- Generate a secure encryption key.
- Use AES-GCM for authenticated encryption.
- Handle incorrect keys and modified encrypted files safely.
- Display useful error messages.
- Avoid exposing secret keys or sensitive file contents.

**2. File Input and Output (File I/O)**

File I/O means reading information from files and writing information to files.

For my project:
- The program reads the original file.
- It encrypts the file contents.
- It writes the encrypted data to an output file.
- During decryption, it reads the encrypted file.
- It verifies and decrypts the data before writing the recovered file.

Python provides built-in file handling functions such as `open()`.

Example:

```python
with open("example.txt", "rb") as file:
    data = file.read()
```

The `rb` mode reads a file as binary data, which is useful when working with files that may contain more than ordinary text.

**3. Test Cases**

Test cases help verify that a program behaves as expected.

Important test cases for my AES project include:

| Test Case | Expected Result |
|---|---|
| Encrypt a valid file | Encrypted output is created |
| Decrypt with the correct key | Original content is recovered |
| Decrypt with an incorrect key | Authentication fails |
| Modify encrypted data | Tampering is detected |
| Use an invalid input path | A useful error is displayed |
| Encrypt an empty file | Program handles it correctly |

**4. Project Security Considerations**

The project should use a trusted cryptographic library rather than implementing AES manually.

AES-GCM requires a unique nonce for every encryption performed with the same key. The nonce does not need to be secret, but it must be stored with the encrypted data so that decryption can use it.

The encryption key must remain secret and should not be stored directly in the source code.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the planning requirements for an AES file encryption project, including file input/output, expected functionality, security considerations, and test cases. I have not confirmed completing a separate planning document or implementation exercise during this session.

**Tools actually used:**
- Kali Linux — learning environment.
- Python 3 — programming language selected for the project.
- AES-GCM — encryption method selected for the project.

No additional project tools or commands are confirmed as used during this session.

**Evidence:**  
These learning notes document the project requirements and proposed test cases. No separate planning screenshots or new commits are confirmed.

## 3. Key Takeaways

- Project requirements explain what a program must accomplish.
- File I/O allows Python programs to read and write files.
- Binary mode is useful for handling different file types.
- Test cases help identify errors and verify expected behavior.
- AES-GCM provides encryption and authentication.
- Nonces must not be reused with the same AES-GCM key.
- Encryption keys must be protected.

**Important Python example:**

```python
with open("example.txt", "rb") as file:
    data = file.read()
```

**Important principle:** Plan the requirements and security behavior before writing the implementation.

## 4. Challenges and Questions

One challenge is planning how the program should handle incorrect keys, modified encrypted files, and missing input files.

Questions for further study:
- How should encrypted data and its nonce be stored together?
- How can Python handle file-related errors?
- How can I verify that decrypted content matches the original?
- Why is authentication important in file encryption?
- How should a project protect generated encryption keys?

## 5. Reflection

Today I learned that successful cybersecurity projects require careful planning before coding begins. I understood that requirements, file handling, and test cases help make a program more reliable and secure.

I also learned that an encryption project must consider more than simply encrypting data. It should handle errors, detect tampering, protect keys, and recover the original file correctly.

I want to review Python file handling and test-case design before moving further with the AES implementation.

## 6. Safety

All project development and testing will use files and systems I own or have permission to use. I will use trusted cryptographic libraries, protect generated encryption keys, and avoid overwriting original files during testing. I will never publish passwords, keys, personal data, or private system details in my GitHub repository.
