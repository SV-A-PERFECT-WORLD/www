---
---

[![A PERFECT WORLD](./i/title_2560.jpg)](/)

## authoring setup

1. create a local Gemfile consisting of following two lines:

       source "https://rubygems.org"
       gem "github-pages", group: :jekyll_plugins

   this is to activate included head-custom.html which is applied via the minima theme

   GH pages imply their own, most likely with a recent version of minima theme, but I don't want to override the whole Gemfile on the server side

1. prepare for the following (bundle install) step:

       sudo chown -R $USER /usr/local/bin/
       sudo chown -R $USER /var/lib/gems/3.1.0

1. run 

       bundle install

1. run 

       bundle exec jekyll serve --incremental

1. verify that Jekyll applies styles from centrally included head-custom.html

   e.g. headings like Values and Goals being typeset in Fredericka font, and Goals have colored labels
