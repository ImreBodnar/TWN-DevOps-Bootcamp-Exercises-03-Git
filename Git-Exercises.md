# Solutions for Exercises-03-Git

## Exercise 1

```bash
# Navigate to the working directory.
cd Repositories

# Cloning.
git clone https://gitlab.com/twn-devops-bootcamp/latest/03-git/git-exercises.git

# Deleting .git folder.
rm -rf git-exercises/.git

# Renaming the folder, because I want to save it to my GitHub repository with a different name.
mv git-exercises TWN-DevOps-Bootcamp-Exercises-03-Git
cd TWN-DevOps-Bootcamp-Exercises-03-Git

git init
git status

# Commit & push.
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/ImreBodnar/TWN-DevOps-Bootcamp-Exercises-03-Git.git
git push -u origin main
```

## Exercise 2

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# After I added .gitignore lets delete some files & folders.
git rm --cached .DS_Store
git rm -r --cached .idea/
git rm -r --cached out/
git rm -r --cached build/

# Commit & push.
git add .
git commit -m "Removed some files by applying .gitignore"
git push
```

## Exercise 3

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Creating & switching new branch
git switch -c feature/first-branch

# After I made the changes...
git diff

git add .
git commit -m "Updated LogStash version and added an image to index.html"
git push --set-upstream origin feature/first-branch
```

## Exercise 4

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Switch back to main, after create & switch to the bugfix branch
git switch main
git switch -c bugfix/misspell

# After I made the changes...
git diff

git add .
git commit -m "Corrected a misspelling error in Application.java"
git push --set-upstream origin bugfix/misspell
```

## Exercise 5

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Switch back to the main branch.
git switch main

# Merge & push.
git merge feature/first-branch
git push
```

## Exercise 6

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Switch back to the main branch.
git switch bugfix/misspell

# After I made the changes...
git add .
git commit -m "Updated the LogStash version to 7.2"

# Try to merge...
git merge main

# After I fixed the merge conflict...
git status
git add .
git commit -m "Resolved merge conflict"
git push
```

## Exercise 7

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# After I fixed the misspell...
git diff
git add .
git commit -m "Corrected a misspell in index.html"

# After I changed the image src...
git diff
git add .
git commit -m "Changed the image source in index.html"

git push

# Undo the last pushed commit.
git reset --hard HEAD~1
git push --force
```

## Exercise 8

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# After I corrected Bruno's job title...
git diff
git add .
git commit -m "Corrected Bruno's job title in index.html"

# Undo the last unpushed commit.
git reset --hard HEAD~1
```

## Exercise 9

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Switch & merge the bugfix branch into main...
git fetch
git switch main

git merge bugfix/misspell
git push
```

## Exercise 10

```bash
# Navigate to the working directory.
cd Repositories/TWN-DevOps-Bootcamp-Exercises-03-Git

# Deleting the unnecessary branches locally...
git branch -d bugfix/misspell
git branch -d feature/first-branch

# Deleting the unnecessary branches remotely...
git push origin --delete bugfix/misspell
git push origin --delete feature/first-branch
```
