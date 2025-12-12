# first-demo
First git repo.
<br>
Author - Prakash Bhanu (PKInnovate)<br>

# 🚀 Git Commands & Python Virtual Environment Guide

## 📌 First Time Git Setup
Configure your Git identity:
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Clone a Repository
```bash
git clone https://github.com/username/repo.git
```

Add Files to Staging
```
git add filename
git add .
```

Save / Commit Changes
```
git commit -m "your commit message"
```

Push to GitHub
```
git push -u origin main
git push
```

Connect Local Project to GitHub (Add Remote)
```
git remote add origin https://github.com/username/repo.git
```

Real-World Daily Workflow
```
git pull
git add .
git commit -m "Updated module"
git push
```

Create a New Repository From Terminal
```
echo "# localrepo" >> README.md
git init
git remote add origin <repo-link>
git remote -v
git branch
git branch -M main

git add README.md
git commit -m "first commit"
git push -u origin main
```

Branch Commands
```
git checkout
git branch -M main
git checkout <branch-name>
git checkout -b <new-branch-name>
git branch -d <branch-name>**
```

Merge & Compare Branches

```
git diff <branch-name>      # Compare branches or files
git merge <branch-name>     # Merge branch

```

Fix “Updates Were Rejected” (Safe Method)
```
git pull --rebase origin main
git push origin main
```
If merge conflicts happen:
```
git add .
git rebase --continue
git push origin main
```
Force push (⚠️ overwrites remote history):
```
git push --force origin main
```

🐍 Python Virtual Environment Setup (For ML / Battery Research)
1️⃣ Create Virtual Environment
```
python -m venv venv
```

2️⃣ Activate Virtual Environment
macOS / Linux
```
source venv/bin/activate
```
Windows (Command Prompt)
```
venv\Scripts\activate
```
Windows (PowerShell)
```
.\venv\Scripts\Activate.ps1
```
3️⃣ Check Installed Packages
```
pip list
```
4️⃣ Install Useful Libraries
```
pip install numpy pandas matplotlib scikit-learn python-dotenv jupyter
```
5️⃣ Save Dependencies
```
pip freeze > requirements.txt
```

Recreate on another system:
```
pip install -r requirements.txt
```
6️⃣ Ignore Virtual Environment in Git
```
echo "venv/" >> .gitignore
git add .gitignore
git commit -m "Ignore venv folder"
```
7️⃣ Deactivate Environment
```
deactivate
```
8️⃣ Optional – Use .env in Python
```
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("API_KEY")
```
✅ Quick Checklist
```
[✔] python -m venv venv — created
[✔] activate venv — done
[✔] pip install — installed
[✔] requirements.txt — saved
[✔] venv/ added to .gitignore
[✔] deactivate — when don
```
