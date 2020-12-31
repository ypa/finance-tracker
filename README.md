# README

Finance tracker rails app

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version
2.7.2

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

## Deployment instructions

This repo is setup to deploy automatically to Heroku upon pushing to github `main` branch.

Also `RAILS_MASTER_KEY` env is set from heroku CLI:
This was a one time setup done from a machine that has master key in its `./config/` directory.
```sh
$ heroku config:set RAILS_MASTER_KEY="$(< config/master.key)"
```

Post deploy run migration from Heroku CLI:
```sh
$ heroku run rails db:migrate
```
