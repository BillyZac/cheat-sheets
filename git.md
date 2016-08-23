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
