# Git Tips

Useful but easy to forget ways of doing things in Git.

## Rebase to the first commit

```sh
$ git rebase -i --root master
```

## Specify Commit Author

```sh
# For current repository
$ git config user.name "{author name can have space}"
$ git config user.email {author email}

# Make it global default system-wise
$ git config --global user.name "{author name can have space}"
$ git config --global user.email {author email}
```
