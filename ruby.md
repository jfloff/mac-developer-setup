# Ruby

Before installing Ruby, we will install **[rbenv](https://github.com/sstephenson/rbenv)**. 

*rbenv* manages  the Ruby versions for your applications and guarantee that your development environment matches production. I know that *rvm* is a more popular pick on this subject, but [this rundown](https://github.com/sstephenson/rbenv/wiki/Why-rbenv%3F) summarizes the good reasons to pick rbenv instead.

To install run:

```shell
$ brew install rbenv ruby-build rbenv-gem-rehash
```

For other usefull plugins checkout this [list](https://github.com/sstephenson/rbenv/wiki/Plugins). Here is my list:
* **rbenv-vars**: lets you set global and project-specific environment variables before spawning Ruby processes.
* 

For each local environment, you have to set it (and install it if needed):

```shell
$ rbenv install 2.2.2
$ rbenv local 2.2.2
```

Then you can set your favorite Ruby version:

```shell
$ rbenv global 2.2.2
```







</br>

Don't touch my *rubys* ...

![](http://33.media.tumblr.com/dfff76814a75fb49d0d7b570b9887c0a/tumblr_n9k0pukYAM1s3ulybo2_250.gif)