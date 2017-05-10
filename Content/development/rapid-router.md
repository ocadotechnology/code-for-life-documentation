---
layout: page
title: Rapid Router
---
<hr>


Rapid Router is the first Code for life project, aimed at teaching primary school children the concepts of programming, through a vehicle routing game.

You can [try Rapid Router for yourself](https://www.codeforlife.education/rapidrouter/).

You can access the source code for Rapid Router on Github, in the following repository:

[https://github.com/ocadotechnology/rapid-router](https://github.com/ocadotechnology/rapid-router)

This page explains how to get started developing for Rapid Router, and how to contribute code to the project.

<hr>

## On this page

* [Run Rapid Router locally](#run-rapid-router-locally)
* [Enable localisation in Rapid Router](#enable-localisation-in-rapid-router)

<hr>

## Run Rapid Router locally

To run Rapid Router locally:

1. Run the following commands to install the necessary prerequisites:

	* `sudo apt-get install git`
	* `sudo apt-get install virtualenvwrapper`
	* `sudo apt-get install python-dev`
	* `sudo apt-get install libxml2-dev libxslt1-dev zlib1g-dev`
	* `sudo apt-get install ruby2.0`
	* `sudo gem install sass -v 3.3.4`

2. Clone the repository

	Follow the instructions [here](../../get-involved#contribute-to-the-code) to learn how to fork and clone the Rapid Router project.

3. Create and activate a virtual environment. We recommend using **virtualenvwrapper**.

	The first time you want to create and activate the environment, run the following command:

	`mkvirtualenv -a path/to/rapid-router rapid-router`

	Every other time, you can just run:

	`workon rapid-router`

	You can find out more about virtualenvwrapper [here](http://virtualenvwrapper.readthedocs.io/en/latest/index.html).

4. Run the `./run` command in your Rapid Router directory.

	The `./run` command:

	* installs all of the dependencies using pip
	* syncs the database
	* collects the static files
	* runs the server

	After you have run the command, you should see the message `Quit the server with CONTROL-C` displayed.

5. Open a browser window and go to [localhost:8000](http://localhost:8000).

	The portal dislays in your browser.

You can now run Rapid Router locally.

### Can't see the portal?

You might not be able to see the portal if you're running it on a machine with a different locale. 

If you can see the error message `ValueError: unknown locale: UTF-8` in the terminal, you need to set both `LANG` and `LC_ALL` environment variables and to `en_US.UTF-8`.

To do this, either:

* export them in your `.bashrc` or `.bash_profile`
* restart the portal with the command `LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8 ./run`

<hr>

## Enable localisation in Rapid Router

To enable localisation for Rapid Router:

1. Run the following command in your Rapid Router directory to include the localisation libraries:

	`./run --with-translation-tools`

2. Get your crowdin API key.

	You can get this from the [settings page](https://crowdin.com/login#integration) of your account.

3. Add your crowdin API key to the `CROWDIN_API_KEY` environment variable.

	It should look something like this:

	`export CROWDIN_API_KEY=<your_key>`

4. Set your `django_language` cookie to `lol-us` to enable in-context localisation.

You have enabled localisation for Rapid Router.