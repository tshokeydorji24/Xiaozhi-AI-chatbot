# Git Commands — XiaoZhi AI Chatbox

## First-time setup (if not already done)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

## Initialize and push to GitHub (new repo)

# 1. Go into your project folder
cd path/to/xiaozhi-ai-chatbox

# 2. Initialize git
git init

# 3. Add all files
git add .

# 4. First commit
git commit -m "Initial commit: XiaoZhi AI Chatbox XiaoZhi + Custom Face UI"

# 5. Link to your GitHub repo (replace with your actual URL)
git remote add origin https://github.com/your-username/xiaozhi-ai-chatbox.git

# 6. Push to GitHub
git branch -M main
git push -u origin main

---

## Day-to-day commands

# Check what files have changed
git status

# Stage all changes
git add .

# Commit with a message
git commit -m "Your message here"

# Push to GitHub
git push

---

## Useful extras

# See commit history
git log --oneline

# Undo last commit (keeps changes)
git reset --soft HEAD~1

# Pull latest from GitHub
git pull origin main
