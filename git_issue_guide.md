
# GitHub Issues Guide

This document explains how to create, manage, and close GitHub Issues effectively.

---

## What is a GitHub Issue?
GitHub Issues are used to:
- Track bugs 🐞
- Request new features ✨
- Discuss improvements or tasks 📌
- Manage project work transparently

---

## Step 1: Navigate to Issues Tab
1. Open your repository on GitHub.
2. Click on the **Issues** tab.
3. Click **New issue**.

---

## Step 2: Create a New Issue
1. Enter a **Title** (short and clear).
2. Add a **Description** including:
   - Problem or requirement
   - Expected behavior
   - Actual behavior (for bugs)
   - Screenshots or logs (if available)
3. Click **Submit new issue**.

---

## Step 3: Issue Best Practices
- Use clear and descriptive titles
- One issue = one task/bug
- Add steps to reproduce (for bugs)
- Mention related PRs or issues using `#issue-number`
- Use Markdown formatting for readability

---

## Step 4: Labels
Labels help categorize issues:
- `bug` – Something is not working
- `enhancement` – New feature request
- `documentation` – Docs related work
- `help wanted` – Extra help needed
- `good first issue` – Beginner-friendly

Assign labels while creating or editing an issue.

---

## Step 5: Assigning Issues
- Assign issues to yourself or team members.
- Helps track ownership and responsibility.

---

## Step 6: Issue Status Tracking
- **Open** – Issue is active
- **In Progress** – Being worked on
- **Closed** – Issue resolved or no longer valid

(Projects or boards can be used for advanced tracking)

---

## Step 7: Linking Issues with Pull Requests
1. Mention issue number in PR description:
   ```
   Fixes #12
   Closes #15
   ```
2. Issue will auto-close when PR is merged.

---

## Step 8: Closing an Issue
- Close manually if resolved without PR.
- Or auto-close via merged PR using keywords:
  - `Fixes`
  - `Closes`
  - `Resolves`

---

## Common Keywords for Auto-Close
- Fixes #issue-number
- Closes #issue-number
- Resolves #issue-number

---

## Tips
- Keep issues small and actionable
- Update issue comments with progress
- Avoid duplicate issues
- Reference commits and PRs when possible

---

## Resources
- https://docs.github.com/en/issues
- https://guides.github.com/features/issues/

---