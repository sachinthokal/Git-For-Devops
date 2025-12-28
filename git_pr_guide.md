
# Git Pull Request (PR) Guide

This guide explains how to create a Pull Request (PR) using Git and GitHub.

---

## Step 1: Fork or Clone the Repository
1. **Fork** the repository if you don't have write access.
2. **Clone** the repository to your local machine:

```bash
git clone https://github.com/username/repo.git
cd repo
```

---

## Step 2: Create a New Branch
1. Always create a new branch for your feature or bug fix.
2. Naming convention suggestion: `feature/branch-name` or `bugfix/branch-name`.

```bash
git checkout -b feature/my-new-feature
```

---

## Step 3: Make Changes Locally
1. Edit, add, or delete files as required.
2. Stage the changes:

```bash
git add .
```

3. Commit the changes with a descriptive message:

```bash
git commit -m "Add feature X to improve Y"
```

---

## Step 4: Push Changes to Remote
Push your branch to your GitHub repository:

```bash
git push origin feature/my-new-feature
```

---

## Step 5: Open a Pull Request on GitHub
1. Go to your fork or the original repository on GitHub.
2. Click **Compare & Pull Request** next to your branch.
3. Fill in PR details:
   - Title: Clear and descriptive
   - Description: Explain what changes you made and why
   - Assign reviewers if needed
4. Click **Create Pull Request**.

---

## Step 6: Review Process
1. Reviewers will check your code.
2. You might be asked to make changes.
3. Make the changes locally, commit, and push again:

```bash
git add .
git commit -m "Update based on review comments"
git push origin feature/my-new-feature
```

4. The PR will update automatically.

---

## Step 7: Merge the Pull Request
1. Once approved, the PR can be merged by:
   - **Squash and merge** (recommended for cleaner history)
   - **Merge commit**
   - **Rebase and merge**
2. After merging, delete your branch to keep the repo clean.

---

## Step 8: Update Your Local Repository
After the PR is merged, update your local `main` branch:

```bash
git checkout main
git pull origin main
```

---

## Tips
- Keep your PRs small and focused.
- Write clear commit messages.
- Pull the latest changes from `main` before starting work.
- Use descriptive branch names.
- Rebase frequently if multiple people are working on the repo.

---

## Resources
- [Git Official Site](https://git-scm.com/)
- [GitHub Docs - Pull Requests](https://docs.github.com/en/pull-requests)
