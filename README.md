# NUIG_hacky_hour
Site for NUIG Hacky Hour

This site will be used to notify members of meeting time/topics, as well as serving as a sandbox for trying out various web things.

# Testing Locally
## Managing ruby installations
We recommend using (`rbenv`)[https://github.com/rbenv/rbenv] to manage ruby installations, whichgets aroudn some of the issues of needing admin access.  You can find instructions here:
https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-14-04

In short, on ubuntu,

```
sudo apt-get update
sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

cd
git clone git://github.com/sstephenson/rbenv.git .rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bash_profile
source ~/.bash_profile


#  And then
rbenv install -v 2.2.3
rbenv global 2.2.3

```


## Running Jekyll

GitHub Pages uses a framework called Jekyll to generate the site.  You can install this for testing the site on your computer.
[Installing Jekyll](https://jekyllrb.com/docs/installation/)

Once you have jekyll installed, you can render the site:
```
# move to wherever you cloned this repository
cd NUIG_hacky_hour
# install bundle to handle jekyll's dependencies
gem install bundle
# install dependencies
bundle install
# run jekyll
bundle exec jekyll serve
```
From there, you should be able to go to the url [127.0.0.1:4000](127.0.0.1:4000) to see your site rendered from your computer.

# Deploying
Just commit and push your changes!
