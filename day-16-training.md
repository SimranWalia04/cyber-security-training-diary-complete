# Day 16 — Access Control

**Environment:** Kali Linux

## Topics
- **Main Topic:** Access Control
- **Focus:** Principle of Least Privilege and Access Rights

## Learning Notes

Access control is a security method used to decide who can access computer systems, files, applications, and other resources. It ensures that users can only perform actions they are authorized to do.

### 1. Principle of Least Privilege

The principle of least privilege means giving each user or application only the minimum permissions needed to complete its tasks.

For example, a normal user who only needs to read a document should not automatically receive permission to modify or delete it.

Benefits include:
- Reducing unauthorized access.
- Preventing accidental changes or deletion.
- Limiting damage if an account is compromised.
- Improving overall system security.

### 2. Access Rights

Access rights define what actions a user can perform on a resource.

In Linux, common file permissions include:

- **Read (r):** Allows viewing file contents.
- **Write (w):** Allows modifying file contents.
- **Execute (x):** Allows executing a file or accessing a directory.

Permissions are assigned to three categories:

1. Owner – The user who owns the file.
2. Group – Users belonging to the file's group.
3. Others – All other users.

For example, permission value `644` means:
- Owner: Read and write.
- Group: Read only.
- Others: Read only.

### 3. Access Control Methods

Common access control models include:

- **Discretionary Access Control (DAC):** Resource owners can decide who receives access.
- **Mandatory Access Control (MAC):** Access is controlled through centrally defined security policies.
- **Role-Based Access Control (RBAC):** Permissions are assigned according to a user's role.

For example, in an organization, an administrator may have more system permissions than an ordinary employee.

### 4. Linux Commands for Access Inspection

Some useful Linux commands include:

- `whoami` – Displays the current username.
- `groups` – Displays the groups associated with the current user.
- `ls -l` – Shows file permissions and ownership.
- `id` – Displays user and group identification information.

## Practical Work and Tools

- **What I actually did:** Studied access control, least privilege, Linux file permissions, and common access control models. Specific permission-management exercises have not been confirmed.
- **Tools actually used:** Kali Linux environment. No additional access-control tools are confirmed.
- **Evidence:** Learning notes describing file access rights, user permissions, and the principle of least privilege.

## Key Takeaways

- Access control determines who can access resources and what they can do.
- Least privilege reduces unnecessary permissions.
- Linux uses read, write, and execute permissions.
- Permissions apply to owners, groups, and others.
- RBAC assigns permissions based on job roles.
- Access rights should be reviewed regularly.

**Commands to remember:**

```bash
whoami
id
groups
ls -l
```

## Challenges and Questions

I am still learning the differences between DAC, MAC, and RBAC. I also want to understand how Linux administrators assign permissions safely and how access rights are reviewed when users change roles.

## Reflection

Today, I learned about access control and how it protects files, applications, and systems from unauthorized use. I understood that the principle of least privilege means providing only the permissions necessary for a task. I also learned about Linux read, write, and execute permissions and different access control models. I want to review these models and practise inspecting file permissions in my own Kali Linux training directory.

## Safety

Only test systems I own or have explicit permission to assess. I will avoid changing permissions on important system files, follow the principle of least privilege, and never include passwords, keys, personal data, or private system details in my training diary.
