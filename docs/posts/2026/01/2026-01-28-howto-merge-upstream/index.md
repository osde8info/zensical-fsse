---
title: "howto merge upstream pull requests to your fork"
date: 2026-01-28
categories: 
  - "fsse"
---

howto merge upstream pull requests to your fork

```
# Make sure you have upstream set 

git remote add upstream https://github.com/ORIGINAL_OWNER/REPO.git 

# Fetch the PR (replace 123 with PR number) 

git fetch upstream pull/123/head:pr-123 

# Switch to the new branch git checkout pr-123

git push origin pr-123

# merge upstream pr into your fork

git checkout main
git merge pr-123
git push origin main

```
