# DevOps Daily Git & GitOps Workflow Sheet

This is a complete guide for DevOps engineers to use Git in daily development, CI/CD, and Kubernetes (AKS) GitOps workflows, with use cases for each command.

---

## 1️⃣ Branching Workflow (Feature / Hotfix / Main)

**Branches:**
- `main` → production ready
- `develop` → integration / staging
- `feature/*` → new feature
- `hotfix/*` → urgent production fix

**Commands & Use Cases:**
```bash
git branch          # List all local branches - useful to see current working branches
git branch -a       # List all branches (local + remote) - check all branches before merging
git checkout -b feature-login   # Create & switch to a new feature branch - start a new task
git checkout main               # Switch to main branch - ready for deployment or merge
git merge feature-login         # Merge feature into main - finalizing feature work
git checkout feature-login      # Switch back to feature branch - continue development
git fetch origin                # Get latest remote updates - keep branch updated
git rebase origin/develop       # Rebase feature branch onto develop - clean commit history
git checkout hotfix/urgent-fix
git cherry-pick <commit-id>     # Apply specific commit to current branch - hotfix or patch
```

---

## 2️⃣ Commit & Stage Best Practices

```bash
git add <file>               # Stage a file for commit - include specific changes
git add .                     # Stage all changes - quick commit preparation
git commit -m "feat: add login endpoint"   # Commit staged changes with message
git commit --amend            # Modify last commit - fix message or add forgotten changes
git reset <file>              # Unstage a file - remove mistakenly staged file
git reset --soft HEAD~1       # Undo last commit but keep staged - tweak commit before push
git revert <commit-id>        # Safely revert a commit - undo mistakes without rewriting history
git stash                     # Temporarily save uncommitted changes - switch context quickly
git stash list                # List all stashed changes - track multiple stashes
git stash apply               # Apply last stash - continue work later
git stash pop                 # Apply & remove last stash - restore changes to working branch
```

---

## 3️⃣ Remote & CI/CD Commands

```bash
git remote -v                 # Show configured remotes - check remote connections
git fetch origin               # Fetch latest remote changes - update local references
git pull                       # Fetch + merge - update current branch with remote
git push                       # Push local commits to remote - share work
git push -u origin feature-login   # Push branch and set upstream - simplify future pushes
git push --force-with-lease    # Safe force push - overwrite remote safely if necessary
git tag -a v1.0.0 -m "Release"  # Tag a release - mark version for deployment
git push origin v1.0.0         # Push tag to remote - share release with team
```

---

## 4️⃣ Git History & Debugging

```bash
git log --oneline --graph --all   # Compact visual commit history - quick overview
git log -p                        # Show full commit diffs - detailed review
git diff                           # Show unstaged changes - inspect modifications
git show <commit-id>               # Show specific commit details - review code changes
git reflog                          # Check commit history including HEAD moves - recover lost commits
```

---

## 5️⃣ Stash / Temporary Save Commands

```bash
git stash          # Temporarily save uncommitted changes - switch branch safely
git stash list     # Show stashed changes - track multiple stashes
git stash apply    # Apply last stash - continue previous work
git stash pop      # Apply & remove stash - restore changes and clean stash
git stash drop     # Delete a stash - clean unused stashes
```

---

## 6️⃣ Undo / Fix Commands

```bash
git reset --hard HEAD       # Reset all changes to last commit - discard uncommitted work
git checkout -- <file>      # Discard local file changes - revert to last committed state
git reflog                   # Recover lost commits - safety net for mistakes
```

---

## 7️⃣ GitOps / AKS Integration (FluxCD Example)

```bash
git checkout feature/deploy-update
vim deployment.yaml
git add deployment.yaml
git commit -m "feat: update replicas for nginx deployment"
git push origin feature/deploy-update
# Open PR → merge to main → FluxCD auto-syncs to AKS cluster
```
**Use Case:** Update Kubernetes deployment via GitOps; ensures cluster changes are versioned and auditable.

---

## 8️⃣ Hotfix / Production Patch Workflow

```bash
git checkout main
git checkout -b hotfix/critical-issue
vim service.py
git add .
git commit -m "fix: handle null pointer exception"
git checkout main
git merge hotfix/critical-issue
git push origin main
git checkout develop
git merge hotfix/critical-issue
git push origin develop
```
**Use Case:** Quickly fix urgent production issues without affecting ongoing development in develop branch.

---

## 9️⃣ Aliases for Faster Commands

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.hist "log --oneline --graph --all"
```
**Use Case:** Speed up frequent commands for efficiency during development and production troubleshooting.

---

## 💡 DevOps Git Best Practices & Tips

- Always work on feature/hotfix branches
- Commit frequently with small changes
- Rebase your branch to keep history clean
- Use Pull Requests for review & approvals
- Stash changes when switching context
- Use tags for production releases & rollback
- Keep secrets outside Git (Key Vault / env variables)
- Always check `git status` before pushing
- Use clear, descriptive branch and commit names

---

## 🔟 Daily Workflow Example

```text
1. git fetch origin
2. git checkout feature/login
3. git rebase origin/develop
4. git add .
5. git commit -m "feat: add login endpoint"
6. git push origin feature/login
7. Open PR → code review
8. Merge → triggers CI/CD pipeline → deploy to AKS
```
**Use Case:** Standard daily workflow to ensure local changes are integrated cleanly with CI/CD pipelines and GitOps deployment.

---

**Summary:**
This sheet contains all essential Git commands, workflows, use cases, and DevOps tips for daily development, CI/CD, and GitOps with AKS. Following this consistently will take you from Git beginner → DevOps Git Hero 🚀