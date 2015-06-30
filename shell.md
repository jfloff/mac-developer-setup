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

#### Terminal Drop down

iTerm 2 has a very useful and timesaving feature where you can make the terminal dropdown from the top of the screen with just a key press. Very useful if you need access to the terminal quickly, and don’t want to alt + tab to eternity.

To enable this, go to *iTerm > Preferences > Profiles - Default > Window*, here you should see a dropdown menu called "Style". Choose **"Top of screen"** in the dropdown. Also, you might want to up the transparency a bit, so you can see while typing. 

Next set a **system-wide hotkey**. Under *Keys > Hotkey* section, enable **“Show/hide iTerm2 with a system-wide hotkey”** and input your hotkey combination, e.g. ```Ctrl + Shift + L```. 

Et Voilá! 

#### Colors Settings

First of all [download](https://github.com/altercation/solarized/tree/master/iterm2-colors-solarized) the Solarized color palette. This palette is designed to be very legible, and easy for your eyes.

Then, go to *Preferences* and load the Solarized Dark file that you just unzipped (click on 'Load Presets' and select the file):

![](iterm-solarized-settings.png)

Now, if your terminal doesn't look like this,

![](https://www.dropbox.com/s/3yvgky963r5wyyy/Screenshot%202015-06-29%2022.47.47.png)

don't worry! I've been there... I want my 3 hours back. But stay calm, lets be a good Hobbit and go try each one of these steps:
* Confirm you iTerm terminal type in *Profiles - Default > Terminal > Report Terminal Type*, set to **```xterm-256color```**. Then add the following lines to .bashrc:

```shell
# Set CLICOLOR if you want Ansi Colors in iTerm2 
export CLICOLOR=1

# Set colors to match iTerm2 Terminal Colors
export TERM=xterm-256color
```

* Check if *Profiles - Default > Colors > Minimum Contrast* value it's high. If it is you might only get black and white.

* Uncheck the "Draw bold text in bright color" in *Profiles - Default > Text*.


#### Other settings
* **Open tab/pane with current working directory:** go to *Profiles - Default > General** and set **Working Directory** to *“Reuse previous session’s directory”.

* 