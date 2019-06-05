---
layout: post
title: Install jekyll
subtitle: start my blog
date: 2018-05-13
author: deng liuyan
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - Blog
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
#### jekyll run with draft visible
`jekyll serve --draft`

#### Run
create jekyll project,and then add gem theme in Gemfile
```bash
bundle install
bundle exec jekyll serve
```
#### Conclusion

let's start。
