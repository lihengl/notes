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

## Flushing SSH identities

There is a way to do so other than rebooting the system.

```sh
# Flush all previously added SSH identities
$ ssh-add -D

# List all current identities
$ ssh-add -l

# List all including full public key text content
$ ssh-add -L
```

## Grep for Multiple Words

Searching for lines that have both foo and bar.

```sh
# When we know foo will always precedent bar
$ grep 'foo.*bar'

# When the order can be arbitrary
$ grep 'foo.*bar\|bar.*foo'
```

## List Large Files

When trying to figure out what is eating up disk space

```sh
# List files larger than 1G
find {directory} -size +1G -ls

# List files larger than 1G but smaller than 2G
find {directory} -size +1G -size -2G -ls
```
