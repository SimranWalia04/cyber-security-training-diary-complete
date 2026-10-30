# Day 38 — Testing and Evidence
 
**Environment:** Kali Linux

## Topics
- **Main topic:** Testing and Evidence
- **Focus:** Verified results and sanitized screenshots

## Learning Notes

Today I studied why testing and evidence are important in a cybersecurity project.

Testing helps determine whether a project works as expected. Evidence helps document what was tested and what results were observed.

### 1. Verified Results

A result should only be described as successful when it has actually been checked.

For my AES encryption project, useful tests include:

- **Round-trip test:** Check whether decrypting an encrypted sample file restores the original content.
- **Wrong-key test:** Confirm that using an incorrect key causes authentication to fail.
- **Modified-ciphertext test:** Confirm that altered encrypted data is rejected.
- **Missing-file test:** Check whether the program handles an unavailable input file safely.
- **Overwrite test:** Check whether an existing output file is protected from accidental replacement.

### 2. Evidence Collection

Evidence provides a record of work completed during a project.

Examples include:
- Screenshots of terminal output.
- Test results.
- Project source-code files.
- GitHub commit history.
- README documentation.

Evidence should be genuine and should represent the actual work performed.

### 3. Sanitized Screenshots

Before sharing screenshots publicly, sensitive information should be removed or hidden.

Examples of information to protect:
- Passwords and encryption keys.
- Personal information.
- Private file paths or system details.
- Confidential data.
- Access tokens and other credentials.

### 4. Accurate Reporting

It is important to distinguish between a test that was planned, a test that was attempted, and a test that passed.

For example, a planned AES-GCM tampering test should not be described as successful until it has actually been performed and its result checked.

## Practical Work and Tools

- **What I actually did:** I reviewed the types of tests and evidence that could demonstrate the AES project's reliability. I also studied the importance of sanitizing screenshots. I have not confirmed running new tests or capturing screenshots today.
- **Tools actually used:** Kali Linux is the training environment. Python, AES-GCM, Git, and GitHub are relevant to the project, but I have not confirmed using them to collect today's evidence.
- **Evidence:** No new screenshots, verified test results, or GitHub commits have been confirmed.

## Key Takeaways

- Testing helps identify problems before a project is presented.
- Evidence should reflect real activities and actual results.
- Screenshots should be checked for sensitive information before sharing.
- A planned test is not the same as a completed test.
- **Important lesson:** Never claim a test passed unless its result has been verified.

## Challenges and Questions

One challenge is deciding which screenshots and test results provide the clearest evidence without revealing private information. I also want to review how to organize test results so that another person can understand what was tested and whether it passed.

## Reflection

Today I learned that evidence and accurate reporting are important parts of cybersecurity work. Testing helps demonstrate whether the AES project behaves correctly, while sanitized screenshots and clear notes help communicate the results safely. I want to review my project documentation and make sure any results I report are supported by genuine evidence.

## Safety

Only test systems and files that I own or have explicit permission to assess. Never include passwords, encryption keys, personal data, access tokens, or private system details in screenshots, logs, or public GitHub repositories.
