# Ruby

Before installing Ruby, we will install **[rbenv](https://github.com/sstephenson/rbenv)**. 

*rbenv* manages  the Ruby versions for your applications and guarantee that your development environment matches production. I know that *rvm* is a more popular pick on this subject, but [this rundown](https://github.com/sstephenson/rbenv/wiki/Why-rbenv%3F) summarizes the good reasons to pick rbenv instead.

To install run:

```shell
$ brew install rbenv ruby-build rbenv-gem-rehash
```

For other usefull plugins checkout this [list](https://github.com/sstephenson/rbenv/wiki/Plugins). Here is my list:
* **rbenv-vars**: lets you set global and project-specific environment variables before spawning Ruby processes.
* **rbenv-default-gems**: creates a hook into the `rbenv install` command to automatically install gems every time you install a new version of Ruby.

There is a known bug with Mac OSX default openssl. Due to that, we have to install Hombrew's openssl package. 

```shell
# uninstall it first if you already have it
$ brew uninstall openssl

$ brew install openssl
```

After that, add the following line to your `~/.zshrc`. 

```shell
# To use Homebrew's directories rather than ~/.rbenv add to your profile:
export RBENV_ROOT=/usr/local/var/rbenv
# To enable shims and autocompletion add to your profile:
if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi
# To fix the openssl but with Homebrew package
export CONFIGURE_OPTS="--with-openssl-dir=`brew --prefix openssl`"
```

**Warning:** Make sure you add the following lines **after** the `PATH` definition.


Now, for each local environment, you have to set it (and install it if needed):

```shell
$ rbenv install 2.2.2
$ rbenv local 2.2.2
```

Then you can set your favorite Ruby version:

```shell
$ rbenv global 2.2.2
```

### Gems

First lets avoid gems to install documentation, we don't need that, we have the interwebs. Add this couple of lines to you `~/.gemrc` file:

```shell
install: --no-rdoc --no-ri
update: --no-rdoc --no-ri
```

The `rbenv-default-gems` plugin will automatically installs the gems listed in the `~/.rbenv/default-gems`, every time you successfully install a new version of Ruby with `rbenv install`. Here is my `default-gems` file:

```shell
bundler
```

</br>

Don't touch my *rubies* ...

![](http://33.media.tumblr.com/dfff76814a75fb49d0d7b570b9887c0a/tumblr_n9k0pukYAM1s3ulybo2_250.gif)