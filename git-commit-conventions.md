# Git Commit Message Conventions

This document explains the recommended way to write **clean, readable, and maintainable Git commit messages** using the `type(scope): message` pattern.

---

## 1️⃣ Structure

```
type(scope): message
```

- **type** → The kind of change. (Required)  
- **scope** → Optional, the affected module/folder/file.  
- **message** → Short, clear description of the change (lowercase after `:` recommended).  

---

## 2️⃣ Common Types & Usage

| Type      | Example Commit Message                        | When to Use |
|-----------|-----------------------------------------------|-------------|
| `feat`    | `feat(auth): add login API`                   | New feature added |
| `fix`     | `fix(api): correct null pointer bug`          | Bug fix |
| `docs`    | `docs(readme): update setup instructions`    | Documentation changes only |
| `chore`   | `chore: update dependencies`                 | Build/maintenance tasks |
| `refactor`| `refactor(auth): simplify login logic`       | Code restructure, no new features/bugs |
| `test`    | `test(auth): add unit tests for login`       | Adding/modifying tests |
| `style`   | `style(css): fix formatting`                 | Only formatting, no logic changes |

---

## 3️⃣ Scope (Optional)

- Scope helps identify **which part of code is affected**  
- Examples: `auth`, `k8s`, `frontend`, `backend`, `api`  
- Example commit with scope:

```
feat(k8s): remove deployment and service yaml files
```

---

## 4️⃣ Message Guidelines

- **Keep it short** (≈50 characters for title)  
- **Use imperative mood** (like a command)  
- **Describe what changed, not what was done**  

**Imperative examples:**

```
Add login API           ✅
Adds login API          ❌
Fixed bug in login      ❌
Fix login null pointer  ✅
```

---

## 5️⃣ Example Commit Messages

```
feat(auth): add JWT-based login authentication
fix(api): handle null pointer exception in getUser()
docs(readme): update Docker setup instructions
chore: upgrade Node.js to v20
refactor(frontend): simplify dashboard component
test(auth): add unit tests for login API
style(css): fix button alignment on mobile
```

---

## ✅ Summary

- Use `type(scope): message` pattern for clarity  
- Type shows **kind of change** (`feat`, `fix`, `chore`, etc.)  
- Scope (optional) shows **affected module/folder**  
- Message should be **short, clear, imperative**  

Following this convention keeps your **Git history clean, professional, and easy to understand**.
