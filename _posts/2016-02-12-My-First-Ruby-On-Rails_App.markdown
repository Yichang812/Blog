---
layout: post
title:  "My First Ruby On Rails App"
date:   2016-02-12 19:55
categories: [Web App]
tags: [Ruby on rails]
---

_I start my first rudy on rails project by following [this](https://www.youtube.com/watch?v=GY7Ps8fqGdc) tutorial._

### Installation 
 - [Ruby on Rails](http://installrails.com/steps/choose_os)
 - MySQL (installed by [Homebrew](http://brew.sh))
 
 _Make sure the version of your rails (4.2.0+) and ruby (2.2.0+)_
 
### Initiation

```
$ rails new [project name] -d mysql
$ cd [project name]
$ bundle install
```
_Remember to configer your database.yml (Add socket, password, etc.)_

### Basic commands

To create a new rails controller with action inside:

```
$ rails generate controller [controller name] [action name] 
```

### Ruby tags

```html
<% ruby code%>
<%= ruby with output%>
<%# comments%>
```