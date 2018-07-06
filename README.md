# NUIG_hacky_hour
Site for NUIG Hacky Hour

This site will be used to notify members of meeting time/topics, as well as serving as a sandbox for trying out various web things.

# Testing Locally
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
