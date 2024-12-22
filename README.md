# Genesys-git-masterclass


# Version Control and Git Basics

## What is Version Control?
Version control is a system that helps you manage changes to files over time. It allows you to:
- Track the history of changes.
- Collaborate with others effectively.
- Revert to previous versions if needed.

## Git vs. GitHub

| **Aspect**    | **Git**                                   | **GitHub**                              |
|---------------|------------------------------------------|-----------------------------------------|
| Definition    | Git is a distributed version control system for tracking changes in source code. | GitHub is a web-based platform for hosting and managing Git repositories. |
| Purpose       | Helps you manage and track changes locally. | Enables collaboration, hosting, and sharing of repositories. |
| Usage         | Command-line tool installed on your computer. | Cloud-based platform accessed via a browser or Git CLI. |

---

## Alternatives to GitHub
Here are three popular alternatives to GitHub:
1. **GitLab**: Provides integrated DevOps tools and a focus on CI/CD pipelines.
2. **Bitbucket**: Designed for teams, offering integration with Jira and Trello.
3. **SourceForge**: A long-standing platform for hosting open-source projects.

---

## Git Commands Explained

### Difference Between `git fetch` and `git pull`

| **Command**    | **Description**                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------|
| `git fetch`    | Downloads changes from the remote repository but does not apply them to your local branch.       |
| `git pull`     | Combines `git fetch` and `git merge`, downloading and immediately applying changes to your branch. |

**Use Case:** Use `git fetch` when you want to review changes before integrating them, and `git pull` for immediate updates.

---

### Git Rebase

#### Simple Explanation:
Rebasing is like rewriting history to create a cleaner commit timeline. Instead of merging, it places your changes "on top" of another branch.

#### Common Command:
```bash
git rebase <branch_name>
```
**Example:** Rebase your feature branch onto the main branch:
```bash
git checkout feature-branch
git rebase main
```

#### Key Points:
- Helps maintain a linear commit history.
- Can make collaboration more organized but should be used carefully, especially in shared branches.

---

### Git Cherry-pick

#### Simple Explanation:
Cherry-picking allows you to take a specific commit from one branch and apply it to another without merging the entire branch.

#### Common Command:
```bash
git cherry-pick <commit_hash>
```
**Example:** Apply a commit from the main branch to your current branch:
```bash
git checkout feature-branch
git cherry-pick abc1234
```

#### Key Points:
- Useful for selectively applying fixes or features.
- Always review the changes to ensure compatibility.

---

