---
layout: post
title: Updated ruby on OS X 12 using HomeBrew
categories: []
tags: []
description: 
comments: true
---

My old Gemfile.lock had a dependency with a known DoS vulnerability and Github notified me to fix. This ran into some issues of OS X 12 install of ruby (v 2.0.0) so I decided to switch over to HomeBrew and manage my own ruby env there. 

# Setup

Install HomeBrew:

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Now set up with `rbenv` to manage different ruby install versions

``` sh
brew update && brew upgrade
brew doctor

brew install rbenv
brew install ruby-build
echo 'export RBENV_ROOT=/usr/local/var/rbenv' >> ~/.bash_profile
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile

rbenv install -l
rbenv install 2.4.0
```

Open a new terminal and `rbenv shell 2.4.0`

Check this has all completed correctly with `rbenv versions` should show OS X v of 2.0.0 and my installed version of 2.4.0. Then check with `ruby --version` now that I have set the global for this bash session to 2.4.0 and it should return that as the version. Can also check the ruby location with `which ruby`.

Then install bundler with `gem install bundler`
Then install jekyll with `gem install jekyll` 

Once this was completed I changed to my github pages directory in my terminal session. Then I used bundle to check my Gemfile and install the dependencies:
``` sh
bundle
bundle install
```

That updated my Gemfile.lock to the latest versions of dependcies for Github pages.

# Ongoing maintenance 

To move from the system to another ruby version per shell session start with

`rbenv shell 2.4.0`

Then run

`bundle exec jekyll serve` 

