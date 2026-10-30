# Day 32 — Git and GitHub

**Environment:** Kali Linux

## Topics
- **Main topic:** Git and GitHub
- **Focus:** Repositories, commits, version history

## Learning Notes

Today I studied how Git and GitHub help manage project files and track changes.

**Git** is a version-control system. It records changes to files so developers can review previous versions and understand how a project has developed.

**GitHub** is an online platform where Git repositories can be stored and shared.

Important concepts:

1. **Repository:** A project folder that Git tracks, including its files and version history.
2. **Commit:** A saved snapshot of changes, accompanied by a message describing what changed.
3. **Version history:** A record of previous commits that helps track project development.
4. **README file:** A document that explains the project's purpose, contents, and usage.
5. **`.gitignore`:** A file that tells Git which untracked files or folders to leave out of version control.

For example, in my AES encryption project, separate commits could document adding the encryption feature, adding decryption, and improving error handling.

Some useful Git commands include:

```bash
git status
git add README.md
git commit -m "Update project documentation"
git log --oneline
```

These are reference examples. They show how to check repository status, stage a file, create a commit, and review commit history. I am not claiming to have executed them today.

## Practical Work and Tools

- **What I actually did:** I studied repositories, commits, version history, and how GitHub can organize my cybersecurity training project. I have not confirmed creating a repository, making commits, or pushing files today.
- **Tools actually used:** Kali Linux is the training environment. Git and GitHub were the main technologies studied, but I have not confirmed using their commands today.
- **Evidence:** No GitHub repository link, screenshot, command output, or commit has been confirmed for today's session.

## Key Takeaways

- Git tracks changes to project files.
- GitHub provides a platform for hosting and sharing Git repositories.
- Commits create useful checkpoints in a project's history.
- A README helps other people understand a project.
- `.gitignore` helps prevent unwanted files from being added to a repository.
- **Important lesson:** Never commit passwords, encryption keys, private files, or other secrets. Adding a file to `.gitignore` does not automatically remove it if Git is already tracking it.

## Challenges and Questions

One challenge is understanding the difference between saving a file, staging a change, committing it, and pushing it to GitHub. I also want to review how to check commit history and organize project folders clearly.

## Reflection

Today I learned how Git and GitHub support organized project development. Repositories keep project files together, commits record changes, and version history makes it easier to follow progress. I want to practise the basic Git workflow and improve the documentation of my AES project.

## Safety

Only upload project files that are safe to share. Never publish passwords, encryption keys, personal data, private system details, or confidential files. Check repository contents before making them public.
