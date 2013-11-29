# Transponder
[![Build Status](https://travis-ci.org/artellectual/transponder.png?branch=master)](https://travis-ci.org/artellectual/transponder) - Master (current release)

[![Build Status](https://travis-ci.org/artellectual/transponder.png?branch=develop)](https://travis-ci.org/artellectual/transponder) - Develop (upcoming release)

Transponder is a opinionated javascript library for assisting in working with front end heavy rails app.

## Installation

Add this line to your application's Gemfile:

    gem 'transponder'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install transponder

## Usage

Once installing the gem run.

    $ rails g transponder:install application

or 

    $ rails g transponder:install application --full

You may be wondering whats the difference between the one with ```--full``` and the one without

Basically there are 2 types of transponder apps basic one and a full one. A full one will give you models / collection / views / templates as well as transponder's own basic primitives.This means you can integrate backbone's primitives into transponder. So if your planning on doing very complex client side stuff and would like to use backbone as well use the ```--full``` flag to generate all the right folders.

### Presenters
Presenter's jobs are to take the response from the server usually html fragment that is rendered by rails and output it to the screen. The reason why we have presenters is so that we can do things to the content before outputting it.

Presenters usually map to your controller action in rails. By default it supports the 7 basic restful actions 

+ index
+ new
+ edit
+ show
+ create
+ update
+ destroy

However you can override this and add your own custom presenter actions if you want. Its not necessary that the presenter action maps to your rails controller action.

### Services
Services are things that apply to alot of items on the page. You could think of these parts of the page as 'widget' and they all have a certain kind of behavior. The behavior of these widgets can be defined by services. Each widget can have the behavior of multiple services.

Some example of services

+ File uploader
+ Poller
+ Push notification subscriber
+ Syntax Highlighter
+ Search Bar

Services are very modular and they can be applied to multiple widgets in a page without conflicting with each other and without rebinding widgets that already have these behaviors.


## TODO - Whats Coming

  + Clean up some APIs
  + Add Documentation
  + Video Screencasts
  + More Generators
  + Example Rails Project

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

