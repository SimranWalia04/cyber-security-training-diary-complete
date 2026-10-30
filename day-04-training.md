# Day 04 — File Management

**Environment:** Kali Linux

## Topics
- **Main Topic:** File Management
- **Focus:** `mkdir`, `cp`, `mv`, `cat`, and `less`

## Learning Notes

File management in Linux involves creating directories, copying files, moving or renaming files, and viewing their contents. These operations help keep the filesystem organized.

The following commands are useful for basic file management:

1. **`mkdir`** – Creates a new directory.  
   Example: `mkdir Training` creates a folder named `Training`.

2. **`cp`** – Copies files or directories.  
   Example: `cp notes.txt backup.txt` creates a copy of `notes.txt` named `backup.txt`.

3. **`mv`** – Moves or renames files and directories.  
   Example: `mv notes.txt old_notes.txt` renames the file.

4. **`cat`** – Displays the contents of a file in the terminal.  
   Example: `cat notes.txt` displays the contents of `notes.txt`.

5. **`less`** – Opens a file for scrolling through its contents.  
   Example: `less notes.txt` is useful for reading longer files. Press `q` to exit.

These commands make it easier to organize information and work with files through the Linux terminal.

## Practical Work and Tools

- **What I actually did:** Studied the purpose and basic syntax of Linux file-management commands. Specific hands-on activities have not been confirmed.
- **Tools actually used:** Kali Linux terminal, if used during the session. No additional tools are confirmed.
- **Evidence:** Notes about creating directories, copying and renaming files, and viewing file contents. A sanitized screenshot can be added if available.

## Key Takeaways

- `mkdir` creates directories.
- `cp` makes copies without removing the original file.
- `mv` moves or renames files.
- `cat` displays file contents directly.
- `less` allows longer files to be read page by page.
- It is important to check filenames and destinations before copying or moving files.

**Commands to remember:**

```bash
mkdir Training
cd Training
cat > notes.txt
less notes.txt
cp notes.txt backup.txt
mv backup.txt old_notes.txt
ls
```

When `cat > notes.txt` is entered, type some practice text and press `Ctrl+D` to save and finish input. The example commands create and modify files in the `Training` directory.

## Challenges and Questions

I am still learning the difference between copying and moving files. I also want to understand how to manage directories containing multiple files and how to avoid accidentally overwriting important information.

## Reflection

Today, I learned about basic Linux file-management commands and how they help organize files and directories. I understood that `mkdir` creates folders, `cp` copies files, `mv` moves or renames them, and `cat` and `less` help read file contents. I want to practise these commands in a dedicated training folder and review how to handle files safely without losing important data.

## Safety

Only test systems I own or have explicit permission to assess. I will practise file operations in a dedicated training directory, check destinations before moving or copying files, and never include passwords, keys, personal data, or private system details.

