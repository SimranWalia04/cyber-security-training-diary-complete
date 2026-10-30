# Day 37 — AES Project Improvements

**Environment:** Kali Linux

## Topics
- **Main topic:** AES Project Improvements
- **Focus:** Error handling, overwrite protection, usability

## Learning Notes

Today I studied ways to improve my AES file-encryption project. A secure project should not only encrypt and decrypt files correctly but should also handle unexpected situations safely.

### 1. Error Handling

Error handling allows a program to respond properly when something goes wrong.

Examples include:
- The input file does not exist.
- The encryption key is invalid.
- The encrypted file has been modified.
- The user provides an incorrect file path.
- Decryption authentication fails.

Python uses exceptions to handle these situations. The program should display a helpful error message without revealing secret information.

### 2. Overwrite Protection

Overwrite protection prevents the program from accidentally replacing an existing file.

For example, before saving a decrypted file, the program should check whether a file with the same name already exists.

A safer design is to ask for confirmation or stop and request a different output filename.

### 3. Usability Improvements

A project should be easy to understand and operate.

Possible improvements include:
- Clear instructions for encryption and decryption.
- Helpful messages when an operation succeeds or fails.
- Clear input and output file paths.
- Validation of user input.
- Simple documentation explaining the project.

### 4. AES-GCM Safety

The project should accept decrypted data only after AES-GCM authentication succeeds. It should not leave a misleading output file when decryption fails.

These improvements make the project more reliable and easier for another person to understand.

## Practical Work and Tools

- **What I actually did:** I reviewed possible improvements to the AES project, including error handling, overwrite protection, and usability. I have not confirmed changing the source code or implementing these improvements today.
- **Tools actually used:** Kali Linux is the training environment. Python and the AES-GCM library are relevant to the project, but I have not confirmed using them for today's improvements.
- **Evidence:** No updated source code, screenshots, test output, or GitHub commit has been confirmed.

## Key Takeaways

- Error handling helps a program respond safely to unexpected situations.
- Overwrite protection helps prevent accidental data loss.
- Clear instructions make software easier to use.
- Authentication failures must not produce trusted plaintext.
- **Important lesson:** A reliable encryption program must protect both the data and the user's existing files.

## Challenges and Questions

One challenge is deciding how the program should handle an existing output file without accidentally deleting useful information. I also want to review how Python exceptions can provide helpful messages while keeping sensitive details private.

## Reflection

Today I learned that improving an encryption project involves more than adding cryptographic features. Safe error handling, overwrite protection, and clear instructions are also important. I want to review these improvements and understand how they can make my AES project more dependable.

## Safety

Only test systems and files that I own or have explicit permission to assess. Use harmless sample files during testing. Never include passwords, encryption keys, personal data, or private system details in project documentation or GitHub commits.
