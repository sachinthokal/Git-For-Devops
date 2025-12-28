# Git Setup Guide for New Users (Zero to Hero)

This guide will take a new user from zero knowledge of Git to being ready to use Git professionally in DevOps workflows.

---

## 1️⃣ Install Git

### Windows:
1. Download Git: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Run the installer and follow defaults.
3. Verify installation:
```bash
git --version
```

### MacOS:
```bash
brew install git   # if Homebrew is installed
```

### Linux (Ubuntu/Debian):
```bash
sudo apt update
sudo apt install git -y
git --version
```

---

## 2️⃣ Configure Git

Set your username and email (used in commits):
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
Verify configuration:
```bash
git config --list
```

---

## 3️⃣ Set Default Editor

Set your preferred text editor for Git (example: VS Code):
```bash
git config --global core.editor "code --wait"
```

---

## 4️⃣ Initialize a Repository

### Create a new project:
```bash
mkdir my-project
cd my-project
git init
```

### Clone an existing repository:
```bash
git clone https://github.com/username/repo.git
```

---

## 5️⃣ SSH Key Setup for GitHub/GitLab

1. Generate SSH key:
```bash
ssh-keygen -t ed25519 -C "youremail@example.com"
```
- Press Enter to accept default file location
- Optionally, add a passphrase for security

2. Start the SSH agent and add your key:
```bash
# Start agent
eval "$(ssh-agent -s)"
# Add key
ssh-add ~/.ssh/id_ed25519
```

3. Copy the public key:
```bash
cat ~/.ssh/id_ed25519.pub
```
- Copy the output and add it to your GitHub/GitLab SSH keys in account settings

4. Test SSH connection:
```bash
ssh -T git@github.com
```
- You should see a success message

**Use Case:** SSH key allows secure password-less connection to Git remotes.

---

## 6️⃣ Basic Workflow

1. Check status:
```bash
git status
```
2. Add files to stage:
```bash
git add <file>
git add .    # add all files
```
3. Commit changes:
```bash
git commit -m "Initial commit"
```
4. Connect to remote:
```bash
git remote add origin git@github.com:username/repo.git
```
5. Push changes:
```bash
git push -u origin main
```

---

```

**Tips for New Users:**
- Commit small changes frequently
- Always pull/fetch before starting work
- Use branches for features and fixes
- Keep commit messages clear and descriptive
- Learn to recover using `reflog` and `stash`

---
```
By following this guide, a beginner can set up Git, configure SSH for secure access, manage repositories, and confidently work on professional DevOps projects.

