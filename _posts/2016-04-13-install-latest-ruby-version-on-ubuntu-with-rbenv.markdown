---
published: true
title: Install Latest Ruby Version on Ubuntu with Rbenv
layout: post
tags: [rbenv, ruby, ubuntu]
---
*This tutorial was original presented by [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-14-04 "Digital Ocean"). I just edit to the Ruby latest version (2.3.0)*

Open your terminal and type the following commands:

// this will update your system and install require packages

    $ sudo apt-get update
    $ sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

// now you are going to clone Rbenv

    $ cd
    $ git clone git://github.com/sstephenson/rbenv.git .rbenv

// this lines add a path to Rbenv into your .bashrc file (configuration file for bash terminal), so you can access Rbenv just typing 'rbenv'

    $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
    $ echo 'eval "$(rbenv init -)"' >> ~/.bashrc

// git clone Ruby

    $ git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

// add Ruby command line into your bash

    $ echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
    $ source ~/.bashrc

// install Ruby version 2.3.0 with rbenv

    $ rbenv install -v 2.3.0
    $ rbenv global 2.3.0

// check if Ruby is installed and its version

    $ ruby -v

// type this line if you do not want Rubygems to generate local documentation for each gem that you install (I really prefer generate docs)

    $ echo "gem: --no-document" > ~/.gemrc

// install Ruby 'bundler' gem to manage your dependencies

    $ gem install bundler

That's all folks!
