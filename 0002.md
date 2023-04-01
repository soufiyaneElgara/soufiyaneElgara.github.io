# Github

---

## Content

- [Github](#github)
  - [Content](#content)
    - [What is Github❓](#what-is-gitub)
    - [what is token ❓](#what-is-token-)
    - [What is Forking \& contributing](#what-is-forking--contributing)
    - [configuration](#configuration)
      - [How to create and manage a project on Github ❓](#how-to-create-and-manage-a-project-on-github-)
  - [fetch vs pull](#fetch-vs-pull)

---

### What is Github❓

- online service that host our project.
- share our code with other developers.
- developers can download the projects and work on theme.
- they can re-upload their edits and marge them with the main code base.
  
### what is token ❓

- personnel access token are alternative to using password for authentication to Github when using CLI or Github API
- a token is no different from a password except:
- it's near-guaranteed to never used else where
- it's guaranteed to have high entropy
- it's scope is more limited than an account-wide password
- in short, Github took things out of the hand of users, because users make poor security decisions.

### What is Forking & contributing

- Forking is a process when you copy a repo that is owned by someone else and he made it public to your forked repos.

### configuration

#### How to create and manage a project on Github ❓

1. **First scenario**: you are building the project for the first time

- create a repo
- copy the URL of you repo
- go to you terminal: `git clone URL`
- after any change and committing the project you can update the project on Github: `git push URL master`(mater or main)
- in general when you clone the Github creates an alias to the URL to verify: `git remote -v` so to update you type only : `git push origin main`(you need a username of your Github, and token)

```bash
git clone https/...  # Copy the project(files) in my local machine
git remote -v        # Display the alias of the url
git push url main    # Update the project with url
git push origin main # Update the project using the alias

```

2. **second scenario**: you have an existing project in your local pc

- you should create a repo, withe the exact name as your project
- copy the link to the repo
- go to terminal
- verify if everything is committed `git status`
- then push to Github : `git push URL main` 
- you can create an alias to the URL : `git remote add origin URL`
- then send:`git push origin main`

1. collaborating on a team

- collaboration, means how to work with Github on a team
- first we suppose we have project on git hub
- after working on the project locally make sure to update from the remote: `git pull origin main`
- create a new branch for the new feature, never work directly on the main(master) : `git checkout -b feature-1` #this command create and move at the same time to the branch
- send the new branch: `git push origin feature-1`
- then i create a pull request, my work need to approved it and reviewed it  by team members or the manger, only than i can merge the branch to main or the master

- How to fork ❓
  - click 'fork' in the original repo
  - in your forked repo, click the clone or download button
  - copy the git link : `git clone URL`
  - How to update from the originals?
  - `git remote add upstream <origin-repo-add>`
  - `git fetch upstream`  
  - `git pull upstream master`: to update the local master
  - Why to submit a pull request?
  - once you have made changes to your fork, you can request for those changes to be merged into the original project.

## fetch vs pull 

1. fetch vs pull
   - both are used to download new data from a remote repo
   1. fetch `git fetch upstream master`
      - git fetch really only downloads new data from a remote repo, but it doesn't integrate this new data into your working files
      - fetch is a greate for getting first view on all things that happend in a remote repo
   2. pull `git pull upstream master`
      - git pull, in contrast, is used with a different goal in lined: to update your corrent HEAD branch with the latest changes from the remote server.
