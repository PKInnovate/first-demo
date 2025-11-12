# first-demo
First git repo.
<br>
Author - Prakash Bhanu (PKInnovate)<br>
<h> Git Commands </h>
<h3>First Time Setup<h3>
Open git bash to config the user..
```python
git config --global user.name "Your Name"
git config --global user.email "your@email.com"\
```
<br>
<h3>🧲 Clone a Repo<h3>
git clone https://github.com/username/repo.git

<br>
<h3>➕ Add files to staging<h3>
git add filename<br>
git add .

<br>
<h3>💾 Save / Commit<h3>
git commit -m "your commit message"

<br>
<h3>⬆️ Push to GitHub<h3>
git push -u origin main<br>
git push


<br>
<h3>🌐 Connect to GitHub<h3>
git remote add origin https://github.com/username/repo.git




<br>
<h3>Real-World Workflow (Daily Use)<h3>
git pull<br>
git add .<br>
git commit -m "Updated module"<br>
git push<br>

<br>
<h3>create a new repository on the command line<h3>
echo "# localrepo" >> README.md
git init<br>
git remote add origin <-link-> <br>
git remote -v <br>
git branch<br>
git branch -M main<br>
<br>
git add README.md<br>
git commit -m "first commit"<br>
git branch -M main<br>
git remote add origin https://github.com/PKInnovate/localrepo.git<br>
git push -u origin main<br>

<br>
<h3>Branch Commands<h3>
git checkout<br>
git branch -M main<br>
git checkout <-branch name-><br>
git checkout -b <-new branch name-><br>
git branch -d <-branch name-><br>

<br>
<h3>Merge Branch Commands<h3>
git diff<-branch name-> (to compare, branches, files and more)<br>
git merge <-branch name-> (to mearge two branches)<br><br>
<br>



✅ To fix it (safe way)

Run this: <br>

git pull --rebase origin main


Then push again: <br>

git push origin main <br>

🧠 Why --rebase?

It replays your local commits on top of the updated <br>remote history, keeping the commit history <br>clean.<br>

If you get merge conflicts: <br>

Git will highlight files. You fix conflicts, then:<br>

git add .
git rebase --continue
git push origin main

⚠️ If you do NOT care about remote changes and want to force push (this overwrites remote):<br>
git push --force origin main


---------------------------------------------------------------------------------------------------------------------------------------

## 1. Create the virtual environment

Open the terminal in your project root and run:
```python
# Create a venv folder named "venv"
python -m venv venv
```
## 2. Activate the virtual environment

Activate the venv for your OS / shell:

```python
# macOS / Linux (bash, zsh)
source venv/bin/activate

# Windows (Command Prompt)
venv\Scripts\activate

# Windows (PowerShell)
.\venv\Scripts\Activate.ps1
```

When activated you should see (venv) in the terminal prompt.

## 3. Verify and list installed packages

After activation, list currently installed packages:

```python
pip list
```


A fresh environment usually shows pip, setuptools, and wheel.

## 4. Install recommended packages (example for battery research)

```python
#Install commonly used libraries for data analysis, ML and environment variables:

pip install numpy pandas matplotlib scikit-learn python-dotenv jupyter
```


(You can add other packages you need, e.g., xgboost, lightgbm, torch, tsfresh, seaborn, etc.)

## 5. Save dependencies (shareable)

Freeze the environment to a requirements.txt file for reproducibility:

```python
pip freeze > requirements.txt
```

To recreate on another machine:

```python
pip install -r requirements.txt
```
## 6. Confirm venv is tracked (or ignored) by git

Recommended: do not commit the venv folder. Add venv/ to .gitignore:

```python
echo "venv/" >> .gitignore
git add .gitignore
git commit -m "Ignore virtual environment folder
```


If you intentionally want to commit the venv (rare, not recommended), remove venv/ from .gitignore and then:
```python
git add venv
git commit -m "Add venv to repo"
```

Check tracked files:
```python
git ls-files | grep venv || echo "venv not tracked"
```
## 7. Deactivate when finished

To exit the virtual environment:
```python
deactivate
```
## 8. Optional: quick .env usage (load env vars in Python)

Create a .env file with variables (do not commit secrets; add .env to .gitignore).

Use python-dotenv to load them:

# example usage in Python
```python
from dotenv import load_dotenv
import os

load_dotenv()  # reads .env in current working directory
api_key = os.getenv("API_KEY")
```
## 9. Quick checklist
```python
 python -m venv venv — created

 source venv/bin/activate or windows alternative — activated

 pip install ... — packages installed

 pip freeze > requirements.txt — saved

 echo "venv/" >> .gitignore — venv ignored by git

 deactivate — when done
```
