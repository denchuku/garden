---
aliases:
  - homebrew
---

[Homebrew](https://brew.sh/) is a great package manager vor macOS. It allows to install typical open source cli tools as well as closed source apps (with ui).

* It's very easy to instal, update and uninstall apps

* Especially covenient for programming frameworks (like dotnet) to keep up to date

* **formula**: normal packages for command line tools / frameworks

* **cask**: package for apps with ui

* **tap**: a repository where homebrew loads packages from (default: "homebrew/cask" and "homebrew/core"

## Links

* [Useful formulas und casks for homebrew](Useful%20formulas%20und%20casks%20for%20homebrew.md)
* [Casks with autoupdate](Casks%20with%20autoupdate.md)
* [Homebrew cheatsheet](https://devhints.io/homebrew)
* [List of installable formulas](https://formulae.brew.sh/formula/)

## Basics

### Install

See [Useful formulas und casks for homebrew](Useful%20formulas%20und%20casks%20for%20homebrew.md).

### Show installed

````
brew list
````

### Show outdated

````
brew outdated
````

### Upgrade

````
brew upgrade
````

### Search for formulas

````
brew search firefox
````
