Sentry running on Heroku
========================

Using this as base repo you can easily deploy sentry on heroku

# Automatic setup

Just click on the deploy button to create a new app with preinstalled sentry and the required redis/postrgesql addons (free)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/alex88/sentry-heroku)

Then, you've to set an environment variable using your new app name:

```
heroku config:set SENTRY_URL_PREFIX=https://YOURAPPNAME.herokuapp.com --app YOURAPPNAME
```

and, using `heroku run` you've to create a new superuser:

```
heroku run "sentry --config=sentry.conf.py createuser" --app YOURAPPNAME
```