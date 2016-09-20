# Using diff

To see the diff between a specific commit and the current commit:
```
git diff commit_id HEAD
```

You can also specify a directory or file to diff e.g.
```
git diff commit_id HEAD app/services
```

Or for a specific file:
```
git diff commit_id HEAD package.json
```

Show unstaged changes:
```
git diff
```

To show staged changes:
```
git diff --cached
```

Show all changes (staged and unstaged):
```
git diff HEAD
```
