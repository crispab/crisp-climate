---
---
# Climate Crisplet - tech setup for the site

Climate crisplet is a web site that describes our work with reducing global warming. The source lives on github and is auto-published on [http://climate.crisp.se](http://climate.crisp.se) every time a change is pushed.

Below are instructions for how to set up a local development environment.

## 1. Install GIT

Here's [how to install GIT](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git). 

## 2. Clone the repo

Tell git to download the crisp-dna source:

    git clone https://github.com/crispab/crisp-climate.git
	cd crisp-climate

You should now have the whole thing, including the README.md file that you are reading right now!

The web site source files are under the main directory! They are written using markdown. When you push to github, it will automatically convert the pages to static html and build the site http://climate.crisp.se. 

## 3. Install Jekyll and related tools

To test the site locally, you need to install jekyll (the tool that github uses to generate sites), which in turn relies on some Ruby stuff. But you can do all easily via Ruby bundler, like this:

First install Ruby if you don't already have it, for example via [homebrew](http://brew.sh).

    brew install ruby

Then install the Ruby Bundler gem, if you don't already have it.

    gem install bundler

Next, tell the bundler to install all the gems needed (jekyll, github-pages, etc). They are listed in Gemfile in case you are curious.

	bundle install	

Congrats! You got the stuff you need. You should now be ready to....

## 4. Run the site locally!

Tell Jekyll to generate the site and serve it up:

    jekyll serve

That's it, your local copy of the Climate Crisplet site should be up and running on
[http://localhost:4000](http://localhost:4000)
