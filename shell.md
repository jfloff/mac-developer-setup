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


Now we are going to install **iTerm** and **Oh My ZSH!**, and when its all done, your shell should look like this: 

![](final_shell.png)

Isn't that awesome?
