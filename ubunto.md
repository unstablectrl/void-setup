# Ubuntu

## Ubuntu Package Manager

Default Package Manager [Apt](https://ubuntu.com/server/docs/package-management)

```bash
sudo apt update && sudo apt upgrade -y
```

Other upgrade commands

```bash
sudo apt dist-upgrade -y
sudo apt autoremove -y
sudo apt full-upgrade -y
```

## Oh My Zsh

Installing [Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

```bash
sudo apt install zsh
```

Installing [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh#basic-installation)

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

My config [.zshrc](https://gist.github.com/unstablectrl/12351f8d50b265652e0a300c378f4a8a)

### **Theme**

`unstable`

```bash
curl "https://gist.githubusercontent.com/unstablectrl/bdbf55d4600441665198347b714d82ec/raw/5a35ad413e096564ccb7c839b2ba68de3a6df736/unstable.zsh-theme" -o "$ZSH_CUSTOM/themes/unstable.zsh-theme" --create-dirs
```

### Custom Plugins

#### zsh-autosuggestions

* [Github](https://github.com/zsh-users/zsh-autosuggestions.git)

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

#### zsh-syntax-highlighting

* [Github](https://github.com/zsh-users/zsh-syntax-highlighting.git)

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

## Apps

### Git

* [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git) - `git`

```bash
sudo apt install git-all
```

```bash
git config --global core.excludesfile "~/.gitignore_global"
git config --global user.name "João Barreiros"
git config --global user.email "unstablectrl@gmail.com"
```

{% tabs %}
{% tab title="Ubuntu" %}
```bash
git config --global core.editor "code"
```
{% endtab %}

{% tab title="WSL2" %}
```bash
git config --global core.editor "code --wait"
```
{% endtab %}
{% endtabs %}

```bash
echo "venv\n.python-version" > ~/.gitignore_global
```

### Pyenv

* [Github](https://github.com/pyenv/pyenv)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/pyenv) - `pyenv`

```bash
sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

```bash
curl https://pyenv.run | bash
```

### Nvm

* [Github](https://github.com/nvm-sh/nvm)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/nvm) - `nvm`

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

### fzf

* [Github](https://github.com/junegunn/fzf)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/fzf) - `fzf`

```bash
sudo apt-get install fzf
```

### Aws Cli

* [Website](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/aws) - `aws`

```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

{% code title="~/.aws/config" %}
```bash
[default]

[profile profilename]
region = ...
output = ...
```
{% endcode %}

{% code title="~/.aws/credentials" %}
```bash
[profilename]
aws_access_key_id = ...
aws_secret_access_key = ...
```
{% endcode %}

### Heroku Cli

* [Website](https://devcenter.heroku.com/articles/heroku-cli)
* [Oh My Zsh Plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/heroku) - `heroku`

```bash
curl https://cli-assets.heroku.com/install.sh | sh
```

```bash
heroku login
```

## Vim

### Theme

```bash
wget  -P ~/.vim/colors/ "https://raw.githubusercontent.com/BarretRen/vim-colorscheme/master/colors/monokai.vim"
```

```text
syntax on
colorscheme monokai
```

