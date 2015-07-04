# Homebrew

By far the best package manager for Mac OS. And trust me, I've been there with *MacPorts* and *Fink* and I know the reason Homebrew was created.

![](https://33.media.tumblr.com/51e823c71b55ccbda3b83501ec7bc78a/tumblr_nojspeQLd81uqyj6qo1_500.gif)

### Installation

Before installing [Homebrew](http://brew.sh/) make sure you have installed **Command Line Tools for Xcode**. This will be installed together with Xcode, but if you want to just install the Command Line Tools and not the full Xcode package, you can use this command:

```shell
$ xcode-select --install
```

Now that we've have everything, lets rock:

```shell
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Brews