---
layout: post
title: Install jekyll
date: 2019-05-13 15:52:24.000000000 +09:00
---
Start my blog；
#### Install RVM
```bash
curl -sSL https://get.rvm.io | bash -s stable
rvm list known
```
#### rvm install ruby
```bash
rvm install ruby-2.4.1
rvm use ruby-2.4.1
rvm --default use 2.4.1
```
#### install jekyll
```bash
gem sources --add https://gems.ruby-china.com/
gem install jekyll
```
#### Run
create jekyll project,and then add gem theme in Gemfile
```bash
bundle install
bundle exec jekyll serve
```
#### Conclusion

let's start。
