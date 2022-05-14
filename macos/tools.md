---
description: Essential tools to have
---

# 🛠 Tools

## Xcode Command Line Tools

Install the command line developer tools

```shell-session
$ xcode-select --install
```

## Package Manager

macOS doesn't come with a package manager, our best option is to install [Homebrew](https://brew.sh/)

> The Missing Package Manager for macOS

```shell-session
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Git

[Install Git](https://git-scm.com/download/mac)

```shell-session
$ brew install git
```

```shell-session
$ git config --global user.name "João Barreiros"
$ git config --global user.email "unstablectrl@gmail.com"
$ git config --global init.defaultBranch "main"
$ git config --global core.editor "code"
```

## Heroku CLI

```shell-session
$ brew tap heroku/brew
$ brew install heroku
```
