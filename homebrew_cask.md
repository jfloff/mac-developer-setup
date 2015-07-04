# Homebrew Cask

You know how we Mac users brag about our installers? The famous "To install, drag this icon"? Well, that's about to change.

[Homebrew Cask](http://caskroom.io/) extends Homebrew and brings its elegance, simplicity, and speed to OS X applications and large binaries alike.

Your software is just one command away from being ready and raring to go. Forget all about babysitting the install process step by step, from website to cleanup.

Cask does one thing, does it well, and plays nice with others. Apps are kept in their Caskroom under /opt and symlinked to your ~/Applications folder.


### Instalation

First, make sure you need Homebrew installed, and then run this line:

```shell
$ brew install caskroom/cask/brew-cask
```

### Applications

Usually, I use the App Store for the applications that are available (to take advantage its auto-update feature). When That doesn't happen, I install it using *cask*. 

Here's a list of all applications (even the ones that are on the App store) that I have mentioned in the apps section:

```shell
$ brew cask install alfred
$ brew cask install google-chrome
$ brew cask install caffeine
$ brew cask install cheatsheet
$ brew cask install atom
$ brew cask install sublime-text
$ brew cask install iterm2
$ brew cask install dropbox
$ brew cask install transmission
$ brew cask install vlc
$ brew cask install apptrap
$ brew cask install 
$ brew cask install asepsis
```

### Quick look plugins
[Plugins](https://github.com/sindresorhus/quick-look-plugins) to enable different files to work with Mac OSX's Quicklook feature.

| Description | Install |
| -- | -- |
| Preview source code files with syntax highlighting | ```$ brew cask install qlcolorcode``` |
| Preview plain text files without a file extension | ```$ brew cask install qlstephen``` |
| Preview Markdown files | ```$ brew cask install qlmarkdown``` |
| Preview JSON files | ```$ brew cask install quicklook-json``` |
| Preview .patch files | ```$ brew cask install qlprettypatch``` |
| Preview CSV files | ```$ brew cask install quicklook-csv``` |
| Preview archives | ```$ brew cask install betterzipql``` |
| Display image size and resolution | ```$ brew cask install qlimagesize``` |
