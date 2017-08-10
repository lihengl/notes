# Add Ubuntu User

When adding user to Ubuntu server that uses SSH authentication

## Create the User

```sh
# This will then prompt for password and other profile data,
# For pure SSH user, keep hitting enter to skip all of them.
adduser {username}
```

## Create SSH Authorization

```sh
mkdir /home/{username}/.ssh
vim /home/{username}/.ssh/authorized_key
# Put the public text content into the file

chown -R {username} /home/{username}/.ssh
chgrp -R {username} /home/{username}/.ssh

chmod 700 /home/{username}/.ssh
chmod 600 /home/{username}/.ssh/authorized_keys
```

Then put the public key text content into `authorized_keys`

## Give sudo Permission

```sh
sudo vim /etc/sudoers
# Add the following line at the end of the file
{username} ALL=(ALL) NOPASSWD: ALL
```
