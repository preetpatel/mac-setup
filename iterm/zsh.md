# Zsh

The Z shell \(also known as `zsh`\) is a Unix shell that is the default shell for macOS. It's recommended to use `zsh` over `bash`. It's also highly recommended to install a framework with `zsh` as it makes dealing with configuration, plugins and themes a lot nicer.

We've also included an `env.sh` file where we store our aliases, exports, path changes etc. We put this in a separate file to not pollute our main configuration file too much. This file is found in the bottom of this page.

Install `zsh` using [Homebrew](../homebrew/):

```bash
brew install zsh
```

Now you should install a framework, we recommend to use [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh).

The configuration file for `zsh` is called `.zshrc` and lives in your home folder \(`~/.zshrc`\).

## Oh My Zsh

[Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) is an open source, community-driven framework for managing your `zsh` configuration. It comes with a bunch of features out of the box and improves your terminal experience.

Install Oh My Zsh:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Configuration

The out-of-the-box configuration is usable but you probably want to customise it to suit your needs. The [Official Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki) contains a lot of useful information if you want to deep dive into what you can do with Oh My Zsh, but we'll cover the basics here.

To apply the changes you make you need to either **start new shell instance** or run:

```bash
source ~/.zshrc
```

#### Plugins

Add plugins to your shell by adding the name of the plugin to the `plugin` array in your `.zshrc`.

```bash
plugins=(colorize gitfast fd nvm vi-mode z)
```

You'll find a list of all plugins on the [Oh My Zsh Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins). Note that adding plugins can cause your shell startup time to increase.

**zsh-syntax-highlighting**

The Syntax Highlighting plugin adds beautiful colours to the commands you are typing.

Clone the zsh-syntax-highlighting plugin’s repo and copy it to the “Oh My ZSH” plugins directory.

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

**zsh-autosuggestions**

This plugin auto suggests any of the previous commands. Pretty handy! To select the completion, simply press → key.

Clone the zsh-autosuggestions plugin’s repo and copy it to the “Oh My ZSH” plugins directory.

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

**Enforce Changes**

To apply the changes you make you need to either **start new shell instance** or run:

```bash
source ~/.zshrc
```

#### Themes

Changing theme is as simple as changing a string in your configuration file. The default theme is `robbyrussell`. Just change that value to change theme, and don't forget to apply your changes.

```bash
ZSH_THEME=pygmalion
```

You'll find a list of themes with screenshots on the [Oh My Zsh Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/themes).

## `env.sh`

To include `env.sh`, open `~/.zshrc` and add the following:

```bash
source ~/<path to file>/env.sh
```

This file comes with some pre-defined settings, **they are all optional**. Please review them before you use them as your configuration. These are just examples to show you what you can customise in your shell.

```bash
#!/bin/zsh

# Add commonly used folders to $PATH
export PATH="/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"

# Specify default editor. Possible values: vim, nano, ed etc.
export EDITOR=vim

# File search functions
function f() { find . -iname "*$1*" ${@:2} }
function r() { grep "$1" ${@:2} -R . }

# Create a folder and move into it in one command
function mkcd() { mkdir -p "$@" && cd "$_"; }

# Example aliases
alias cppcompile='c++ -std=c++11 -stdlib=libc++'
alias g='git'
```

