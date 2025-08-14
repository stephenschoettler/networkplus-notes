## 💡 Using Source Control (OBJ 1.8)

Source Control's purpose is to track changes to files, especially in team environments. **Git** is the industry standard for code repositories.

✅ **Why use Git (Exam Focus)**
- **Version Control:** Track changes to files over time.
- **Source Control:** Manage code for templates, runbooks, Infrastructure as Code (IaC), and scripts.
- **Collaboration:** Enables multiple team members to work on and merge changes to the same files.

✅ **Basic Git Concepts/Commands (Demonstrated)**
- `git config --global user.name "Your Name"`: Sets global username.
- `git config --global user.email "your@email.com"`: Sets global email.
- `git init [directory]`: Initializes a new Git repository.
- `git status`: Shows current repository state (untracked, modified, staged files).
- `git add [file]`: Stages changes for commit (tells Git to track/include changes).
- `git commit -m "Message"`: Records staged changes to the repository.
- `git log`: Displays commit history.