# git

## Merge conflicts

To checkout your own version you can use one of:

```
git checkout HEAD -- <filename>

git checkout --ours -- <filename>

git show :2:<filename> > <filename> # (stage 2 is ours)
```

To checkout the other version you can use one of:

```
git checkout test-branch -- <filename>

git checkout --theirs -- <filename>

git show :3:<filename> > <filename> # (stage 3 is theirs)
```


You would also need to run 'add' to mark it as resolved:

```
git add <filename>
```

## Show what a commit did

`git show <commit-id>`

Also try
`git diff <commit-id1> <commit-id2>`

and
`git log -p`


## Pull a specific branch

`git pull origin branch-i-want`

This pulls the remote branch into your current local branch. You might actually want to do the following instead:

## Create a new local branch based on a remote branch

`git co -b forecast-end-date origin/forecast-end-date`

## Push to a specific branch on the remote repo

`git push origin <local-branch>:<remote-branch>`

## Replace the url of a remote repo
Assuming the name of the remote is "origin":
`git remote set-url origin <new-url>`

## Keep your fork synced with the original
First, fork a project and clone your version to your local machine. Then add the original repo as an upstream remote:
```
git remote add upstream https://github.com/octocat/Spoon-Knife.git
git remote -v # Confirm that it worked
```

When stuff changes on the original, fetch it:
```
git fetch upstream
git checkout master
git merge upstream/master
```

## Roll back to a specific commit, create a new commit.
This command creates a new commit that undoes the changes from a previous commit. This command adds new history to the project (it doesn't modify existing history).
```
git revert <commit>
```

## Roll back to a specific commit, changing history
```
git reset --hard <commit>
```

## Force push to a remote repository
This overwrites history on the remote, so with care!
```
git push origin master -f
```
