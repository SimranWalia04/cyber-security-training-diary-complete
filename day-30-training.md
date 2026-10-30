# Day 30 — AES Project Testing

**Environment:** Kali Linux

## Topics
- **Main topic:** AES Project Testing
- **Focus:** Round-trip, wrong-key, modified-ciphertext tests

## Learning Notes

Today I studied how to test an AES file-encryption project. Testing helps confirm that the program behaves correctly in normal situations and handles errors safely.

The main tests are:

1. **Round-trip test:** Encrypt a sample file and then decrypt it using the correct key. The decrypted content should match the original file exactly.
2. **Wrong-key test:** Try decrypting the encrypted data with an incorrect key. With AES-GCM, authentication should fail, and the program must not accept the result as valid plaintext.
3. **Modified-ciphertext test:** Change part of the encrypted data and attempt decryption. AES-GCM should detect that the data has been altered and reject it.

For example, if a sample text file contains `Training file for AES testing`, a successful round-trip test should produce exactly the same text after decryption.

AES-GCM provides both encryption and authentication. This means it helps protect confidentiality and detect unauthorized changes to encrypted data.

## Practical Work and Tools

- **What I actually did:** I reviewed the three main test cases for the AES project and studied what the expected results should be. I have not confirmed that I executed these tests on Kali Linux, so I am not claiming that they were run.
- **Tools actually used:** Kali Linux is the training environment. Python and the AES-GCM library are relevant to the project, but I have not confirmed using them to execute today's tests.
- **Evidence:** No test screenshots, test output, or commit have been confirmed.

## Key Takeaways

- A round-trip test checks whether encryption and decryption preserve the original file content.
- A wrong key should cause authentication to fail.
- Modified ciphertext should be detected rather than accepted.
- AES-GCM uses authentication to help detect tampering.
- **Important lesson:** Never treat decrypted data as valid unless authentication succeeds.

## Challenges and Questions

One important challenge is understanding how the program reports authentication failures. I also want to review how to compare the original file with the decrypted file and how to make sure a failed decryption does not leave behind an incomplete or misleading output file.

## Reflection

Today I learned that testing is an essential part of building a reliable encryption project. The round-trip test checks normal operation, while wrong-key and modified-ciphertext tests check whether the program rejects invalid data. I want to review Python testing methods and practise these cases with sample files in an authorized local environment.

## Safety

Only test systems and files that I own or have explicit permission to assess. Use sample data, protect encryption keys, and never include passwords, keys, personal information, or private system details in GitHub screenshots or commits.
