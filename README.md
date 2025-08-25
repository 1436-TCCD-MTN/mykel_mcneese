# Home
Welcome to your "Home" repository for Programming Fundamentals!
## 🎯 Purpose of this Repository
This repository is your central development hub for the entire semester. You should launch your GitHub Codespace from **this repository only.** All of your assignments and projects will be cloned _into_ this Codespace environment.
Think of this as your personal, cloud-based computer for our class.
## ⚙️ Standard Assignment Workflow Reminder
Every assignment in this course will follow the same professional Git workflow. Use this checklist as a quick reminder for each assignment you start.
### 1. Clone & Setup
- In your "Home" Codespace terminal, use `git clone` to download the new assignment repository.
- `cd` into the new assignment folder.
- Run `git config core.hooksPath .githooks` to enable the automated checks for that specific repository.
### 2. Create Your Branch
- Before writing any code, create a new branch for your work. This keeps the `main` branch clean and is required for submission.
```bash
git checkout -b <branch_name>
# Example: git checkout -b feat/implement-guessing-game
```
### 3. Write Code & Commit Your Progress
- As you work, save your progress in small, logical chunks. The pre-commit hooks will automatically check your code for formatting and errors.
```bash
# Stage the specific file(s) you changed
git add src/main.rs

# Commit your changes with a semantic message
git commit
# (This opens an editor for you to write a message like "feat: generate secret number")
```
### 4. Push Your Branch
- When you are done with a chunk of work, or just want to back up your commits to GitHub, push your branch.
```bash
# The first time you push a new branch:
git push --set-upstream origin <branch_name>

# For all future pushes on the same branch:
git push
```
### 5. Update Changelog & Create a Pull Request
- Once all your code for the assignment is complete and pushed, you have two final steps to submit your work:
1. **Generate the Changelog:** Run these commands to automatically update the `CHANGELOG.md` file and push it.
```bash
git cliff -o CHANGELOG.md
git add CHANGELOG.md
git commit -m "chore: update changelog"
git push
```
2. **Create a Pull Request:** Go to the assignment repository page on GitHub. You will see a green button to "Compare & pull request". Click it, give your PR a title, and submit it. This formally marks your assignment as ready for grading.