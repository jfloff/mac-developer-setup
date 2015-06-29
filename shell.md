# Shell

The shell is the bread and butter of any developer (well, not really but you get the point). Hence you should the right amount of time configuring it to fit your needs, and to make sure you maximize your performance while using it.


It's just like Bilbo says: if you intend ride a horse all day, you just learn how to ride a horse.

![](http://28.media.tumblr.com/tumblr_lxjxfkj2bi1r0pci8o1_500.gi)

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


### iTerm 
If you're still using Terminal, stop it. Right now. Just close it, remove the shortcuts and do yourself a favour: install **[iTerm2](https://www.iterm2.com/)**. Future you will thank both you and me.


#### Colors Settings

First of all [download](https://github.com/altercation/solarized/tree/master/iterm2-colors-solarized) the Solarized color palette. This palette is designed to be very legible, and easy for your eyes.

Then, go to *Preferences* and load the Solarized Dark file that you just unzipped (click on 'Load Presets' and select the file):

![](iterm-solarized-settings.png)

Now, if your terminal doesn't look like this,

![](https://www.dropbox.com/s/3yvgky963r5wyyy/Screenshot%202015-06-29%2022.47.47.png)

don't worry! I've been there... It was awful. But stay calm, lets be a good Hobit and go through some steps:
* Confirm you iTerm terminal type in  iTerm2 Preferences > Terminal > Report Terminal Type, set to either xterm-256color or xtermAdd the following lines to .bashrc:

```shell
# Set CLICOLOR if you want Ansi Colors in iTerm2 
export CLICOLOR=1

# Set colors to match iTerm2 Terminal Colors
export TERM=xterm-256color
```


* Uncheck the "Draw bold text in bright color".



####Open tab/pane with current working directory
Under **Profiles** tab, go to **General** subtab, set **Working Directory** to *“Reuse previous session’s directory”.

#### System-wide hotkey to toggle iTerm2
Under **Keys** tab, in **Hotkey** section, enable *“Show/hide iTerm2 with a system-wide hotkey”* and input your hotkey combination, e.g. I use ```Ctrl + Shift + L```.

#### Switch pane with mouse cursor
Under **Pointer**, in **Miscellaneous Settings** section, enable *“Focus follows mouse”*.

#### Colors and Font Settings

* Download the **[Source Code Pro](https://github.com/adobe-fonts/source-code-pro)** font, and change the iTerm font to the Source Code Pro Lite 14pt.
* Download the **** iTerm colors from here. And then set these to your default profile colors.