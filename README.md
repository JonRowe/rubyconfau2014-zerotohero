# Zero To Hero

We're going to be working through examples from the ground up but just to make
sure we're all running off the same page let's assert some basic setup here...

## Ruby

We're going to be aiming for Ruby 2.1.0 here (this is the future, honest), but
Ruby 2.0.0 is going to be ok, and so for the most part is 1.9.

If you're not familiar with the process of setting up Ruby, I'd advise you take
a look at the excellent [RailsGirls guide for setting up Ruby](http://guides.railsgirls.com/install/).


## Gems

We're going to be running cutting edge RSpec on the day, it's pretty easy, just
clone this repo and run `rake setup`, or your `bundle install` command of choice.

## Commands

To run RSpec style tests: `rake spec`
To run MiniTest style tests: `rake test`

If you'd prefer to run the rspec exectuable directly, you'll need to add `./bin/`
to your path, e.g: `export $PATH=./bin:$PATH`
