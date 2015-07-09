# Oh My ZSH!

*[oh-my-zsh](http://ohmyz.sh/)* is a community-driven framework for managing your zsh configuration. The great thing about it is the plugin variety that you can install, and the amazing themes you have at your disposal. All of that paired with an auto-update tool that makes your life much easier.

To install it just run this command:
```shell
$ curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

### Aliases

Create an alias files where we will place all our aliases, let's call it ```.zsh_aliases```. Here is my file:

```shell
alias edit="${EDITOR} $1"

# -------------------------------------------------------------------
# directory movement
# -------------------------------------------------------------------
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'
```

Finally add this line to your ```.zshrc``` so your aliases files is sourced correctly.

```shell
[ -e "${HOME}/.zsh_aliases" ] && source "${HOME}/.zsh_aliases"
```

### Antigen

[Antigen](http://antigen.sharats.me/) is a small set of functions that help you easily manage your shell (zsh) plugins, called bundles. Its like a package manager for *zsh* shells.

To install just run this commands:
```shell
$ mkdir ~/.antigen
$ curl -L https://raw.githubusercontent.com/zsh-users/antigen/master/antigen.zsh > ~/.antigen/antigen.zsh
$ source ~/.antigen/antigen.zsh
```

### Theme and Plugins
Now you can customize your shell with a theme, choosing one from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). My personal choice is the *pygmalion* theme.

You can choose the plugins you want from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview).

Both theme and plugins are going to be placed on the antigen configuration in our ```.zshrc``` file. Here's my own:

```shell
source /.antigen/antigen.zsh

# Load the oh-my-zsh's library.
antigen use oh-my-zsh

# Bundles from the default repo (robbyrussell's oh-my-zsh).
antigen bundle atom
antigen bundle aws
antigen bundle bundler
antigen bundle common-aliases
antigen bundle gem
antigen bundle git
antigen bundle git-extras
antigen bundle github
antigen bundle httpie
antigen bundle jsontools
antigen bundle last-working-dir
antigen bundle osx
antigen bundle ruby
antigen bundle rvm
antigen bundle wd
antigen bundle colored-man
antigen bundle colorize
antigen bundle cp
antigen bundle extract
antigen bundle brew
antigen bundle brew-cask
antigen bundle unixorn/autoupdate-antigen.zshplugin
antigen bundle command-not-found
antigen bundle zsh-users/zsh-syntax-highlighting
antigen bundle zsh-users/zsh-completions src
antigen bundle zsh-users/zsh-history-substring-search

# Load the theme.
antigen theme pygmalion

# Tell antigen that you're done.
antigen apply
```

<br>

That's right, we've fallen into ***shell's darksness***!
![](http://25.media.tumblr.com/3f5c9cac69387e803763ee5b1d35019e/tumblr_mhv1cxlzim1s3uvpwo5_500.gif)