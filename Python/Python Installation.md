# Python installation
Required: [[Homebrew/index|homebrew]]

## Install python
```shell
brew install python
```
In order not to use macOS old python, add new python to the path of the shell: In `.zshrc`:
```shell
export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```


## Install pipenv
Also install [[pipenv]] to manage virtual environments:
```shell
brew install pipenv
```