# Push document-analyzer to GitHub

To push this skill to your GitHub repository, follow these steps:

## Step 1: Navigate to your skills directory
```bash
cd ~/Claude/Skills
```

## Step 2: Initialize git and add the skill
```bash
# If this isn't already a git repo:
git init

# Add the document-analyzer skill
git add document-analyzer/

# Commit
git commit -m "Add document-analyzer skill for document summarization"
```

## Step 3: Add your GitHub remote and push
```bash
# Add your GitHub repo as remote
git remote add origin https://github.com/olesund1/Metria-test-repo.git

# Push to main branch
git push -u origin main
```

## Step 4: Verify
Check your GitHub repo at: https://github.com/olesund1/Metria-test-repo

---

**Alternative: If you already have a local git repo with a different remote:**

```bash
cd ~/Claude/Skills
git add document-analyzer/
git commit -m "Add document-analyzer skill"
git push
```

That's it! Your skill will be live on GitHub.
