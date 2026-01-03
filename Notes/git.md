---
aliases:
createdon: 2026-01-02 08:16:03
type: Tool
tags:
---
# Git
---
Git is a fast, scalable, distributed version control system. It originally created by Linus Torvalds in 2005. It has become the most commonly used version control system in the world with nearly 95% of developers reporting it as their primary system, based on a 2022 Stack Overflow survey.

Or as the man page refers to itself:  *git - the stupid content tracker*
## General Usage
---


## Tips and Tricks
---
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

## References
---
