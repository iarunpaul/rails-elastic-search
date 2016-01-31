ES-Tutorial
===========

This repository is a sample application for my Elastic Search with Ruby on Rails
article published on [tutorials.pluralsight.com][1]

How to set it up
----------------

As usual you will need to:

```bash
bundle install
rake db:migrate
```

Now you will need to turn an Elastic Search instance online on port `9300` and
then initialise the sample search data from Wikipedia provided with the repo.

It is important to have Elastic Search running prior to running `rake db:seed`
as it will also appropriately index the data in ES.

```bash
elasticsearch >/devnull </dev/null &
rake db:seed
```

[1]: http://tutorials.pluralsight.com