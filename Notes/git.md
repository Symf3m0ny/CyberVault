---
aliases:
createdon: 2026-01-02 08:16:03
type: Tool
tags:
---
# Git
---


## Tips and Tricks

### Remove files from history
Let's assume we have committed a file to the repository that should not have been committed.

This rewrites history using `amend` and `rebase`, so it's important to make other repository collaborators aware that this is happening.

#### File in the most recent commit
```
git restore -staged <file-to-remove>
```

```
git commit --amend --no-edit
```

#### File in an older commit

```
git rebase -i Head~n
```

```
git rm --cached <file-to-remove>
```

```
git commit --amend
```

```
git rebase --continue
```

```
git push --force
```