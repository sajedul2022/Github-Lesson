# Git Command List

bash Working Directory: Local Direcory : Remote Directory

```bash git config --list ```

# For User Config
```bash git config --global user.name "sajedul2022" ```

```bash git config --global user.email=sajedul.idb.info@gmail.com ```

# pwd- Present Directory

```bash touch readme.md  ```

```bash git status ```

```bash git init ```

```bash ls // list show  ```

```bash ls -a // hidden file show ```

```bash git add --all / git add .(Present Directory, Not Sub folder add, But Root Directory is fine) / git add filename ```

```bash git commit -m "New file readme and Git command handnote file created" ```

```bash git log/ git log --oneline  // History for comment ```

```bash vi readme.md // :q for close ```

```bash touch help.md ```

# // revert previous comment:

git reset --hard a1f5460 // revert previous comment and Id head 
git reflog // show all comment ID
git reset --hard 8c4adf9 // revert code with comment id

git rm help.md // remove file 

# // Branch
git branch --list // show list
git branch dev/add-heading-text // create branch as master sub branch
git branch -d dev/add-heading-text // delete branch
git switch dev/add-heading-text // switch another branch
git branch -m feature/add-heading-text // rename branch 

git branch feature/fix-text
git switch feature/fix-text

# // Merge Branch 
git switch master
git merge feature/add-heading-text

# // conflict
show both branch code and edit 
git add .
git commit 
:wq

# // Stash: switch another branch without commiting
git stash 

# // later show or add 
git stash list 
git stash show -p
:q
git stash pop
git stash apply stashId
git add .
git commit 

# // git ignore 
mkdir node_modules
touch .gitignore

# // already coomit file , need to ignore
git rm --cached abcd.md
git rm --cached node_modules
git diff .gitignore

# ======== Git hub ======

# // create a new repository on the command line

git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sajedul2022/Github-Lesson.git
git push -u origin main

# // push an existing repository from the command line

git remote add origin https://github.com/sajedul2022/Github-Lesson.git
git branch -M main
git push -u origin main


# // update data after push, merge pull request

git pull


# Docker summary command : 
Dockerfile: 

FROM node:alpine
COPY . /app 
WORKDIR /app
CMD node app.js

# docker version check
docker version

# build: 
docker build -t docter-test .

# see images:

docker images
docker image ls

# docker run
docker run docter-test  // Folder name [docter-test]

# docker hub Online Repo Local to Dockerhub push

docker login 
docker tag 7f51a5914209 sajedul2022/docter-test
docker images
docker push sajedul2022/docter-test

# pull Others computer / docker / pc / online play etc

Like: https://labs.play-with-docker.com/

docker version
docker images
docker pull sajedul2022/docter-test:latest
docker images
docker run sajedul2022/docter-test

