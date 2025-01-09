# Week 1 Activity Solution

---

#### **Part 1: File System Navigation and Manipulation**
1. `pwd` – to check the current working directory.
2. `mkdir my_project` – to create the directory.
3. `cd my_project` – to navigate into the directory.
4. `touch readme.txt` – to create the file.
5. Use `nano readme.txt` (or `vim readme.txt`), add "This is my first project", then save and exit.
6. `cp readme.txt info.txt` – to copy the file.
7. `mv info.txt ~/info.txt` – to move the file to the home directory.
8. `rm readme.txt` – to delete the file.
9. `cd ~` – to return to the home directory.
10. `ls` – to list files and confirm `info.txt` is present.

---

#### **Part 2: Introduction to Git**
1. in the `my_project` directory, use `git init` – to initialize a repository.
2. Create `main.py` with `nano main.py` (or any editor), add `print("Hello, world!")`.
3. `git status` – to check the status of the repository.
4. `git add main.py` – to stage the file.
5. `git commit -m "Initial commit"` – to commit the changes.
6. `git branch feature-branch` – to create a new branch.
7. `git checkout feature-branch` – to switch to the new branch.
8. Update `main.py` with the new text `print("Hello, Python World!")` and save the changes.
9. `git add main.py` – to stage the updated file.
10. `git commit -m "Updated greeting in main.py"` – to commit the changes.
11. `git checkout main` – to switch back to the `main` branch.
12. `git merge feature-branch` – to merge the changes.
13. go create a new public repo on github called `my_project`.
14. `git push -u origin main` – to push the repository to GitHub (requires prior GitHub setup). 


















