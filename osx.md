# Mac OS X

Customization tips while using a Mac computer

## Focus Follows Mouse

> The Linux Command Line: A Complete Introduction, Chapter 1
>
> In "A Few Words about Mice and Focus" there is a paragraph
> explaining that this will make a window get focus when the
> mouse just passes over it. It will not come to the fore-
> ground until you click it, but it will be able to receive
> input.
>
> It is suggested in that paragraph that this will make using
> terminal windows easier.

```sh
# Type the folowing into a shell and restart Terminal.app
$ defaults write com.apple.Terminal FocusFollowsMouse -string YES

# And to disable it:
$ defaults write com.apple.Terminal FocusFollowsMouse -string NO
```

Open multiple terminal windows. You can type into one as soon as
you move your mouse cursor over it.

## Change Local Hostname

```sh
# To change it permanently
$ sudo scutil --set HostName {hostname}

# To change it temporarily for current session:
$ sudo hostname {hostname}
```

## Unmount USB Thumbdrive

```sh
# Find the IDENTIFIER string for the thumbdrive first.
# Usually it looks something like /dev/disk2s1
$ diskutil list

# Use the finding above to unmount it
$ diskutil unmount {identifier}
```

## Copy from Terminal to Clipboard

Pipe to `pbcopy` command to get it ready for Ctrl+V

```sh
# Copy entire file content. Works with other commands that print to STDOUT, too
$ cat {somefile} | pbcopy
```
