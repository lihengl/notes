# Ubuntu 14.04 LTS

Useful commands when working on Ubuntu.

## Add New User to Ubuntu

When adding and granting user SSH access to an Ubuntu system.

### Create the User

```sh
# This will then prompt for password and other profile data,
# For pure SSH user, keep hitting enter to skip all of them.
$ adduser {username}
```

### Create SSH Authorization

```sh
$ sudo mkdir /home/{username}/.ssh
$ sudo vim /home/{username}/.ssh/authorized_keys

$ sudo chown -R {username} /home/{username}/.ssh
$ sudo chgrp -R {username} /home/{username}/.ssh

$ sudo chmod 700 /home/{username}/.ssh
$ sudo chmod 600 /home/{username}/.ssh/authorized_keys
```

Then put the public key text content into `authorized_keys`

### Give sudo Permission

```sh
$ sudo vim /etc/sudoers
# Add the following line at the end of the file
{username} ALL=(ALL) NOPASSWD: ALL
```
