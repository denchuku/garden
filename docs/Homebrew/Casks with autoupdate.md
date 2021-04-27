Two types of casks are not automatically updated by [homebrew](index.md):

* Casks with `autoupdate`: Use the update mechanism of the app
* Casks with `version` `latest` instead of a specific version number

This information is visible with the `brew info <name>`  command for these apps.

## buo/cask-upgrade

[GitHub - buo/homebrew-cask-upgrade: A command line tool for upgrading every outdated app installed by Homebrew Cask](https://github.com/buo/homebrew-cask-upgrade) allows to better manage these apps.

````shell
# Add tap once
brew tap buo/cask-upgrade
````

To update outdated apps and show a list of casks and their version number

````shell
brew cu
````

Use `brew cu -a` to reinstall apps with autoupdate. Use `-f` to reinstall apps with version `latest`.
