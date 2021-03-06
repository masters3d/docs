# Exercism.io End-User Documentation

Markdown-driven static site.

Borrowed heavily from [lineman-docs](https://github.com/linemanjs/lineman-docs).

## Getting Started

1. Clone this repository.
* Run `gem install bundler` if you haven't already installed [bundler](http://bundler.io).
* Run `cd docs/` so that you are inside the directory that contains the repository.
* Run `bundle install` to install the sass dependency.
* Run `npm install -g lineman` if you haven't already installed [lineman.js](https://github.com/linemanjs/lineman#install).
* Run `npm install` to install required project dependencies.
* Run `lineman run` while you work on writing markdown files. Visit the site on [localhost:8000](http://localhost:8000)

If you are on Mac OS X, depending on your configuration one or more of the steps might fail. If a step fails, try to run the command with `sudo` in front of it, e.g. `sudo npm install -g lineman`.

If you need some more documentation on getting started with lineman, there's a [great tutorial](http://lineman-install.herokuapp.com/) for creating a "Hello, world" app.

The documentation topics live in `app/pages/**/*.md`. Lineman regenerates the site on save, so you don't need to restart the server.

## Creating New Topics

Include metadata at the top of the file. The required fields are `slug`, and `category`.

The `category` value must match the name of the directory that the file lives in.

The `ordinal` value allows posts to be sorted.

```plain
---
title: "Ruby"
slug: "ruby"
category: "languages"
ordinal: 1
---
```

Below the metadata, the documentation can be added using GitHub flavored markdown.

## Running on a different port

If you have multiple lineman apps, you may want to run this on something other than `8000`, which is the default.

```bash
$ WEB_PORT=9000 lineman run
```

## LICENSE

The MIT License (MIT)

Copyright (c) 2014 Katrina Owen, _@kytrinyx.com
