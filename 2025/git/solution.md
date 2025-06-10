# Week 4 Challenge: Git & GitHub Basics

## 🔧 Task 1–4 Git Commands Used


## Git Commands Used:
- `git clone`
- `git init`
- `git add`
- `git commit`
- `git branch`
- `git switch`
- `git push`
- `git log`
- `git remote set-url`


```bash
# Forked and cloned the repository
git clone https://github.com/Nidhi-kumarii/90DaysOfDevOps.git
cd 2025/git/01_Git_and_Github_Basics

# Created challenge directory and initialized Git repo
mkdir week-4-challenge
cd week-4-challenge
git init

# Created and committed a new file
echo "My name is Nidhi Kumari. I am learning DevOps!" > info.txt
git add info.txt
git commit -m "Initial commit: Add info.txt with introductory content"

# Configured remote with Personal Access Token (PAT)
git remote add origin https://<username>:<PAT>@github.com/Nidhi-kumarii/90DaysOfDevOps.git
# or if it already exists
git remote set-url origin https://<username>:<PAT>@github.com/Nidhi-kumarii/90DaysOfDevOps.git

# Pushed the local commit to GitHub
git push -u origin master

# Checked commit history
git log

```
commit 040eafab140659dde273a56dda01f3df211365ff (HEAD -> master, orgin/master)
Author: Nidhi-kumarii <ns4732900@gmail.com>
Date:   Tue Jun 10 08:58:41 2025 +0000
```
    I

```
## Why Branching Strategies Are Important
Branching is a powerful feature of Git that allows developers to work on different parts of a project independently. Here’s why branching strategies matter:

 1. Isolating Features and Bug Fixes
Branches allow developers to work on features or bug fixes in isolation from the main codebase. This prevents half-done code or bugs from affecting the main product

2. Facilitating Parallel Development
Multiple developers or teams can work on different branches simultaneously without interfering with each other's work — speeding up development.

3. Reducing Merge Conflicts
Structured branching (like feature/, bugfix/, release/) helps avoid code conflicts and keeps changes organized.

4.Enabling Effective Code Reviews
Pull Requests (PRs) from feature branches make it easier for reviewers to see what changed and give feedback before merging into main or master.


Common  Branching Strategies


| Strategy        | Purpose                                     |
| --------------- | ------------------------------------------- |
| `main`/`master` | Stable production-ready code                |
| `develop`       | Integration branch for feature branches     |
| `feature/*`     | For developing new features                 |
| `bugfix/*`      | For fixing small issues                     |
| `hotfix/*`      | Urgent fixes for production                 |
| `release/*`     | Pre-release final testing and prep branches |

