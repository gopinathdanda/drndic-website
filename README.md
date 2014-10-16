# Drndić Lab Website

This is the source code for the [Drndić Lab Website](http://www.physics.upenn.edu/drndicgroup/).

It is built with [Jekyll], a static-site generator, and uses [Foundation] as a responsive front-end framework.

## Dependencies

You'll need to have the following items installed before continuing.

### [Jekyll]

[Jekyll] is used for static site generation. Basically, you write your website using [Jekyll]'s formatting, and then use [Jekyll] to turn your simple code into the many pages of your website.

Note that Windows is **not** an officially supported platform, although instructions exist to help with the installation.

 * [Jekyll]'s [Jekyll on Windows page](http://jekyllrb.com/docs/windows/#installation).
 * Julian Thilo's [Run Jekyll on Windows tutorial](http://jekyll-windows.juthilo.com/).

Instructions for installing [Jekyll] can be found [here](http://jekyllrb.com/docs/installation/), summarized below. 

 1. [Install Ruby](http://www.ruby-lang.org/en/downloads/) (Including development headers).
 2. [Install Ruby Gems](http://rubygems.org/pages/download) (Comes with Ruby on Ubuntu).
 3. [Install NodeJS](http://nodejs.org/).
 4. Install [Jekyll] (May need sudo). 
```bash
$ gem install jekyll
```

### [Foundation]

[Foundation] is a responsive front-end framework. Basically, it comes with a bunch of CSS/SCSS styles that you can use to easly create sites that look good on both mobile and desktop environments.

Installation instructions are [here](http://foundation.zurb.com/docs/sass.html) (see libsass version), and are summarized below.

1. [Foundation] uses [Bower](http://bower.io/) to manage updates to [Foundation] and the third-party libraries that [Foundation] is built on.

  ```bash
$ npm install -g bower grunt-cli
  ```

2. Installing the Foundation CLI

  ```bash
$ gem install foundation
  ```

## Getting started with the source

First, clone the repo and move to the directory.

```bash
$ git clone https://github.com/parkin/drndic-website.git
$ cd drndic-website
```

Next, install the node modules.

```bash
$ npm install
```

This should create the directory `node_modules` and populate it with the modules needed.

Then, install the bower components. Bower is used to to keep Foundation assets up to date within the project.

```bash
$ bower install
```
This should create the directory `bower_components` and populated it with the components needed.

Now, you should be ready to build the site.

## Building and previewing the site

[Jekyll] takes this website source code and builds the full html pages for the entire site, and sticks those pages by default in the `_site` directory. So, if you want to actually see the website or see any changes you make, you need to rebuild the site. There are three steps in this process.

1. Compile [SASS](http://sass-lang.com/) files to CSS. This is done with [libsass](http://libsass.org/), and can be triggered with the following command. Note that at the moment, this only applies if you change any `.scss` file.

  ```bash
$ grunt build
  ```
  
2. Compile the website source using [Jekyll]. This takes the source code from this website and outputs the working website in the `_site` directory, by default. Use the command

  ```bash
$ jekyll build
  ```
3. To view the site, start a server that serves from the `_site` directory. There are many ways to do this, but one way is
 
  ```bash
$ jekyll serve
  ```
Then open a browser and go to [http://localhost:4000/](http://localhost:4000/)



[Jekyll]: http://jekyllrb.com/
[Foundation]: http://foundation.zurb.com/
