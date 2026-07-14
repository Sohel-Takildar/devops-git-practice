# Day 28 – Revision Day (Day 1 to Day 27)

## Name
Sohel Takildar

## Date
14 July 2026

---

# Task 1 – Self Assessment Checklist

## Linux

| Topic | Status |
|--------|--------|
| Navigate file system | ✅ Can do confidently |
| Manage processes | ✅ Can do confidently |
| systemd services | ✅ Can do confidently |
| Edit files using vim/nano | ✅ Can do confidently |
| CPU/Memory/Disk troubleshooting | ✅ Can do confidently |
| Linux File System Hierarchy | ✅ Can do confidently |
| Users & Groups | ✅ Can do confidently |
| chmod permissions | ✅ Can do confidently |
| chown/chgrp | ✅ Can do confidently |
| LVM | ⚠ Need to revisit |
| Networking commands | ✅ Can do confidently |
| DNS, IP, Subnet, Ports | ⚠ Need to revisit |

---

## Shell Scripting

| Topic | Status |
|--------|--------|
| Variables & Arguments | ✅ Can do confidently |
| if/else & case | ✅ Can do confidently |
| Loops | ✅ Can do confidently |
| Functions | ✅ Can do confidently |
| grep, awk, sed | ⚠ Need to revisit |
| Error handling | ✅ Can do confidently |
| Crontab | ✅ Can do confidently |

---

## Git & GitHub

| Topic | Status |
|--------|--------|
| Init, Add, Commit | ✅ Can do confidently |
| Branches | ✅ Can do confidently |
| Push/Pull | ✅ Can do confidently |
| Clone vs Fork | ✅ Can do confidently |
| Merge | ✅ Can do confidently |
| Rebase | ✅ Can do confidently |
| Git Stash | ✅ Can do confidently |
| Cherry Pick | ✅ Can do confidently |
| Squash Merge | ⚠ Need to revisit |
| Reset & Revert | ✅ Can do confidently |
| Branching Strategies | ⚠ Need to revisit |
| GitHub CLI | ✅ Can do confidently |

---

# Task 2 – Topics Revisited

## 1. LVM

### Re-learned
- Physical Volume (PV)
- Volume Group (VG)
- Logical Volume (LV)
- Extend and Reduce Storage
- Resize filesystem without data loss

---

## 2. grep / awk / sed

### Re-learned

grep

```bash
grep ERROR app.log
```

awk

```bash
awk '{print $1}'
```

sed

```bash
sed 's/error/success/g'
```

---

## 3. Git Branching Strategies

### Re-learned

- GitFlow
- GitHub Flow
- Trunk Based Development
- When to use each strategy
- Weekly release workflow

---

# Task 3 – Quick Fire Questions

## 1. What does chmod 755 script.sh do?

Owner gets Read, Write, Execute.

Group gets Read and Execute.

Others get Read and Execute.

---

## 2. Difference between Process and Service?

A process is a running program.

A service is a background process managed by systemd.

---

## 3. Find process using port 8080

```bash
sudo ss -tulpn | grep 8080
```

or

```bash
sudo lsof -i :8080
```

---

## 4. What does set -euo pipefail do?

- -e Exit on error
- -u Error on undefined variables
- pipefail Detect pipeline failures

---

## 5. Difference between git reset --hard and git revert

git reset --hard

Removes commits and working directory changes.

git revert

Creates a new commit that undoes previous changes.

---

## 6. Best branching strategy for a team of 5 developers shipping weekly?

GitHub Flow because it is simple, supports pull requests, and works well for frequent releases.

---

## 7. What does git stash do?

Temporarily saves uncommitted work so you can switch branches without committing.

---

## 8. Schedule script every day at 3 AM

```bash
0 3 * * * /home/user/script.sh
```

---

## 9. Difference between git fetch and git pull

git fetch

Downloads new commits only.

git pull

Downloads and merges automatically.

---

## 10. What is LVM?

LVM is Logical Volume Manager.

It allows resizing storage, creating snapshots, and managing disks more flexibly than normal partitions.

---

# Task 4 – Repository Check

- ✅ All Day 1–27 folders available
- ✅ All commits pushed
- ✅ git-commands.md updated
- ✅ Shell Scripting Cheat Sheet completed
- ✅ GitHub Profile updated

---

# Task 5 – Teach It Back

## Explaining Git Branching

Git branching allows developers to work on new features without affecting the main project. Each branch is an independent workspace where changes can be made safely. After testing, the branch is merged back into the main branch using Git. This enables multiple developers to work simultaneously without conflicts and keeps the project organized. Branching is one of Git's most powerful features for collaborative software development.

---

# Revision Summary

During Day 28, I revised everything from Day 1 to Day 27. I reviewed Linux fundamentals, shell scripting, Git & GitHub, GitHub CLI, networking, LVM, permissions, and developer branding. I identified a few weak areas and revised them again. This revision increased my confidence and strengthened my understanding of DevOps fundamentals.
