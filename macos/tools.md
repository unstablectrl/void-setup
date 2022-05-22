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

## GPG

```shell-session
$ mkdir ~/.gpg
$ touch ~/.gpg/private.key
```

Paste private key inside the newly created `private.key` file

```shell-session
$ brew install gpg
$ gpg --import ~/.gpg/private.key
```

Change the key trust

```shell-session
$ gpg --edit-key <keyname>

gpg> trust

Please decide how far you trust this user to correctly verify other users' keys
(by looking at passports, checking fingerprints from different sources, etc.)

  1 = I don't know or won't say
  2 = I do NOT trust
  3 = I trust marginally
  4 = I trust fully
  5 = I trust ultimately
  m = back to the main menu

Your decision? 5

Do you really want to set this key to ultimate trust? (y/N) y

gpg> save
gpg> quit
```

Set your GPG signing key in Git

```shell-session
$ git config --global user.signingkey "${$(gpg --list-keys --keyid-format=long | awk '/pub/{if (length($2) > 0) print $2}')##*/}"
```

```shell-session
$ gpg --armor --export "${$(gpg --list-keys --keyid-format=long | awk '/pub/{if (length($2) > 0) print $2}')##*/}"
```

To be able to sign using Visual Studio Code

```shell-session
$ brew install pinentry-mac
$ echo "pinentry-program /opt/homebrew/bin/pinentry-mac" >> ~/.gnupg/gpg-agent.conf
```

Uncertain if this is needed

```shell-session
$ git config --global --add gpg.program $(which gpg)
```

## Heroku CLI

```shell-session
$ brew tap heroku/brew
$ brew install heroku
```
