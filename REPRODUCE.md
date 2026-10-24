# Reproduction and GitHub instructions (Windows / VS Code)

## 1. Copy your real project files here
Copy the completed `assignment.ipynb`, `olivetti_split.npz`, and the clean/masked figure from your computer into this folder. Add any actual source scripts required by your rubric. Do not rerun the expensive Q3 experiment just to collect files.

## 2. Set up Python in PowerShell
```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```
If activation is blocked:
```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## 3. Create an empty GitHub repository
Create a new empty repository on GitHub. Open this folder in VS Code and select Terminal > New Terminal. Then run:
```powershell
git init
git add .
git status
git commit -m "Add Olivetti Faces assignment results"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
Replace the URL with your real repository URL. If Git asks for identity:
```powershell
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```
Then retry the commit.

## 4. Add code snapshot hash to the report
Run `git rev-parse HEAD`, copy the full hash into page 1, and replace the repository URL placeholder. Save the completed PDF as `report.pdf`.

## 5. Commit the final PDF
```powershell
git add report.pdf
git commit -m "Add final report"
git push
git rev-parse HEAD
```
Paste that last hash into `FINAL_COMMIT.txt`, then run:
```powershell
git add FINAL_COMMIT.txt
git commit -m "Record final repository commit"
git push
git rev-parse HEAD
```
Record the latest hash wherever your instructor requires. The hash printed in the PDF is the code snapshot hash from before the report commit; adding a hash to the PDF necessarily changes the commit.

## 6. Final check
Open the GitHub repository in a browser and verify that the notebook, split, report, plots, config, results, and environment files are present. Check the report page limit and first-page requirements. Use any more specific instructions given by your instructor.
