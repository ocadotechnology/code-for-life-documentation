---
layout: page
title: AI:MMO
---

<hr>

AI:MMO is our second game, aimed as a follow up to [Rapid Router](../rapid-router) for teaching computing to secondary school children. AI:MMO is a **M**assively **M**ulti-player **O**nline game, where players create **A**rtificially **I**ntelligent programs to play on their behalf.

You can access the source code for AI:MMO on Github, in the following repository:

[https://github.com/ocadotechnology/aimmo](https://github.com/ocadotechnology/aimmo)

This page explains how to get started developing for AI:MMO, and how to contribute code to the project.

<hr>

## On this page

* [Run AI:MMO locally](#run-aimmo-locally)
* [Quick commands](#quick-commands)

<hr>

## Run AI:MMO locally

To run the AI:MMO project locally:

1. Clone the repository

	Follow the instructions [here](../../get-involved#contribute-to-the-code) to learn how to fork and clone the AI:MMO project.

2. Create and activate a virtual environment. We recommend using **virtualenvwrapper**.

	The first time you want to create and activate the environment, run the following command:

	`mkvirtualenv -a path/to/aimmo aimmo`

	Every other time, you can just run:

	`workon aimmo`

	You can find out more about virtualenvwrapper [here](http://virtualenvwrapper.readthedocs.io/en/latest/index.html).

3. Run the `./run` command in your AI:MMO directory.

	The `./run` command:

	* if necessary, create a superuser with the password 'admin'
	* installs all of the dependencies using pip
	* syncs the database
	* collects the static files
	* runs the server

You can now run AI:MMO locally.

<hr>

## Quick commands

To create an admin account, run the following command:

`python example_project/manage.py createsuperuser`

You can quickly create players as desired by running the following command:

`python example_project/manage.py generate_players 5 dumb_avatar.py`

This creates five users with the password '123', and creates an avatar that runs the code in the file dumb_avatar.py, for each user.

You can delete the generated players by running the following command:

`python example_project/manage.py delete_generated_players`




