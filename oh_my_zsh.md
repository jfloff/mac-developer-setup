# Oh My ZSH

*[Oh My ZSH](http://ohmyz.sh/)* is a community-driven framework for managing your zsh configuration. The great thing about it is the plugin variety that you can install, and the amazing themes you have at your disposal. All of that paired with an auto-update tool that makes your life much easier.

To install it just run this command:
```shell
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
```

### Theme
Now you can customize your shell with a theme, choose one from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes). In order to enable a theme, set ```ZSH_THEME``` to the name of the theme in your ```~/.zshrc```; for example: ```ZSH_THEME=agnoster```. If you do not want any theme enabled, just set ```ZSH_THEME`````` to blank: ZSH_THEME=""```.

My personal choice is the **pygmalion* theme. To set the theme, open the `~/.zshrc` file and look for the line starting with `ZSH_THEME`. Paste the name of your theme.


### Plugins

 You can choose the plugins you want from this [list](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview). Enable the plugins you want by editing your ```~/.zshrc``` file, just like my plugins:
 
 ```shell
plugins=(atom brew common-aliases encode64 git git-extras github httpie jsontools last-working-dir osx sublime wd colored-man colorize cp extract brew brew-cask vagrant ruby rvm gem docker bundler aws bower)
 ```

