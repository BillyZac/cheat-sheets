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
