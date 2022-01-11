# Git Manual
## Git Basics
### Commit Locally
Create a local git repository
```console
$ git init
```

Add all the files in the folder to the git repository
```console
$ git add .
```

Commit the change locally
```console
$ git commit -m 'comments for this commit'
```

For example, 
```console
$ git commit -m 'initial commit'
```
### Configure Romote Repository
Firstly, you should create a git repository on git web, and link of the repository is available on the web. Let's take this `git-manual` repository as an example
```console
$ git remote add origin https://github.com/Bill0412/git-manual.git 
```

You can verify if you have configured it right by using
```console
$ git remote -v
```

If you want to remove a remote upstream, for instance, the `origin`, you may use
```console
$ git remote remove origin
```

### Push to remote
You should be prompted to enter your git username and password after entering the following command. Follow the instructions and if the login info is right, your push should be finished after a while.
```console
$ git push origin master
```

## Git Branches
### Create a git branch

```console
$ git branch new-branch
$ git checkout new-branch
```

Or alternatively, with a single command

```console
$ git checkout -b new-branch
```

## Git Merge

### Make sure your local master is up-to-date
```console
$ git pull origin master
```

### Merge local master to your branch
```console
$ git checkout your-branch
$ git merge master
```
After merging master to your local branch, you should fix the possible conflicts, test the code to make sure the merge is successful.

### Merge your branch back to local master
If the previous step is corret, the following commands should be safe to go.
```console
$ git checkout master
$ git merge your-branch
```

### Push the change to git server
```console
$ git push origin master
```

### Ready for the next stage
Now switch back to your branch and be ready for the next development stage.
```console
$ git checkout your-branch
```
