# Bash Tips

Useful but easy to forget tips while doing some bashing.

## Know Your Environment

Two handy commands to view what's in the bash.

```sh
# This would list all available aliases
$ alias

# This would list all environment variables
$ printenv
```

## Change Owner or Change Group Recursively

```sh
$ chown -R {username} {targetpath}
$ chgrp -R {username} {targetpath}
```

## View content of .gz files

```sh
$ zless {filename}.gz
```
