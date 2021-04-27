## Linking files

Link file to a directory included in path
```shell
# Assuming that "/usr/local/bin/" is in path, "my-command" is available in path after the link has been created
$ ln -s ~/Documents/my-command /usr/local/bin/my-command
```

### Show location of command
Command
```shell
$ which git
/usr/local/bin/git
```

### Who were command links to
Command
```shell
$ readlink /usr/local/bin/git
../Cellar/git/2.31.1/bin/git
```

Open Finder from Terminal: `open .`

To clear current command: `⌃` + `U`

To set zsh as default shell: `chsh -s /bin/zsh`