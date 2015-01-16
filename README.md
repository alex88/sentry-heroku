Sentry 7 running on Heroku
========================

Using this as base repo you can easily deploy sentry on heroku

# Automatic setup

Just click on the deploy button to create a new app with preinstalled sentry and the required redis/postrgesql/sendgrid addons (free)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/alex88/sentry-heroku)

Be sure to set an app name and change the environemnt variable accordignly.
In case you didn't do that, use this command to set the sentry base url:

```
heroku config:set SENTRY_URL_PREFIX=https://YOURAPPNAME.herokuapp.com --app YOURAPPNAME
```

and, using `heroku run` you've to create a new superuser:

```
heroku run "sentry --config=sentry.conf.py createuser" --app YOURAPPNAME
```