# Git

Yes, our white knight, our savior is here: *Git*.

![](http://ak-hdl.buzzfed.com/static/2014-05/enhanced/webdr07/21/13/anigif_enhanced-12395-1400693542-1.gif)

What's a developer without Git? To install, simply run:

```shell
$ brew install git
```

Now type:

```shell
$ which git
```

... oops! looks like our OS is still using the pre-installed version of git.To fix it you need to tell bash to look in the correct path for the Homebrew managed version of Git.

Just execute this command and then restart terminal:

```shell
echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.zshrc
```

Take note that this command is for *zsh* shell. 
