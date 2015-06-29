# Shell

The shell is the bread and butter of any developer (well, not really but you get the point). Hence you should the right amount of time configuring it to fit your needs, and to make sure you maximize your performance while using it.


It's just like Bilbo says: if you intend ride a horse all day, you just learn how to ride a horse.

![](http://28.media.tumblr.com/tumblr_lxjxfkj2bi1r0pci8o1_500.gif)

### Shell Config Files

As I was researching this I found myself in a bit of confusion between ```.bashrc``` and ```.bash_profile```. [This](http://stackoverflow.com/a/415444) answers explains the difference very nicely, but in a nutshell:
* ```.profile``` is simply the login script filename originally used by ```/bin/sh```.
* ```.bashrc```, ```.zshrc```, amongst others are config files that are read by "interactive" shells (as in, ones connected to a terminal.
    * ```.bashrc``` is only read by a shell that's both interactive and non-login
* Other shells behave differently - eg with ```zsh```, ```.zshrc``` is always read for an interactive shell, whether it's a login one or not.

To avoid all this mess, I concentrate all the configurations in ```.bashrc```, and then I tell all the other files to read from that file, using something like:

```shell
[[ -r ~/.bashrc ]] && . ~/.bashrc
```

To avoid all this mess, I concentrate all the profiles in a single file: ```.bashrc```. And



**Warning:** This can have obvious side effects. If you don't want a specific command running in a certain type of shell, you might have to re-think this a bit.

### iTerm 
If you're still using Terminal, stop it. Right now. Just close it, remove the shortcuts and do yourself a favour: install **iTerm2**. Future you will thank both you and me.





### Colors and Font Settings


####Open tab/pane with current working directory
Under **Profiles** tab, go to **General** subtab, set **Working Directory** to *“Reuse previous session’s directory”.

#### System-wide hotkey to toggle iTerm2
Under **Keys** tab, in **Hotkey** section, enable *“Show/hide iTerm2 with a system-wide hotkey”* and input your hotkey combination, e.g. I use ```Ctrl + Shift + L```.

#### Switch pane with mouse cursor
Under **Pointer**, in **Miscellaneous Settings** section, enable *“Focus follows mouse”*.

#### Colors and Font Settings

* Download the **[Source Code Pro](https://github.com/adobe-fonts/source-code-pro)** font, and change the iTerm font to the Source Code Pro Lite 14pt.
* Download the **[Solarized dark](https://github.com/altercation/solarized/tree/master/iterm2-colors-solarized)** iTerm colors from here. And then set these to your default profile colors.