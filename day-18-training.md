
# Day 18 — Web Security Basics

**Environment:** Kali Linux  
**Main Topic:** Web Security Basics  
**Focus:** Input Validation, Sessions, and Access Control

## 1. Learning Notes

Today I learned about basic web security and how websites protect information and user accounts.

Three important concepts are:

**1. Input Validation**

Input validation means checking information entered by users before an application processes it. It helps prevent unexpected or harmful input from causing problems.

Examples:
- Checking that an email address follows an expected format.
- Making sure required fields are not empty.
- Limiting the length of user input.
- Validating data on the server, not just in the browser.

**2. Sessions**

A session helps a website remember a user's activity after they sign in. Websites commonly use session identifiers, often stored in cookies, to associate requests with a logged-in user.

Important security practices include:
- Using HTTPS to protect data in transit.
- Keeping session identifiers private.
- Expiring inactive sessions.
- Creating a new session after authentication.
- Logging out properly and invalidating the session.

**3. Access Control**

Access control determines what a user is allowed to view or do within an application.

For example:
- A normal user may view their own profile.
- An administrator may manage user accounts.
- A user should not be able to access another person's private information simply by changing a URL or record identifier.

A useful principle from my earlier training is **least privilege**: users should receive only the permissions they need.

## 2. Practical Work and Tools

**What I actually did:**  
I studied the basic concepts of web security, including input validation, session management, and access control. I have not confirmed performing practical web application testing.

**Tools actually used:**  
No specific web security testing tools are confirmed for this session. Kali Linux was the learning environment.

**Evidence:**  
These learning notes serve as documentation. No practical screenshots, test results, or commits are confirmed.

## 3. Key Takeaways

- Input validation helps ensure that applications process expected data.
- Session management protects the relationship between a user and their logged-in account.
- Access control prevents users from accessing resources without permission.
- HTTPS helps protect information while it travels between a browser and a website.
- Server-side checks are important because browser-side validation alone is not sufficient.
- The principle of least privilege helps limit the impact of unauthorized access.

**Important lesson:** Never assume that hiding a page or button in the browser is enough to protect it. The server must verify permissions for every protected action.

## 4. Challenges and Questions

One concept I want to understand better is how websites securely manage sessions and check permissions behind the scenes.

Questions for further study:
- What makes a session cookie secure?
- Why is server-side input validation necessary?
- How do websites prevent users from accessing another user's records?
- What is the difference between authentication and authorization?

## 5. Reflection

Today I learned that web security involves protecting both user input and user accounts. Input validation helps applications handle information safely, sessions help maintain secure login states, and access control ensures that users can only perform permitted actions.

I want to review how secure cookies work and understand how websites check permissions on the server. These concepts will help me understand how secure web applications are designed.

## 6. Safety

All cybersecurity learning and testing must take place on systems I own or have explicit permission to assess. I will use intentionally vulnerable practice applications only in authorized environments. I will never include passwords, session tokens, API keys, personal data, or private system details in my GitHub repository.
