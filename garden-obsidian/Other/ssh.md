SSH keys can be used to login with the ssh tool. It's also useful for accessing git repositories.

## Initial configuration / ssh directory
ssh configuration files are located at `~/.ssh/`. 
If directory doesn'te exist create it and limit access:
```shell
chmod 700 ~/.ssh
```

On macOS adjust `~/.ssh/config` so that passwords for ssh keys can be fetched from macOS keychain automatically without having to enter the password every time.
```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  Protocol 2
#  # Default Identity file 
#  IdentityFile ~/.ssh/id_ed25519  
```

> [The Ultimate Guide to SSH - Setting Up SSH Keys](https://www.freecodecamp.org/news/the-ultimate-guide-to-ssh-setting-up-ssh-keys/):
> With that, whenever you run `ssh` it will look for keys in Keychain Access. If it finds one, you will no longer be prompted for a password. Keys will also automatically be added to `ssh-agent` every time you restart your machine.

## Create key
Create your private key / public key pair:
```shell
ssh-keygen -t ed25519 -f ~/.ssh/id_github_com_ed25519 -C "ID+username_@users.noreply.github.com"
```
It's recommended to set a password for the key (and save that password somewhere safe).

- `-C`: Your email. For github you can hide your email in commits ([Setting your commit email address - GitHub Docs](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address))
- `-f`: Specify location where key will be saved. If you don't specify it will have a default (e.g. `.ssh/id_ed25519`)

If you don't use the default filename for the keys then you might have to specify the filename every time. A non-default filename might be useful if you need multiple keys. You can avoid having to specify the key with every ssh call be defining a host entry (see below).

On macOS you can add the key to ssh agent so that you don't have to type the password every time the ssh key is used:

`ris:Apple` macOS: 

```shell
ssh-add -K ~/.ssh/id_github_com_ed25519
```

- `-K` is a macOS specific option

This only has to be done once.

## Have a config for a specific host
Edit ( `~/.ssh/config` ) in order to specify keys and settings for specific hosts (e.g. `github.com`):
```
Host github.com
  Hostname github.com
  User git
  IdentitiesOnly yes
  IdentityFile ~/.ssh/id_github_com_ed25519
```

## Copy public ssh key to clipboard
`ris:Apple` macOS: 
```shell
pbcopy < ~/.ssh/id_github_com_ed25519.pub
```

## Test ssh connection
Test if you can connect with ssh:
```shell
ssh -T github.com
```
