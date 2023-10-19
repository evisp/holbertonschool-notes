## Git
### What is source code management
- Source code management allows a developer to organize code iterations chronologically, and version it for an application

### What is Git
- Git is a popular approach of a version control system. It stores information in an organized structure that resembles a tree. Merging algorithm is smart - it figures out most conflicts by itself
- You can make several commits - they are local. 
- When you want the team to know, you push (pull first, conflicts resolved on local computer)

### What is GitHub	
- Github is one of the many services that provide
	- A git repository server to push to
	- A web UI and extra features

### What is the difference between Git and GitHub
- Git is a source management system that comes with a command line. GitHub is a popular approach a version control system

### How to create a repository
- git init allows to initialize a local directory as a git repository

### What is a README
- Source of information to tell collaborators and others what the project is about

### How to write good READMEs
- What the project does; why is the project useful; how can users start with the project; how can they get help

### How to commit
- Commits are small atomit iterations made by developers on a branch
- **`git commit -m “Helpful message”`**

### How to write helpful commit messages
- All commits have a one-line sentence describing the commit. It helps to have the project track changes at a glance

### How to push code
- **`git push origin -u main`**

### How to pull updates
- **`git pull origin my_feature`**

### How to create a branch
- **`git branch my_feature`**

### How to merge branches
- **`git checkout main`**
- **`git merge my_feature`**

### How to work as collaborators on a project
- Settings add collaborators from UI

### Which files should and which files should not appear in your repo
- Configurations, keys, password, environment variables do not
- General assets or binary dependencies do not
[Click Here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)
