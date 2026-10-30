# Day 05 — Users and Permissions

**Environment:** Kali Linux

## Topics
- **Main Topic:** Users and Permissions
- **Focus:** Users, Groups, Ownership, and `chmod`

## Learning Notes

Linux is a multi-user operating system. This means multiple user accounts can access the same computer while having different permissions.

Users and groups help control who can access files and directories.

1. **Users:** Each user has an account with a username and permissions. The command `whoami` displays the current username.

2. **Groups:** Groups allow administrators to assign permissions to multiple users together. The command `groups` displays the groups associated with the current user.

3. **Ownership:** Every file and directory has an owner and an associated group. The command `ls -l` displays ownership and permission information.

4. **File permissions:** Linux uses three main permission types:
   - `r` – Read: allows viewing file contents.
   - `w` – Write: allows modifying file contents.
   - `x` – Execute: allows running a file or accessing a directory.

Permissions are generally displayed for three categories:
- Owner: the user who owns the file.
- Group: users belonging to the associated group.
- Others: everyone else.

**The `chmod` command** changes file permissions.

For example:

```bash
chmod 644 notes.txt
```

This gives the owner read and write permissions, while the group and others receive read-only permission.

Another example:

```bash
chmod 755 script.sh
```

This gives the owner read, write, and execute permissions, while the group and others receive read and execute permissions.

## Practical Work and Tools

- **What I actually did:** Studied Linux users, groups, file ownership, and permission categories. Specific permission-changing exercises have not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional tools are confirmed.
- **Evidence:** Notes explaining read, write, and execute permissions, along with examples of `chmod` and `ls -l`.

## Key Takeaways

- Linux uses users and groups to manage access.
- Every file has an owner and an associated group.
- Read, write, and execute are the three basic permission types.
- `ls -l` displays file permissions and ownership.
- `chmod` changes file permissions.
- Permissions should follow the principle of least privilege: users should receive only the access they need.

**Commands to remember:**

```bash
whoami
groups
ls -l
chmod 644 notes.txt
```

## Challenges and Questions

I am still learning how numerical permissions work and how values such as `644` and `755` represent different access levels. I want to understand the difference between changing file permissions and changing file ownership.

## Reflection

Today, I learned how Linux manages users, groups, ownership, and file permissions. I understood that permissions control who can read, modify, or execute files. I also learned that `chmod` can change permissions and that `ls -l` helps inspect them. I want to review numerical permission values and practise changing permissions on files inside my own training directory.

## Safety

Only test systems I own or have explicit permission to assess. I will avoid changing permissions on important system files, use a personal practice directory, and never include passwords, keys, personal data, or private system details.

