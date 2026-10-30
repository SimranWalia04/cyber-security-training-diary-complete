# Day-03_Linux-Navigation

**Environment:** Kali Linux

## Topics
- **Main Topic:** Linux Navigation
- **Focus:** `pwd`, `ls`, `cd`, and Filesystem Paths

## Learning Notes

Linux navigation involves moving between directories and understanding how files and folders are organized. In Kali Linux, I can use terminal commands to find my current location, view directory contents, and move through the filesystem.

- **`pwd`** — Displays the full path of the current working directory. Example output might be `/home/student`.
- **`ls`** — Lists the files and directories in the current location. The command `ls -l` displays additional details, such as permissions and file sizes.
- **`cd`** — Changes the current directory. For example, `cd Documents` enters the `Documents` directory if it exists in the current location.
- **Filesystem paths** — Describe where files and directories are located.

There are two common types of paths:

1. **Absolute path:** Starts from the root directory `/`, such as `/home/student/Documents`.
2. **Relative path:** Describes a location in relation to the current directory, such as `Documents`.

The special path `..` refers to the parent directory, so `cd ..` moves up one directory. The shortcut `~` represents the current user's home directory.

## Practical Work and Tools

- **What I actually did:** Studied the purpose of Linux navigation commands and the difference between absolute and relative paths. Specific hands-on practice has not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional tools are confirmed.
- **Evidence:** Notes describing `pwd`, `ls`, `cd`, absolute paths, and relative paths. A sanitized terminal screenshot can be added if available.

## Key Takeaways

- `pwd` identifies my current directory.
- `ls` helps me inspect files and folders.
- `cd` allows me to move between directories.
- Absolute paths start at `/`, while relative paths depend on the current directory.
- The `..` shortcut refers to the parent directory, and `~` represents the home directory.

**Command sequence to remember:**

```bash
pwd
ls
cd Documents
pwd
cd ..
```

The sequence shows how to check a location, list its contents, enter a directory, and return to its parent. The `cd Documents` command works only if that directory exists in the current location.

## Challenges and Questions

I am still learning how relative paths depend on the current directory. I want to practise navigating between folders and understand how to handle directory names containing spaces.

## Reflection

Today, I learned how Linux navigation commands help me move through the filesystem. I understand that `pwd` shows my current location, `ls` lists available files and directories, and `cd` changes locations. I also learned the difference between absolute and relative paths. I want to review directory navigation and practise using paths correctly so that I can work more confidently in the Kali Linux terminal.

## Safety

Only test systems I own or have explicit permission to assess. I will use basic navigation commands carefully and never include passwords, keys, personal data, or private system details in my training diary.

