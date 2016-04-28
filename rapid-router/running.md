---
layout: default
title: Running locally
---

## To run the app locally
* Clone the repo
* Make and activate a virtualenv (We recommend [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/index.html) - [this blog post](http://mkelsey.com/2013/04/30/how-i-setup-virtualenv-and-virtualenvwrapper-on-my-mac/) may also be
 useful if you're using a Mac)
    * e.g. the first time, `mkvirtualenv -a path/to/rapid-router rapid-router`
    * and thereafter `workon rapid-router`
* `./run` in your rapid-router dir - This will:
    * install all of the dependencies using pip
    * sync the database
    * collect the static files
    * run the server

