# Shell

The shell is the bread and butter of any developer. Hence you should the right amount of time configuring it to fit your needs, and to make sure you maximize your performance while using it.

Many people use the command line every day and never bother to customize their prompts. It's just like Bilbo says: if you intend to ride a horse all day, you need to learn how to ride a horse.

![](http://28.media.tumblr.com/tumblr_lxjxfkj2bi1r0pci8o1_500.gif)


### Shell Config Files

As I was researching this I found myself in a bit of confusion between ```.bashrc```,  ```.bash_profile```, ```.profile```, etc. [This](http://stackoverflow.com/a/415444) answers explains the difference very nicely, but in a nutshell:
* ```.profile``` is simply the login script filename originally used by ```/bin/sh```.
* ```.bashrc```, ```.zshrc```, amongst others are config files that are read by "interactive" shells (as in, ones connected to a terminal.
    * ```.bashrc``` is only read by a shell that's both interactive and non-login
* Other shells behave differently - eg with ```zsh```, ```.zshrc``` is always read for an interactive shell, whether it's a login one or not.

To avoid all this mess, I concentrate all the configurations in ```.bashrc```, and then I tell all the other files to read from that file, using something like:

```shell
[[ -r ~/.bashrc ]] && . ~/.bashrc
```

**Warning:** This can have obvious side effects. If you don't want a specific command running in a certain type of shell, you might have to re-think this a bit.

In the end, your shell should look like this? Isn't that awesome?

![](final_shell.png)





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


