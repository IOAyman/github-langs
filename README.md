# Github Language Checker

[![Build Status](https://travis-ci.org/wildan3105/github-langs.svg?branch=master)](https://travis-ci.org/wildan3105/github-langs) [![HitCount](http://hits.dwyl.com/wildan3105/github-langs.svg)](http://hits.dwyl.com/wildan3105/github-langs)   [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/wildan3105/github-langs/issues)


## What ?

> Useful web checker to see what languages are used from a github account.

[Go to the web!](https://githublangs.herokuapp.com)

![Screenshot](screenshot3.png)

## Why ?

Let everyone know their languages statistic on github repo.

## Running the app locally
* Copy `.env.sample` to `.env`
* [Generate a GitHub OAuth client id and client secret](https://github.com/settings/applications/new) to ensure you don't get rate limited API call,
and add them to your `.env` file:
```
CLIENT_ID=your_client_id
CLIENT_SECRET=your_client_secret
```
* Install dependency : `npm install`
* Start the app `npm start` and go to : `http://localhost:5000`

## Running the app in production
You have to provide you [OpBeat](https://opbeat.com/) credentials as well in `.env` file:
```
OPBEAT_APP_ID=your_key
OPBEAT_ORGANIZATION_ID=your_key
OPBEAT_SECRET_TOKEN=your_key
```

## Running app through Docker

* Build image : `docker build -t local/github-langs .`
* Run image : `docker run -it -p 5000:5000 --env-file .env local/github-langs`
* App now available on `http://localhost:5000`

## TO DO LIST (sorted by priority) :
- [x] : Show repo > 100 (currently, only support repo < 100)
- [x] : Add vertical bar based on languages
- [x] : Refactor the controller (**urgent**) [#22](https://github.com/wildan3105/github-langs/issues/22)
- [x] : Beautify the page [#16](https://github.com/wildan3105/github-langs/issues/16)
- [ ] : Add social button (fb `share` & twitter `tweet`)
- [ ] : Save graph as image
- [ ] : Toggle graph color (white or colorful)
- [ ] : Redirect to `/me` if user already logged in (Github)
- [ ] : Improve UI
- [ ] : Increase speed & security

## Contributing

Check out this [page](CONTRIBUTING.md)

## License :

MIT (c) Wildan S. Nahar 2017
