# Git

---

## Content

- [Git](#git)
  - [Content](#content)
    - [What is Git❓](#what-is-git)
    - [Why use Git❓](#why-use-git)
    - [How Git works❓](#how-git-works)
    - [What is branches ❓](#what-is-branches-)
    - [Configuration](#configuration)

---

### What is Git❓

- Git is free and open source for distribution version control.
- It's a system that records changes to our files over time.
- Git allows users to track code changes and manage their project using simple commands.
- We can recalls specific version of those files at any given time.
- Many people can easily collaborate on a project and have their own version of project files on their computer.
  
### Why use Git❓

- Store revisions in a project history in just one directory.
- Rewind on new features in the project I wanted to.
- Work on a new feature without messing up the main codebase.
- Easily collaborate with other programmers.
  
### How Git works❓

- The hart of Git is **repository** used to contain a project.
- What is **Repository** ?
  - A repository is a container for a project you want to track with git.
  - A repository can allow users to store several different repo's and truck each one dependently.
  - You can have many different repos's for many different projects on your computer.
- What is **commits** ?
  - Git commit, creates a commit, which is like a snapshot of your repository.
  - commits are the building blocks of a 'save points' with in git's version control.
  - This commit are snapshots of your entire repository to a specific times.
  - You should make new commits often, based around logical unites of change.
  - Over time commits should tell us a story of the history of your repo and how it came to be they way it currently is.
- What is **the commit process** ?
  - The Git committing process requires several steps: Moving Changes to the staging area and Saving them with Commit Command.
  - The phases of a commit:
      1. **Modified**: Changed files not commited.
      2. **Staging**: Add any changed files to staging that you want to commit.
      3. **Commited**: Any files in the stagin area are added to the commit when we make one.

### What is branches ❓

- A branch is new/separate version of the main repo.
- Branches allow you to work on different parts of a project, without impacting the main branch.

### Configuration

1. some basic commands in git:

```bash
sudo apt install git  #used to insall git on ubuntu.
git --version         #display the version.
git config --global user.name soufiyane             #to set a username to the git.
git config --gloabal user.email soufiyane@gmail.com #to set an email to git.
git config user.name  #display the username.
git config user.email #dispaly the email.

```

1. How to create and manipulate repos ?

- Create a new repo:

```bash
mkdir my-project` #create a folder for the project
cd my-project     #go to the folder
git init          #intialize a new, empty repo here

```

- How to commit a change ?

```bash
git add filename       #add the changed file to the staged phase
git add .              #add all files to the staging phase
git rm --cach filename #to remove a file from the stage phase
git status             #display the status file in stage phase(if add or not)
git commit -m "describ the current commit" #now you'r committing, with a discription message
git log                #display all the commits in the long format
git log --oneline      #display all the commits in a concise format
```

- How to back and change the commits ?

1. checkout a commit : View the commits without changing anything (read only)

```bash
git checkout 3243FFD #view the all the commits specific time, without editing(read only)

 ```

1. revert a commit: Basically it can modify a commit, but it creates a new one, withe the new or deleted feature

```bash
git revert 233EDS #the reverted commit steel in the logs
```

1. reset a commit: it means deleting the commit for good
   1. deleting the commit, with the possibility to recover

```bash
git reset 3242ffs #stell we have the changing in the working area, to recover:
    git add . 
    git commit -m "undo the reset"
```

   1. deleting for good(no chance to recover)

```bash
git reset 12131 --hard #remove the commit defentlly
```

1. How to manipulate branches:

- create new branch and move to it

```bash
git bransh feature-1   # Create a new branch
git branch -a          # Display all the branches
git checkout feature-1 # Switch to a specific branch
```

- How to delete a branch?

```bash
git checkout master     # You should move to master/main first
git branch -d feature-1 # Delete a merged branch
git branch -D feature-1 # Delete un merged branch

```

- How to merge a branch?

```bash
git checkout master # Move to the branch that you want to marge in to it
git merge feature-1 # Merge the feature 1 to master branch
```
  
- What is conflict?
  - An example of a conflict, when you make a new Branch for new feature, then after you a guy modifies in the master branch, then you need to help Git to decide which modification to keep

```bash
git marge feature-1 # pops an error, you need modifie the code
git add .           # add to stagin erea
git commit`         # make a commit witout a name(:wq, if a bash file is popeds)
```
