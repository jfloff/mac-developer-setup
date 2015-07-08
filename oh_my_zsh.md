# Oh My ZSH!

*[oh-my-zsh](http://ohmyz.sh/)* is a community-driven framework for managing your zsh configuration. The great thing about it is the plugin variety that you can install, and the amazing themes you have at your disposal. All of that paired with an auto-update tool that makes your life much easier.

To install it just run this command:
```shell
$ curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

### Antigen

[Antigen](http://antigen.sharats.me/) is a small set of functions that help you easily manage your shell (zsh) plugins, called bundles. Its like a package manager for *zsh* shells.

To install just run this commands:
```shell
mkdir ~/.antigen
curl -L https://raw.githubusercontent.com/zsh-users/antigen/master/antigen.zsh > ~/.antigen/antigen.zsh
source ~/.antigen/antigen.zsh
```

Next we edit our ```.zshrc``` with the typical antigen settings. Here's my own:
```shell
source /.antigen/antigen.zsh

# Load the oh-my-zsh's library.
antigen use oh-my-zsh

# Bundles from the default repo (robbyrussell's oh-my-zsh).
antigen bundle git
antigen bundle heroku
antigen bundle pip
antigen bundle lein
antigen bundle command-not-found

# Syntax highlighting bundle.
antigen bundle zsh-users/zsh-syntax-highlighting

# Load the theme.
antigen theme robbyrussell

# Tell antigen that you're done.
antigen apply
```

### Theme
Now you can customize your shell with a theme, choose one from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). My personal choice is the *pygmalion* theme. To enable a theme, just type (replace *pygmalion* with a theme of your choice):

```shell
antigen theme pygmalion
```


### Plugins

 You can choose the plugins you want from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview). To install plugins just type ```antigen Enable the plugins you want by editing your ```~/.zshrc``` file, just like my plugins:
 
 ```shell
plugins=(atom brew common-aliases encode64 git git-extras
    github httpie jsontools last-working-dir osx sublime wd
    colored-man colorize cp extract brew brew-cask vagrant
    ruby rvm gem docker bundler aws bower)
 ```

<br>

That's right, we've fallen into ***shell's darksness***!
![](http://25.media.tumblr.com/3f5c9cac69387e803763ee5b1d35019e/tumblr_mhv1cxlzim1s3uvpwo5_500.gif)